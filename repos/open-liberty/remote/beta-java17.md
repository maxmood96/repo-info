## `open-liberty:beta-java17`

```console
$ docker pull open-liberty@sha256:c785ac5cbb1d0cd3d527f5836de9e9d1739266724043d8714650596e6c39384b
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
$ docker pull open-liberty@sha256:e3353d9c1e0bb238b46c302e64387b781c9e76aefb8a5331934ba91919fea3c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **470.7 MB (470685474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e6455d12bf7190625cde42595fe70f9c9e3ce32a92d6f0cb8962d46aad87ba`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Wed, 17 Jul 2024 15:19:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jul 2024 15:19:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV JAVA_VERSION=jdk-17.0.12+7_openj9-0.46.0
# Wed, 17 Jul 2024 15:19:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c0e0ccad2ceb4e35321fcf7871571c1bc3ccaf98a41b7e15c530ea510fe646e3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.0/ibm-semeru-open-jre_aarch64_linux_17.0.12_7_openj9-0.46.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='ff35f2abcd84ac92f59aa501cd546399d1be97eca3404d263c13fa6c2272c34d';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.0/ibm-semeru-open-jre_ppc64le_linux_17.0.12_7_openj9-0.46.0.tar.gz';          ;;        amd64|x86_64)          ESUM='8227ff054505167ca7f379ad0ec618614ba72ab90fb4bf8f90b7db87d2f122f7';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.0/ibm-semeru-open-jre_x64_linux_17.0.12_7_openj9-0.46.0.tar.gz';          ;;        s390x)          ESUM='8327736054aa9f1f1ccad4ef2aee4a4fa3362cc93930fe0d34ab79b2a2741d1a';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.0/ibm-semeru-open-jre_s390x_linux_17.0.12_7_openj9-0.46.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jul 2024 15:19:40 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 17 Jul 2024 15:19:40 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
USER root
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_VERSION=24.0.0.8-beta
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_BUILD_LABEL=cl240720240701-1102
# Wed, 17 Jul 2024 15:19:40 GMT
ARG OPENJ9_SCC=true
# Wed, 17 Jul 2024 15:19:40 GMT
ARG VERBOSE=false
# Wed, 17 Jul 2024 15:19:40 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240720240701-1102 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=24.0.0.8-beta
# Wed, 17 Jul 2024 15:19:40 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 17 Jul 2024 15:19:40 GMT
USER 1001
# Wed, 17 Jul 2024 15:19:40 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 17 Jul 2024 15:19:40 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 17 Jul 2024 15:19:40 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1828da88ba930dff47373f1ad91e410933a3763cae0a116c3928f13ec47a7598`  
		Last Modified: Mon, 12 Aug 2024 17:59:19 GMT  
		Size: 12.2 MB (12156576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f6261c5043debeaa6ca14787b499ee7a6d80dff8a0f1abea681d49bd55749c`  
		Last Modified: Mon, 12 Aug 2024 17:59:20 GMT  
		Size: 51.5 MB (51534687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df24d8997c73e863bac33ac3b7903884866f6ba1cf44a0b80f329f09399622f1`  
		Last Modified: Mon, 12 Aug 2024 17:59:19 GMT  
		Size: 5.0 MB (4966846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3250196bdc22cb9cf6e0be1421dca1f48c7629ee5e2dcba51ab160a99dece588`  
		Last Modified: Mon, 12 Aug 2024 18:54:38 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2986e48dbe8ee211763fb7ab8a2cc3ddffa8d87bfc2b175e8980dee9fd9c06ba`  
		Last Modified: Mon, 12 Aug 2024 18:54:38 GMT  
		Size: 10.0 KB (9991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21e98a4debabd17d6904683ad3eeb016b59a7f42f776c3c8ba4ad63fb05bde9`  
		Last Modified: Mon, 12 Aug 2024 18:54:38 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98d2d360e1ddd6d02c1b75055206bec0500e6827ff12da7ff780dd3390723f1`  
		Last Modified: Mon, 12 Aug 2024 18:54:38 GMT  
		Size: 31.7 KB (31745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3e734dd41ad6b2b7213e1a8d95b9dbdfc6515422746b01b5fb55865c853afd`  
		Last Modified: Mon, 12 Aug 2024 18:54:44 GMT  
		Size: 358.5 MB (358519441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cb1764425f0ef340088ec4ad20842a2b20f9608e613d7c17aa4c0a0c84daa5`  
		Last Modified: Mon, 12 Aug 2024 18:54:39 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03fe099d3865201fe9e51c615cb25d718c472994868eefc8b3df347102210a9`  
		Last Modified: Mon, 12 Aug 2024 18:54:39 GMT  
		Size: 11.3 KB (11342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3a9134860535f54f1786c342aedb0bdf33a8fefdc55a5e938e8dbcbd9c144f`  
		Last Modified: Mon, 12 Aug 2024 18:54:40 GMT  
		Size: 13.9 MB (13918446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java17` - unknown; unknown

```console
$ docker pull open-liberty@sha256:b6de9833b5187786452b2be69adea6713d5071edb7a915bb857764eedc13c00b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5443742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a63b59bc1fbe68a8a957219517def4c20faa28ad2595f1469ddaa9baff41f8d4`

```dockerfile
```

-	Layers:
	-	`sha256:4a89f91e6c643739ff8e5bd7c884603388a270e7e2689cd3b715bed9e8ff913c`  
		Last Modified: Mon, 12 Aug 2024 18:54:39 GMT  
		Size: 5.4 MB (5405081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfb53e7c27fd71e1e0940bc30e27626773cd4d51fca1bf77dba69e8c1e4e6c0a`  
		Last Modified: Mon, 12 Aug 2024 18:54:38 GMT  
		Size: 38.7 KB (38661 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta-java17` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:8c0fa4596b9500feb022465ca7b44fcd2f5ef231bb976c2e9196e9ffb8533a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.9 MB (463874644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af5148b48ad664688a18468fa00f29e1350d3180b3731738c34cce1f5a6c7271`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Wed, 17 Jul 2024 15:19:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jul 2024 15:19:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV JAVA_VERSION=jdk-17.0.12+7_openj9-0.46.0
# Wed, 17 Jul 2024 15:19:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c0e0ccad2ceb4e35321fcf7871571c1bc3ccaf98a41b7e15c530ea510fe646e3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.0/ibm-semeru-open-jre_aarch64_linux_17.0.12_7_openj9-0.46.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='ff35f2abcd84ac92f59aa501cd546399d1be97eca3404d263c13fa6c2272c34d';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.0/ibm-semeru-open-jre_ppc64le_linux_17.0.12_7_openj9-0.46.0.tar.gz';          ;;        amd64|x86_64)          ESUM='8227ff054505167ca7f379ad0ec618614ba72ab90fb4bf8f90b7db87d2f122f7';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.0/ibm-semeru-open-jre_x64_linux_17.0.12_7_openj9-0.46.0.tar.gz';          ;;        s390x)          ESUM='8327736054aa9f1f1ccad4ef2aee4a4fa3362cc93930fe0d34ab79b2a2741d1a';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.0/ibm-semeru-open-jre_s390x_linux_17.0.12_7_openj9-0.46.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jul 2024 15:19:40 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 17 Jul 2024 15:19:40 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
USER root
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_VERSION=24.0.0.8-beta
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_BUILD_LABEL=cl240720240701-1102
# Wed, 17 Jul 2024 15:19:40 GMT
ARG OPENJ9_SCC=true
# Wed, 17 Jul 2024 15:19:40 GMT
ARG VERBOSE=false
# Wed, 17 Jul 2024 15:19:40 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240720240701-1102 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=24.0.0.8-beta
# Wed, 17 Jul 2024 15:19:40 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 17 Jul 2024 15:19:40 GMT
USER 1001
# Wed, 17 Jul 2024 15:19:40 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 17 Jul 2024 15:19:40 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 17 Jul 2024 15:19:40 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3bd8d80133d843daaa8d5b12adef4a1bb1a9950ef8a5bb999ca2111d459a677`  
		Last Modified: Mon, 12 Aug 2024 18:01:16 GMT  
		Size: 12.1 MB (12114290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b10ee8e18379644bd5859681f1868c100a4b225e7c4d32345b7dab3c2ac7e9`  
		Last Modified: Mon, 12 Aug 2024 18:12:48 GMT  
		Size: 47.9 MB (47916674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a53e736f6ac3b56dfe0b3dbf90879e8f51e9e12993520ab68e2b3715de7ab4`  
		Last Modified: Mon, 12 Aug 2024 18:12:47 GMT  
		Size: 4.7 MB (4689464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d71dbdd18bc60bcd2d033b98cdb0c5443af7e4d638f4d82df18108db904858a`  
		Last Modified: Mon, 12 Aug 2024 19:05:51 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042093bff9b56c1109655fdb8f5d1c4d50ee6ebf296ab885ec2f53d8adec0876`  
		Last Modified: Mon, 12 Aug 2024 19:05:51 GMT  
		Size: 10.0 KB (9987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6a93723cfd9ca7880ae7f29b2bcc5f43cc930feb497aabd306f8fd803de761`  
		Last Modified: Mon, 12 Aug 2024 19:05:51 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d853900886382ca641f28a4a31a5a9aa28dc8bdd5302da95b335a825c59cbd`  
		Last Modified: Mon, 12 Aug 2024 20:19:23 GMT  
		Size: 42.3 KB (42324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3c80e05f6f78c5d30e05bd058bce7ca5b6d5fd24f1b0e7970051eab2358129`  
		Last Modified: Mon, 12 Aug 2024 20:19:30 GMT  
		Size: 358.5 MB (358519713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c562d1d7a418ac4dfc7e8272b1d3c8d10a6648a239d705d58cc3f352c14392b2`  
		Last Modified: Mon, 12 Aug 2024 20:19:23 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d675b2e6386eee2acfdceda0a38e96c6dc4bdd5f86a71f075646682ab8d81aa7`  
		Last Modified: Mon, 12 Aug 2024 20:19:23 GMT  
		Size: 11.3 KB (11344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bc8a8cdedc29efd5bab6edaafbeba1556e6fb3ed2696b52705cfd4a5799079`  
		Last Modified: Mon, 12 Aug 2024 20:19:24 GMT  
		Size: 13.2 MB (13208475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java17` - unknown; unknown

```console
$ docker pull open-liberty@sha256:1e1096e75fd4eaf0d2a1b469bffee6e8162a2957fd24398bbcef9edf0e66aa14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c04251b6829067046f655905f2155604dfe4c40cdef753ccca708651cf2bdb`

```dockerfile
```

-	Layers:
	-	`sha256:4ceced37a4d826218fe1e3e8a1478de9d7b2e9f70deffdfbdfdae62326778ca7`  
		Last Modified: Mon, 12 Aug 2024 20:19:23 GMT  
		Size: 5.4 MB (5405334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:464662ce587d2e3f945144941facb05793e3afe5ae343c7a559a796241a9592e`  
		Last Modified: Mon, 12 Aug 2024 20:19:22 GMT  
		Size: 39.0 KB (39010 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta-java17` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:6b6c87346ed7d9431300de7ad28ca5ca1a32a635a735fbf26d5718ba71d7f751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **474.7 MB (474713555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94994a1d24f8e446fe6f2f2db07c3d438a78d85f33d933e718a182dfa6b394ee`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Wed, 17 Jul 2024 15:19:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jul 2024 15:19:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV JAVA_VERSION=jdk-17.0.12+7_openj9-0.46.0
# Wed, 17 Jul 2024 15:19:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c0e0ccad2ceb4e35321fcf7871571c1bc3ccaf98a41b7e15c530ea510fe646e3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.0/ibm-semeru-open-jre_aarch64_linux_17.0.12_7_openj9-0.46.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='ff35f2abcd84ac92f59aa501cd546399d1be97eca3404d263c13fa6c2272c34d';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.0/ibm-semeru-open-jre_ppc64le_linux_17.0.12_7_openj9-0.46.0.tar.gz';          ;;        amd64|x86_64)          ESUM='8227ff054505167ca7f379ad0ec618614ba72ab90fb4bf8f90b7db87d2f122f7';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.0/ibm-semeru-open-jre_x64_linux_17.0.12_7_openj9-0.46.0.tar.gz';          ;;        s390x)          ESUM='8327736054aa9f1f1ccad4ef2aee4a4fa3362cc93930fe0d34ab79b2a2741d1a';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.0/ibm-semeru-open-jre_s390x_linux_17.0.12_7_openj9-0.46.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jul 2024 15:19:40 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 17 Jul 2024 15:19:40 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
USER root
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_VERSION=24.0.0.8-beta
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_BUILD_LABEL=cl240720240701-1102
# Wed, 17 Jul 2024 15:19:40 GMT
ARG OPENJ9_SCC=true
# Wed, 17 Jul 2024 15:19:40 GMT
ARG VERBOSE=false
# Wed, 17 Jul 2024 15:19:40 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240720240701-1102 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=24.0.0.8-beta
# Wed, 17 Jul 2024 15:19:40 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 17 Jul 2024 15:19:40 GMT
USER 1001
# Wed, 17 Jul 2024 15:19:40 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 17 Jul 2024 15:19:40 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 17 Jul 2024 15:19:40 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346f6b0caf9e82f11ff311008151b002cbef7156dabe22bc30c0b0bfab72dcb3`  
		Last Modified: Mon, 12 Aug 2024 18:04:26 GMT  
		Size: 12.9 MB (12888358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822e174788f1def77f988e9732a9ea0183cdf0605a7bdf9524738e0f71626895`  
		Last Modified: Mon, 12 Aug 2024 18:20:01 GMT  
		Size: 53.1 MB (53115578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:285eb429d17c96752d60b629a66d7402153c728d80cfed488359a3468c74bc35`  
		Last Modified: Mon, 12 Aug 2024 18:20:00 GMT  
		Size: 3.8 MB (3797082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47897e9d18b2f0d34b1d046e81d723f9d7869d322d166a3889ef8d3b3b9a2afb`  
		Last Modified: Mon, 12 Aug 2024 22:00:53 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e4d980cbfe70c5367489b33d26bc7f11a147205535b232e6ca20d561dad8ba`  
		Last Modified: Mon, 12 Aug 2024 22:00:53 GMT  
		Size: 10.0 KB (9990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1596045058787105be9f72d4a544a125e10e8d9cc3469483bebb8191a89b4b8`  
		Last Modified: Mon, 12 Aug 2024 22:00:54 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc57a2a4f03ea46a863b2529a6667c8e4d043aeb1b73b01ecb881526e29afde8`  
		Last Modified: Mon, 12 Aug 2024 22:00:54 GMT  
		Size: 36.5 KB (36497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f600dbcffa0cc6879ac7fcef0c3ce4efcf89daee3758d097b2ab3749e3cd4400`  
		Last Modified: Mon, 12 Aug 2024 22:01:18 GMT  
		Size: 358.5 MB (358519960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dc1c3b65f6a9a565b2015f5105e070270319896531c75522aaa096e625de20`  
		Last Modified: Mon, 12 Aug 2024 22:00:54 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781f59f30fa73c8e96c34a70b647ed2edd0ebc8b7989961aea73cb0fa4f57802`  
		Last Modified: Mon, 12 Aug 2024 22:00:55 GMT  
		Size: 11.3 KB (11346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949bce78e52d7e17780ef04c62491510ee5fcc04082513ad9d4c307ea8a27eff`  
		Last Modified: Mon, 12 Aug 2024 22:00:56 GMT  
		Size: 11.9 MB (11871315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java17` - unknown; unknown

```console
$ docker pull open-liberty@sha256:4a8d748cbd98860eaffc16b36f5c506db4ef86702955bc00575f0831120b5037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5448258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c6ade5a6d0a0c08c50fdd51888744490e294521cda1ead1f2392f77e3764512`

```dockerfile
```

-	Layers:
	-	`sha256:5bb8cf77ec7b7d727edcc1fc1ee4fbe9943ea555f0b59945d0e6986e1ea9b1ad`  
		Last Modified: Mon, 12 Aug 2024 22:00:54 GMT  
		Size: 5.4 MB (5409563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6834a2a8ec5b3372eb9ad70a90e3ba51138c9db1c307da500894636e031b292`  
		Last Modified: Mon, 12 Aug 2024 22:00:53 GMT  
		Size: 38.7 KB (38695 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta-java17` - linux; s390x

```console
$ docker pull open-liberty@sha256:a8cd413a6af0e0a69243b5ecb48b495d4a9da5030b48c7262b9781e26e753d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **468.2 MB (468152022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887b6b22c6d642bbc5b3a340156b09afe6ce83df0c967b614f7102eb2408ea9e`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 27 Jun 2024 19:26:47 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:26:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:26:50 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Thu, 27 Jun 2024 19:26:50 GMT
CMD ["/bin/bash"]
# Wed, 17 Jul 2024 15:19:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jul 2024 15:19:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV JAVA_VERSION=jdk-17.0.12+7_openj9-0.46.0
# Wed, 17 Jul 2024 15:19:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='c0e0ccad2ceb4e35321fcf7871571c1bc3ccaf98a41b7e15c530ea510fe646e3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.0/ibm-semeru-open-jre_aarch64_linux_17.0.12_7_openj9-0.46.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='ff35f2abcd84ac92f59aa501cd546399d1be97eca3404d263c13fa6c2272c34d';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.0/ibm-semeru-open-jre_ppc64le_linux_17.0.12_7_openj9-0.46.0.tar.gz';          ;;        amd64|x86_64)          ESUM='8227ff054505167ca7f379ad0ec618614ba72ab90fb4bf8f90b7db87d2f122f7';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.0/ibm-semeru-open-jre_x64_linux_17.0.12_7_openj9-0.46.0.tar.gz';          ;;        s390x)          ESUM='8327736054aa9f1f1ccad4ef2aee4a4fa3362cc93930fe0d34ab79b2a2741d1a';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.0/ibm-semeru-open-jre_s390x_linux_17.0.12_7_openj9-0.46.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jul 2024 15:19:40 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 17 Jul 2024 15:19:40 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
USER root
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_VERSION=24.0.0.8-beta
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip
# Wed, 17 Jul 2024 15:19:40 GMT
ARG LIBERTY_BUILD_LABEL=cl240720240701-1102
# Wed, 17 Jul 2024 15:19:40 GMT
ARG OPENJ9_SCC=true
# Wed, 17 Jul 2024 15:19:40 GMT
ARG VERBOSE=false
# Wed, 17 Jul 2024 15:19:40 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240720240701-1102 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=24.0.0.8-beta
# Wed, 17 Jul 2024 15:19:40 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
# ARGS: LIBERTY_VERSION=24.0.0.8-beta LIBERTY_SHA=b3f82c191e1dcbe8a64fe7395b6b25dcc0943869 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.8-beta/openliberty-runtime-24.0.0.8-beta.zip LIBERTY_BUILD_LABEL=cl240720240701-1102 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 17 Jul 2024 15:19:40 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 17 Jul 2024 15:19:40 GMT
USER 1001
# Wed, 17 Jul 2024 15:19:40 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 17 Jul 2024 15:19:40 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 17 Jul 2024 15:19:40 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:bc95fae2023d2ac4f35628ab3a262084bf2801462adfa6e7304b2b4e70ff4ab1`  
		Last Modified: Thu, 27 Jun 2024 20:18:52 GMT  
		Size: 28.0 MB (28000540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928fcb5dd7fd89cdaf703469776b84f22f2a0896c6669206b1c3e5fd07dd7ccf`  
		Last Modified: Mon, 12 Aug 2024 18:02:49 GMT  
		Size: 12.2 MB (12203937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac1245bb6d0f7b0ff13542d0de9a3be5a415e9315b5a8c061e07439a6d40149`  
		Last Modified: Mon, 12 Aug 2024 18:18:19 GMT  
		Size: 50.5 MB (50470197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0d11c8341f155083fa380f7c88751722560b1a1321ed84f5ae610f032d4472`  
		Last Modified: Mon, 12 Aug 2024 18:18:18 GMT  
		Size: 5.1 MB (5057019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcf1774591bcaf42ef8cc32765ad2448c02c076a3caf3ccbea2c33cd28801b9`  
		Last Modified: Mon, 12 Aug 2024 18:59:21 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11eaadf74b047591f43a56e6bbd0ee7ae575aacbe2cc27ced386ace59bc12b18`  
		Last Modified: Mon, 12 Aug 2024 18:59:21 GMT  
		Size: 10.0 KB (9987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491c52a4ad21bc21adee99b3f9c34dc9636781c2c25424e754c5f58f25c2b545`  
		Last Modified: Mon, 12 Aug 2024 18:59:21 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c90cbdcb2d8d46f8bc5cad2c313cf48882ad579d18e486f4e3e32af24cc77b3`  
		Last Modified: Mon, 12 Aug 2024 18:59:22 GMT  
		Size: 33.1 KB (33113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88bbdb11cd6e00bf3dadcbd972741a7d2940d25ada1d80a3206db731b25bc053`  
		Last Modified: Mon, 12 Aug 2024 18:59:28 GMT  
		Size: 358.5 MB (358519530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb64436e766faeb10934e945d59670d066f0f8779a7371683c73fa189d68e1d`  
		Last Modified: Mon, 12 Aug 2024 18:59:22 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1f2d314f312ddcaf86c03d7b9dce8aa47ee4abb7ccf537479a84fc032059a4`  
		Last Modified: Mon, 12 Aug 2024 18:59:22 GMT  
		Size: 11.3 KB (11342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6cd241ccf327450c44cc50d576a1cb81004ad71ff2288942baee358cc5026f`  
		Last Modified: Mon, 12 Aug 2024 18:59:25 GMT  
		Size: 13.8 MB (13844012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java17` - unknown; unknown

```console
$ docker pull open-liberty@sha256:37bf3dd2ae4e232a689defcb225708cfbb1508ddd655ddca2283b33cd701fbe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5443781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc09aab0d916aa47be504a7a9daf32079a38428c364e98a55b3ba6fbc94f7669`

```dockerfile
```

-	Layers:
	-	`sha256:0304859f8846d0ed17f25a243faeee676780e254b87f82eed4d9de5fe8ac2b31`  
		Last Modified: Mon, 12 Aug 2024 18:59:21 GMT  
		Size: 5.4 MB (5405120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4682df7a1e9a181464808366b7ffb13d091b0f273a4a1e42c35940e1f7e156e`  
		Last Modified: Mon, 12 Aug 2024 18:59:21 GMT  
		Size: 38.7 KB (38661 bytes)  
		MIME: application/vnd.in-toto+json
