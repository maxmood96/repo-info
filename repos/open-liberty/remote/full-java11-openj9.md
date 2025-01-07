## `open-liberty:full-java11-openj9`

```console
$ docker pull open-liberty@sha256:c24a78c936bd0a7c82716f2918569e7be551ae47295f6a10d39b1d66fd2b9941
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
$ docker pull open-liberty@sha256:9668059524769e0b11fbb1615b579f35c731e8d68ab585190185022985ba8465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.2 MB (450204210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b958fb9c4659721756f015537b2f1065fcf25ca54b4c5bfac03ea0c80433d8d3`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Tue, 03 Dec 2024 20:41:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 03 Dec 2024 20:41:16 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
ENV JAVA_VERSION=jdk-11.0.25+9_openj9-0.48.0
# Tue, 03 Dec 2024 20:41:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3ebe7dc3fc6d7a0145d8834d01ca5adda19c1812af9a4f63655bc4de463377b6';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_aarch64_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='451c6da5d286af654d857c2383698c19e9f05070b8e018f73f82ab1df1c51ba3';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_ppc64le_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7d8407bbc68303e84615d1981abbdda690236edfcff5535789dc7915a3c4f629';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_x64_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='28c3adeefd79d0054cd8f5b5de0a95277ae19a53e1f503a15d4955c38a9e715d';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_s390x_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 20:41:16 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 03 Dec 2024 20:41:16 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.98/bin/apache-tomcat-9.0.98.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
USER root
# Tue, 03 Dec 2024 20:41:16 GMT
ARG LIBERTY_VERSION=24.0.0.12
# Tue, 03 Dec 2024 20:41:16 GMT
ARG LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554
# Tue, 03 Dec 2024 20:41:16 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip
# Tue, 03 Dec 2024 20:41:16 GMT
ARG LIBERTY_BUILD_LABEL=cl241220241119-0657
# Tue, 03 Dec 2024 20:41:16 GMT
ARG OPENJ9_SCC=true
# Tue, 03 Dec 2024 20:41:16 GMT
ARG VERBOSE=false
# Tue, 03 Dec 2024 20:41:16 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl241220241119-0657 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=24.0.0.12
# Tue, 03 Dec 2024 20:41:16 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 03 Dec 2024 20:41:16 GMT
USER 1001
# Tue, 03 Dec 2024 20:41:16 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 03 Dec 2024 20:41:16 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 03 Dec 2024 20:41:16 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8525614b4e6de0b0e55d400320432c437503e7c7b0d9f29a5d1b4da03c50866c`  
		Last Modified: Thu, 19 Dec 2024 21:31:39 GMT  
		Size: 12.2 MB (12174488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae4eff47a9d9c0ea60c86c156120fb097de0ed587ea389cf132d302cb46571c`  
		Last Modified: Thu, 19 Dec 2024 21:31:40 GMT  
		Size: 52.3 MB (52287794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706058aad73b2780c0e6706405562bb940ec0783b94b5443e466ead7e2c56f6e`  
		Last Modified: Thu, 19 Dec 2024 21:31:39 GMT  
		Size: 4.4 MB (4449965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcdb77040f48739de620a5bb24f737392008c17b5b0c3a7fb9018812b999437b`  
		Last Modified: Thu, 19 Dec 2024 22:17:04 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb408114ad56669d7f088452c184f063eb14405e0b9be3c059b687effda6599`  
		Last Modified: Thu, 19 Dec 2024 22:17:04 GMT  
		Size: 10.0 KB (9985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef4f43e4060311f43702ceec34cc80aa8f45eaa3005f5ff75cd08b4b7fca887`  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b170cf691345a6f77c2ce896b794741e07069ce81ecf792c6e20d4130b4810`  
		Last Modified: Thu, 19 Dec 2024 22:17:04 GMT  
		Size: 31.8 KB (31750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91be14a12c9f5c765dbb248dd736fbaf451fa9861518569d104fa71aa5e0393`  
		Last Modified: Thu, 19 Dec 2024 22:17:09 GMT  
		Size: 337.9 MB (337911911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44b70d64d6b832efcf36122258e2549a85dc97a026e2b3a22c87fb5acd3108b`  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcfbd8a966449d70caff394e59c924610bfe8b17354340a27f2a81c2e7118b4`  
		Last Modified: Thu, 19 Dec 2024 22:17:05 GMT  
		Size: 11.3 KB (11336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05ca27cc62cb6d497c7f170ce769c79176317c7632cfdd37b44df0af50a4a81`  
		Last Modified: Thu, 19 Dec 2024 22:17:06 GMT  
		Size: 13.8 MB (13788944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:030f797fe34629e52e5f556c03e93c6fbf5dd64764f1a7456ed91a383886f4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5560666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9985f21a62eff361e4ef090da8d2fe1c0656f946d465506c7f0066cdc5f99bf8`

```dockerfile
```

-	Layers:
	-	`sha256:ee419d1e1b5892676308c2ae7297625c95b1fe2b447775461d6798a124eb477f`  
		Last Modified: Thu, 19 Dec 2024 22:17:04 GMT  
		Size: 5.5 MB (5522079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c094ca0d0d6cb94daa58bbd444671c7e2be1602370a1bd6d8bf7b529c1cb2b3c`  
		Last Modified: Thu, 19 Dec 2024 22:17:04 GMT  
		Size: 38.6 KB (38587 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java11-openj9` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:733317a32e8ca860e22d5539162a0162ef2d36fd75be364d4f35203c4130ed01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **443.2 MB (443184699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3c8745f283b5be5f7f5341413e49f5473cc04564f807ac200c9d717208f0f3`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Tue, 03 Dec 2024 20:41:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 03 Dec 2024 20:41:16 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
ENV JAVA_VERSION=jdk-11.0.25+9_openj9-0.48.0
# Tue, 03 Dec 2024 20:41:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3ebe7dc3fc6d7a0145d8834d01ca5adda19c1812af9a4f63655bc4de463377b6';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_aarch64_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='451c6da5d286af654d857c2383698c19e9f05070b8e018f73f82ab1df1c51ba3';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_ppc64le_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7d8407bbc68303e84615d1981abbdda690236edfcff5535789dc7915a3c4f629';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_x64_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='28c3adeefd79d0054cd8f5b5de0a95277ae19a53e1f503a15d4955c38a9e715d';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_s390x_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 20:41:16 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 03 Dec 2024 20:41:16 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.98/bin/apache-tomcat-9.0.98.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
USER root
# Tue, 03 Dec 2024 20:41:16 GMT
ARG LIBERTY_VERSION=24.0.0.12
# Tue, 03 Dec 2024 20:41:16 GMT
ARG LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554
# Tue, 03 Dec 2024 20:41:16 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip
# Tue, 03 Dec 2024 20:41:16 GMT
ARG LIBERTY_BUILD_LABEL=cl241220241119-0657
# Tue, 03 Dec 2024 20:41:16 GMT
ARG OPENJ9_SCC=true
# Tue, 03 Dec 2024 20:41:16 GMT
ARG VERBOSE=false
# Tue, 03 Dec 2024 20:41:16 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl241220241119-0657 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=24.0.0.12
# Tue, 03 Dec 2024 20:41:16 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 03 Dec 2024 20:41:16 GMT
USER 1001
# Tue, 03 Dec 2024 20:41:16 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 03 Dec 2024 20:41:16 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 03 Dec 2024 20:41:16 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e2579fa9ed432452dd8563d1dc040de22c49fcfc4a3cd906b5e75b095c2926`  
		Last Modified: Mon, 18 Nov 2024 19:12:40 GMT  
		Size: 12.1 MB (12128239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585691ad625e93cdddb0de99cf13a7826edb732382b03457d442db22dbbbd259`  
		Last Modified: Thu, 19 Dec 2024 22:22:04 GMT  
		Size: 48.4 MB (48398557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5894bf3e7230fd983d9c16ddb6cf31be223eeae53e42d04535c280bafed85fa7`  
		Size: 4.2 MB (4169154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80d77dd0735efef66141890e6c63c04a5888c85d6e2830d9a6262eda426c34e`  
		Last Modified: Thu, 19 Dec 2024 23:11:30 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddad240b8d35185173f8512fde26c1935d921990d24480cd852f72e1308fcdc1`  
		Last Modified: Thu, 19 Dec 2024 23:11:30 GMT  
		Size: 10.0 KB (9982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d33cd8f2d07c8b839219dfdfd545004fad0623c81ea4f3fa348dcf59d6d057`  
		Last Modified: Thu, 19 Dec 2024 23:11:30 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b2e920a55c8082912d73c92f7a679393094afddd3e9a5750cd6cc33eef02b2`  
		Last Modified: Thu, 19 Dec 2024 23:16:33 GMT  
		Size: 42.3 KB (42326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccfdadaf7a7e3ef786526e78d7676c0a13a35338fa38a45dfaa1a2b4959665b`  
		Last Modified: Thu, 19 Dec 2024 23:16:40 GMT  
		Size: 337.9 MB (337912216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefea425974817ce7766e0e28b28046d810ab835a2625e069c02a83b219069f6`  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75464c5c5a30e12456d1f643265f6517b78ebbc63ac2bca52f763d9f244d281b`  
		Last Modified: Thu, 19 Dec 2024 23:16:34 GMT  
		Size: 11.3 KB (11346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56baf7556d387c5ea1af38747f8cc0253a13dc43643bab38badb3170813efd9a`  
		Last Modified: Thu, 19 Dec 2024 23:16:35 GMT  
		Size: 13.2 MB (13152205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:a72b1a5d118de9ed945400370ae1e5a012d040c62eb6e57cecd09a9df666c660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5552275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e588768f7f35a73c7fb09d907f0d9528d5cc2c0c71df6ab94cac86dd43b95051`

```dockerfile
```

-	Layers:
	-	`sha256:652fa1c05c7ef874b30de23cbd2e1b4f34e968fa970f9e8bab1d8c226aee0e4d`  
		Size: 5.5 MB (5513559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5069392c5a5da5a7dcefe82de656240697b667cf786bdf6d1e7b6af8506ab322`  
		Last Modified: Thu, 19 Dec 2024 23:16:33 GMT  
		Size: 38.7 KB (38716 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java11-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:d1165dc538fda9a522829fcd4acbe159323591a71b634ca4981b291d2a176cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.2 MB (454219115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91bd38bdebed5aeaff2e3b331d6e6af264db2538467d92e09e4e1f96f1d6a801`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Tue, 03 Dec 2024 20:41:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 03 Dec 2024 20:41:16 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
ENV JAVA_VERSION=jdk-11.0.25+9_openj9-0.48.0
# Tue, 03 Dec 2024 20:41:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3ebe7dc3fc6d7a0145d8834d01ca5adda19c1812af9a4f63655bc4de463377b6';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_aarch64_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='451c6da5d286af654d857c2383698c19e9f05070b8e018f73f82ab1df1c51ba3';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_ppc64le_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7d8407bbc68303e84615d1981abbdda690236edfcff5535789dc7915a3c4f629';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_x64_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='28c3adeefd79d0054cd8f5b5de0a95277ae19a53e1f503a15d4955c38a9e715d';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_s390x_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 20:41:16 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 03 Dec 2024 20:41:16 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.98/bin/apache-tomcat-9.0.98.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
USER root
# Tue, 03 Dec 2024 20:41:16 GMT
ARG LIBERTY_VERSION=24.0.0.12
# Tue, 03 Dec 2024 20:41:16 GMT
ARG LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554
# Tue, 03 Dec 2024 20:41:16 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip
# Tue, 03 Dec 2024 20:41:16 GMT
ARG LIBERTY_BUILD_LABEL=cl241220241119-0657
# Tue, 03 Dec 2024 20:41:16 GMT
ARG OPENJ9_SCC=true
# Tue, 03 Dec 2024 20:41:16 GMT
ARG VERBOSE=false
# Tue, 03 Dec 2024 20:41:16 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl241220241119-0657 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=24.0.0.12
# Tue, 03 Dec 2024 20:41:16 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 03 Dec 2024 20:41:16 GMT
USER 1001
# Tue, 03 Dec 2024 20:41:16 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 03 Dec 2024 20:41:16 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 03 Dec 2024 20:41:16 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6230a31e14b4a918b32fc7a3b685fad8ecafe0901deee916736d3e6f4db6ad`  
		Last Modified: Tue, 17 Sep 2024 01:15:01 GMT  
		Size: 12.9 MB (12888132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d41fa978cf87aac305b049cd5de5554c77f72fc25bf28d474d5b025207bcb9d`  
		Last Modified: Mon, 18 Nov 2024 19:17:51 GMT  
		Size: 53.6 MB (53595890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f276d8c24867d9b1f6bbc4d270b8a81c3c24e5dc700408c990fd1c3ae1246f`  
		Size: 3.4 MB (3424091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a2ce4946e70ea749e081390feb6010127c56314c273799e798162449a591e2`  
		Last Modified: Thu, 19 Dec 2024 23:10:24 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5112d24a33aa7bb2d98cd8b388dfb23fa82502395f65e50c705f6112d23795`  
		Last Modified: Thu, 19 Dec 2024 23:10:24 GMT  
		Size: 10.0 KB (9984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08da1b781f8061587034d446344c88c26f76faf3a08f3bf6bbc12953d398e288`  
		Last Modified: Thu, 19 Dec 2024 23:10:24 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c95a9f27f0667527413dc0ec260581792e38012b8cd6449d5a022666075257c`  
		Last Modified: Thu, 19 Dec 2024 23:21:45 GMT  
		Size: 36.5 KB (36499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f58d0c3e32a473eab3addd1d4b29a44af94d1fb7a0157a2cad32f0ca1a048f`  
		Last Modified: Thu, 19 Dec 2024 23:22:10 GMT  
		Size: 337.9 MB (337912808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6806b2a28d07aeb71428b4687e858778943dea3576f46ef1fddde58dce6f4d`  
		Last Modified: Thu, 19 Dec 2024 23:21:45 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c0ab8d99fc2e37b92265971e7c6838ffad657e04cabe7009b416bd548700b3`  
		Last Modified: Thu, 19 Dec 2024 23:21:45 GMT  
		Size: 11.3 KB (11348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9e7b6adc9cd179a602c6ea6b4add19906e9e37478da6a909d2618fade13182`  
		Last Modified: Thu, 19 Dec 2024 23:21:47 GMT  
		Size: 11.9 MB (11889776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:53ceb6934bc3a9d88346e66c74331bdf1660b15972b8c009b6842410e4e3874e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5557449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8461347bba28e2c4ba36d529bd6790a535e512503f42432e6f94e70e83c22d54`

```dockerfile
```

-	Layers:
	-	`sha256:69c156cf7e7a10452405e44155bdaa91c59dd5cc99d63c5c719c061e81163938`  
		Last Modified: Thu, 19 Dec 2024 23:21:45 GMT  
		Size: 5.5 MB (5518827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07036e00f7655789a2066c7ef8ad58d7399b1c4e9626fc7cab73882ea5a6052b`  
		Last Modified: Thu, 19 Dec 2024 23:21:45 GMT  
		Size: 38.6 KB (38622 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java11-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:046138886e13d25dc0c0ec2d41bdfd9cc31b3b85bfe1f3ff63cd2ab7d31d7a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.2 MB (447236401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:876e5c8aad2040bb9fc5271741935fe525cc0771a126dffad21429615ea0100d`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:31 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:32 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 11 Sep 2024 16:25:32 GMT
CMD ["/bin/bash"]
# Tue, 03 Dec 2024 20:41:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 03 Dec 2024 20:41:16 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
ENV JAVA_VERSION=jdk-11.0.25+9_openj9-0.48.0
# Tue, 03 Dec 2024 20:41:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3ebe7dc3fc6d7a0145d8834d01ca5adda19c1812af9a4f63655bc4de463377b6';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_aarch64_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='451c6da5d286af654d857c2383698c19e9f05070b8e018f73f82ab1df1c51ba3';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_ppc64le_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7d8407bbc68303e84615d1981abbdda690236edfcff5535789dc7915a3c4f629';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_x64_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='28c3adeefd79d0054cd8f5b5de0a95277ae19a53e1f503a15d4955c38a9e715d';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_s390x_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 20:41:16 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 03 Dec 2024 20:41:16 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.98/bin/apache-tomcat-9.0.98.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
USER root
# Tue, 03 Dec 2024 20:41:16 GMT
ARG LIBERTY_VERSION=24.0.0.12
# Tue, 03 Dec 2024 20:41:16 GMT
ARG LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554
# Tue, 03 Dec 2024 20:41:16 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip
# Tue, 03 Dec 2024 20:41:16 GMT
ARG LIBERTY_BUILD_LABEL=cl241220241119-0657
# Tue, 03 Dec 2024 20:41:16 GMT
ARG OPENJ9_SCC=true
# Tue, 03 Dec 2024 20:41:16 GMT
ARG VERBOSE=false
# Tue, 03 Dec 2024 20:41:16 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl241220241119-0657 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=24.0.0.12
# Tue, 03 Dec 2024 20:41:16 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12 LIBERTY_SHA=c98874d1c28a5814c99573563f944cacbd6dd554 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.12/openliberty-runtime-24.0.0.12.zip LIBERTY_BUILD_LABEL=cl241220241119-0657 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 03 Dec 2024 20:41:16 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 03 Dec 2024 20:41:16 GMT
USER 1001
# Tue, 03 Dec 2024 20:41:16 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 03 Dec 2024 20:41:16 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 03 Dec 2024 20:41:16 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d7fcbb74a18dbda1a95a881c01c2cc4d8a0d6fe38b3b4f8b5899f281f9815e`  
		Last Modified: Tue, 17 Sep 2024 01:57:02 GMT  
		Size: 12.2 MB (12203759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f548077faffbeb9ab09f574ebae67e13d3317200cd3613df609effae4b92c77`  
		Last Modified: Thu, 19 Dec 2024 21:49:19 GMT  
		Size: 50.9 MB (50865429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ddec57d686772b9ae7f80d1d520170f90bcdf89ece83b87fb6201872b5286d1`  
		Last Modified: Thu, 19 Dec 2024 21:49:18 GMT  
		Size: 4.6 MB (4555256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53bd6591b6faaf33732aad8cd9e10163c5a137d6f080aba9ed0c8d6323a9509d`  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081abeb906a039fbd4b91e47ef25b09cc4efd294b5c6fedb3adfe013ff236c6e`  
		Last Modified: Thu, 19 Dec 2024 22:45:34 GMT  
		Size: 10.0 KB (9987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d160aa519e23bf7472354191021b2b60888e52db9d5654476bc7c9249851a0`  
		Last Modified: Thu, 19 Dec 2024 22:45:34 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a20d04f8215b61ae35578e9fd8807807468d072dd01a249cbf68b0e6f14c7e`  
		Last Modified: Thu, 19 Dec 2024 22:57:43 GMT  
		Size: 33.1 KB (33113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72d03250eb6ea9734bc4106d54963f04ab97dba17e1bade4e2bbce5a51363ca`  
		Last Modified: Thu, 19 Dec 2024 22:57:47 GMT  
		Size: 337.9 MB (337912473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f422ee00b9012fc93f44aa0663664376b703c5b95d58d07a1c9a4c2b9d7d72e`  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3f5d93c48a75e7a83b14902781d69bb300232126aa15cff510487016e6595b`  
		Size: 11.3 KB (11346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3205ac3a810ff515e83504a4260c575a89b268729f949c9d617e2028e41765c`  
		Last Modified: Thu, 19 Dec 2024 22:57:45 GMT  
		Size: 13.6 MB (13641208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:1f60ddb10721168e198ae852c66895be99dd01f60bf13027f3636644270ad54f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5553949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d1616b9c40f9808804b20b6ef6ac873cb665b7fd5feebb6244f0478e2e3ccaf`

```dockerfile
```

-	Layers:
	-	`sha256:89679afcd05d136b3942ebffc92bf25e24e4405271e1bdb79adbfda05a2bedac`  
		Last Modified: Thu, 19 Dec 2024 22:57:43 GMT  
		Size: 5.5 MB (5515361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f730ede27c71eafd87bc87e5e7e4aa820981ce8b8c47bb93aae393895d792997`  
		Last Modified: Thu, 19 Dec 2024 22:57:43 GMT  
		Size: 38.6 KB (38588 bytes)  
		MIME: application/vnd.in-toto+json
