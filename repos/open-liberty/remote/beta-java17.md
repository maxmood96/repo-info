## `open-liberty:beta-java17`

```console
$ docker pull open-liberty@sha256:e81da1e4bbe3c6a626eacb537137a5f4edbf7e1274edfd3d58f3b04f4cca26d4
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
$ docker pull open-liberty@sha256:0e96b27a5ce5d0556bd6824afd9e7cf89924172eedfdc32a61013c7f1fdf0ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.7 MB (489665972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bdd59dbfa7ad8b79de0f7487d38a2f622f83d1b1c470a36f021ea4a9477af92`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:46:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:46:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:46:10 GMT
ENV JAVA_VERSION=17.0.19.0
# Thu, 30 Apr 2026 23:46:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3ce5bd7829e198408dd3e27825f096f79d19438ac1e96bc583a32d9580f1d3a6';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_aarch64_linux_17.0.19.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='2dc4cfb4256642cfbea7fbe0edc30e79f995e7f1e01408876b88517b52cae4ad';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_ppc64le_linux_17.0.19.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b40a28e68e84461607a5d802fe6ddb7376e4a3d8e477b32bbe5c1cdf5638a7ed';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_x64_linux_17.0.19.0.tar.gz';          ;;        s390x)          ESUM='a9abce59480d62967ffe4a6c4b176a3e22bbef7e9ec9dd4cb58d23d5881f4d58';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_s390x_linux_17.0.19.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Apr 2026 23:46:12 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:46:12 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Apr 2026 23:47:15 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54";     TOMCAT_VERSION="9.0.117";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 29 May 2026 23:04:30 GMT
USER root
# Fri, 29 May 2026 23:04:30 GMT
ARG LIBERTY_VERSION=26.0.0.6-beta
# Fri, 29 May 2026 23:04:30 GMT
ARG LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52
# Fri, 29 May 2026 23:04:30 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip
# Fri, 29 May 2026 23:04:30 GMT
ARG LIBERTY_BUILD_LABEL=cl260520260430-1602
# Fri, 29 May 2026 23:04:30 GMT
ARG OPENJ9_SCC=true
# Fri, 29 May 2026 23:04:30 GMT
ARG VERBOSE=false
# Fri, 29 May 2026 23:04:30 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260520260430-1602 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=26.0.0.6-beta liberty.version=26.0.0.6-beta io.openliberty.version=26.0.0.6-beta
# Fri, 29 May 2026 23:04:30 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Fri, 29 May 2026 23:04:30 GMT
COPY helpers /opt/ol/helpers # buildkit
# Fri, 29 May 2026 23:04:30 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Fri, 29 May 2026 23:04:30 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 29 May 2026 23:04:42 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Fri, 29 May 2026 23:04:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 29 May 2026 23:04:43 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 29 May 2026 23:04:43 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 29 May 2026 23:05:05 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Fri, 29 May 2026 23:05:05 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 29 May 2026 23:05:05 GMT
USER 1001
# Fri, 29 May 2026 23:05:05 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 29 May 2026 23:05:05 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 29 May 2026 23:05:05 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cd737a8b9091e9a2bcd6d0afc1e4c62a0f2c266c8566bc302804b9c46de824`  
		Last Modified: Thu, 30 Apr 2026 23:47:27 GMT  
		Size: 12.8 MB (12805392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61a0132dbaf5c7b1e692be574dafc2896e1e40a6f082923cfc06208aed92d15`  
		Last Modified: Thu, 30 Apr 2026 23:47:28 GMT  
		Size: 56.1 MB (56093691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb25686fef712ae235cec141ed46c4ba20ec8f2d118c3a936bcb1c531472734`  
		Last Modified: Thu, 30 Apr 2026 23:47:27 GMT  
		Size: 5.0 MB (5007826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b40d4bd5b6e22ee48abecae3b3d0d3d5f4307603709e6b311b3c5b31e395ce7`  
		Last Modified: Fri, 29 May 2026 23:05:29 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755ab4b0d3a47f2f3de5b1777e94308e0ea76349e49be12fdc1a33827db58719`  
		Last Modified: Fri, 29 May 2026 23:05:29 GMT  
		Size: 12.8 KB (12773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefed9faab58e973853d80c51a02e32a299e1827077c971a95124e88e76aafe4`  
		Last Modified: Fri, 29 May 2026 23:05:29 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846dd971328db4d14b469b020ea91fd7a834eece950ffab00f68085841eab602`  
		Last Modified: Fri, 29 May 2026 23:05:29 GMT  
		Size: 31.8 KB (31750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a3085e1434f0b20edfa3c712ac849a766d1334d4243134ffe4324f748f93b9`  
		Last Modified: Fri, 29 May 2026 23:05:38 GMT  
		Size: 371.4 MB (371400216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b86aa2b67d77dfdd50f6bb5eda9384d399b07b07257b974a1643a322cb2567a`  
		Last Modified: Fri, 29 May 2026 23:05:30 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37feae4cad5cd519a64291b59944be0283e9ec7ee6fb578f1729b4edecefddd1`  
		Last Modified: Fri, 29 May 2026 23:05:30 GMT  
		Size: 14.2 KB (14213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f32a43a810dfd14b2d30f8dc4db94efd1eaa08e0eead17c760ef891c75c308`  
		Last Modified: Fri, 29 May 2026 23:05:31 GMT  
		Size: 14.6 MB (14564787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java17` - unknown; unknown

```console
$ docker pull open-liberty@sha256:c3e80ea522616e06b8f619375745a60eb6adb3cabbd03ca5bb2ad843351d3166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5253614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce146966627e0a5579bec2e5f8f796e3a802eed5d04104dbd3727a24e38d15f`

```dockerfile
```

-	Layers:
	-	`sha256:676b1deaf386d25299c49e43fb849911611d972bef34013d2ab1df10b337cbc1`  
		Last Modified: Fri, 29 May 2026 23:05:29 GMT  
		Size: 5.2 MB (5214237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3c871648bdfa9cabfef15bea1ff60bbe4e896a1695a8496322b7f6cddbf1fdc`  
		Last Modified: Fri, 29 May 2026 23:05:29 GMT  
		Size: 39.4 KB (39377 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta-java17` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:5b44284b3245852caea6ebdf442c5a521972134e5eb37c66351ae06172e5bdae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.3 MB (486256596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081bfd14d04aa0ebecfb38c1704bc0b5f180ef18488e23090335d816e2897254`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:46:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:46:28 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:46:28 GMT
ENV JAVA_VERSION=17.0.19.0
# Thu, 30 Apr 2026 23:46:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3ce5bd7829e198408dd3e27825f096f79d19438ac1e96bc583a32d9580f1d3a6';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_aarch64_linux_17.0.19.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='2dc4cfb4256642cfbea7fbe0edc30e79f995e7f1e01408876b88517b52cae4ad';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_ppc64le_linux_17.0.19.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b40a28e68e84461607a5d802fe6ddb7376e4a3d8e477b32bbe5c1cdf5638a7ed';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_x64_linux_17.0.19.0.tar.gz';          ;;        s390x)          ESUM='a9abce59480d62967ffe4a6c4b176a3e22bbef7e9ec9dd4cb58d23d5881f4d58';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_s390x_linux_17.0.19.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Apr 2026 23:46:30 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:46:30 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Apr 2026 23:47:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54";     TOMCAT_VERSION="9.0.117";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 29 May 2026 23:04:07 GMT
USER root
# Fri, 29 May 2026 23:04:07 GMT
ARG LIBERTY_VERSION=26.0.0.6-beta
# Fri, 29 May 2026 23:04:07 GMT
ARG LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52
# Fri, 29 May 2026 23:04:07 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip
# Fri, 29 May 2026 23:04:07 GMT
ARG LIBERTY_BUILD_LABEL=cl260520260430-1602
# Fri, 29 May 2026 23:04:07 GMT
ARG OPENJ9_SCC=true
# Fri, 29 May 2026 23:04:07 GMT
ARG VERBOSE=false
# Fri, 29 May 2026 23:04:07 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260520260430-1602 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=26.0.0.6-beta liberty.version=26.0.0.6-beta io.openliberty.version=26.0.0.6-beta
# Fri, 29 May 2026 23:04:07 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Fri, 29 May 2026 23:04:07 GMT
COPY helpers /opt/ol/helpers # buildkit
# Fri, 29 May 2026 23:04:07 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Fri, 29 May 2026 23:04:08 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 29 May 2026 23:04:24 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Fri, 29 May 2026 23:04:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 29 May 2026 23:04:24 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 29 May 2026 23:04:24 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 29 May 2026 23:04:50 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Fri, 29 May 2026 23:04:50 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 29 May 2026 23:04:50 GMT
USER 1001
# Fri, 29 May 2026 23:04:50 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 29 May 2026 23:04:50 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 29 May 2026 23:04:50 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58682390813eb4e99e41d3b95e0549a0d76691a908f1899a748b1fe6152e74e2`  
		Last Modified: Thu, 30 Apr 2026 23:47:46 GMT  
		Size: 12.8 MB (12837805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a2eeae307beb04671a80776bebbd5db9864e5e0f572ad0325c4cd7ec0dd3ae`  
		Last Modified: Thu, 30 Apr 2026 23:47:47 GMT  
		Size: 54.0 MB (54002667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9bde1a0155156418897c9c3cce40d2e977a72ffd8afb2c2d01bec210a475b6`  
		Last Modified: Thu, 30 Apr 2026 23:47:46 GMT  
		Size: 4.8 MB (4778048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e6d941e6e280796a82cf5066e10500fbe23dca65990d1f58787a3e5002fcb0`  
		Last Modified: Fri, 29 May 2026 23:05:16 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c497c19b20f974050e8836f080bfde2fdcbc396bd166d2d0701b83d46e105ab`  
		Last Modified: Fri, 29 May 2026 23:05:17 GMT  
		Size: 12.8 KB (12777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a167473c96d7ef9e1f90d4b7fd6bbf8de4222aa7e45d19350a98354c259f8d3c`  
		Last Modified: Fri, 29 May 2026 23:05:17 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4910931203b3418510bb7dbdba109c8f51786da6bd03d7f9ad47cd45cd718f72`  
		Last Modified: Fri, 29 May 2026 23:05:17 GMT  
		Size: 42.3 KB (42325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31977b279d965d912bbe9eca103b58acc17730b81a174bd8ad2e298d5360322`  
		Last Modified: Fri, 29 May 2026 23:05:25 GMT  
		Size: 371.4 MB (371400354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed786d0cef947cfdc8130aa4f924d61b52fba4cf892e3658eb40ada94b2c6fb1`  
		Last Modified: Fri, 29 May 2026 23:05:18 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8d6c35a878a2f674cc36a67567a829dbf2b9a321666e97730328347395f3c6`  
		Last Modified: Fri, 29 May 2026 23:05:18 GMT  
		Size: 14.2 KB (14216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772743056623e7f80ccfc65e3595879bfb19757e2ea08160c6d9e7055a2df4c5`  
		Last Modified: Fri, 29 May 2026 23:05:18 GMT  
		Size: 14.3 MB (14290273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java17` - unknown; unknown

```console
$ docker pull open-liberty@sha256:b77bfe6cb0e4299be5af1391bd9bbde2601b7e9f3dd1d20769ff568ac846c3e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e43fc8e195f8e918dd499c21f3bd7fd477d6c7bf7adf8ea3c5bb9f873c06ba60`

```dockerfile
```

-	Layers:
	-	`sha256:ed1b2f248f1f37e95d9dcd0ce562da9d24d0e731844d04a8c3182a7fc374f24d`  
		Last Modified: Fri, 29 May 2026 23:05:17 GMT  
		Size: 5.2 MB (5212767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:546cc9dafa02b0355ea58b384b44a78ab8641923ec17d97494390ddd0b6a4ea9`  
		Last Modified: Fri, 29 May 2026 23:05:17 GMT  
		Size: 39.5 KB (39505 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta-java17` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:791764e5befc2bb26aa74faf40d0576aa4ac586339873ce073b3e831e1a2ec6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.5 MB (494463798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e6bf824ea3d6e6e563ebc1ee129284c3f1dfc9f6fe45f9bc367bb9f3b7fc684`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:39:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 21:39:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:39:02 GMT
ENV JAVA_VERSION=17.0.19.0
# Fri, 01 May 2026 04:55:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3ce5bd7829e198408dd3e27825f096f79d19438ac1e96bc583a32d9580f1d3a6';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_aarch64_linux_17.0.19.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='2dc4cfb4256642cfbea7fbe0edc30e79f995e7f1e01408876b88517b52cae4ad';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_ppc64le_linux_17.0.19.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b40a28e68e84461607a5d802fe6ddb7376e4a3d8e477b32bbe5c1cdf5638a7ed';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_x64_linux_17.0.19.0.tar.gz';          ;;        s390x)          ESUM='a9abce59480d62967ffe4a6c4b176a3e22bbef7e9ec9dd4cb58d23d5881f4d58';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_s390x_linux_17.0.19.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 May 2026 04:55:38 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 04:55:38 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 01 May 2026 04:56:47 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54";     TOMCAT_VERSION="9.0.117";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 29 May 2026 23:05:27 GMT
USER root
# Fri, 29 May 2026 23:05:27 GMT
ARG LIBERTY_VERSION=26.0.0.6-beta
# Fri, 29 May 2026 23:05:27 GMT
ARG LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52
# Fri, 29 May 2026 23:05:27 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip
# Fri, 29 May 2026 23:05:27 GMT
ARG LIBERTY_BUILD_LABEL=cl260520260430-1602
# Fri, 29 May 2026 23:05:27 GMT
ARG OPENJ9_SCC=true
# Fri, 29 May 2026 23:05:27 GMT
ARG VERBOSE=false
# Fri, 29 May 2026 23:05:27 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260520260430-1602 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=26.0.0.6-beta liberty.version=26.0.0.6-beta io.openliberty.version=26.0.0.6-beta
# Fri, 29 May 2026 23:05:27 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Fri, 29 May 2026 23:05:28 GMT
COPY helpers /opt/ol/helpers # buildkit
# Fri, 29 May 2026 23:05:28 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Fri, 29 May 2026 23:05:29 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 29 May 2026 23:05:48 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Fri, 29 May 2026 23:05:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 29 May 2026 23:05:49 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 29 May 2026 23:05:50 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 29 May 2026 23:06:33 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Fri, 29 May 2026 23:06:33 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 29 May 2026 23:06:33 GMT
USER 1001
# Fri, 29 May 2026 23:06:33 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 29 May 2026 23:06:33 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 29 May 2026 23:06:33 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccf3833ba70e5f487e107c0fc757f71c24195588839e7b794b482f819b1bf2d`  
		Last Modified: Wed, 15 Apr 2026 21:40:36 GMT  
		Size: 13.8 MB (13788494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73189a25a3352c3753e616453541d65053722fa055f7ae16f6917a7d066a8012`  
		Last Modified: Fri, 01 May 2026 04:57:18 GMT  
		Size: 58.0 MB (58022967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffab9d03b1a173697b85dcf6367cd0b90155bc06c2fcd0935ad95b1c0130bd88`  
		Last Modified: Fri, 01 May 2026 04:57:16 GMT  
		Size: 3.9 MB (3866922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969f508657dd7145a1309ecf119140f99c9be6bcaf09d461f1d17f1a2c38b308`  
		Last Modified: Fri, 29 May 2026 23:07:23 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4ef2f21cdc32314af43dfde67fae276ef4353d8b43c5809c55f637ad376ffa`  
		Last Modified: Fri, 29 May 2026 23:07:23 GMT  
		Size: 12.8 KB (12775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963eadce252da3146d69166601cf610eb570c2d72a53aaa54fd459eba7c371cc`  
		Last Modified: Fri, 29 May 2026 23:07:23 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71d8459a1f055990749d845f9d6f971dc7e0772f735746a4d234f14742d34f1`  
		Last Modified: Fri, 29 May 2026 23:07:23 GMT  
		Size: 36.5 KB (36499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09b70b98606e62c117cf82996b49da2042e77db0f955bf6ae253dc5ed1c6ffd`  
		Last Modified: Fri, 29 May 2026 23:07:32 GMT  
		Size: 371.4 MB (371400642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df5a3774f4ede08df5f4f26ec3e7de818176e445d53daa32cde8a4252267787`  
		Last Modified: Fri, 29 May 2026 23:07:24 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfdfe3e657b2107c07d82428cdf46de80278c75fc0df73318018dcf895d626d`  
		Last Modified: Fri, 29 May 2026 23:07:24 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d63e56170be28d3f76fb7f55ad16a6de84d3ab33d246e33302dba72ca3a37c`  
		Last Modified: Fri, 29 May 2026 23:07:25 GMT  
		Size: 13.0 MB (13004739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java17` - unknown; unknown

```console
$ docker pull open-liberty@sha256:778ee7529059238926b64b8eb033fc111a4a40f448fc5aab997d862d269eb13b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5258270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa6fba8718d830f55cbbc487bbf074a31c118d8bfad3a3cfe872e27ce76d3fbf`

```dockerfile
```

-	Layers:
	-	`sha256:4396c7e0879f7512b1cdf2dbdd345f254b83e92138b9508d9a6cd4844e599292`  
		Last Modified: Fri, 29 May 2026 23:07:23 GMT  
		Size: 5.2 MB (5218859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b982d70ae554440ba111bd21a1fb011dfedfb56d7e6aa4bda17dd02656ac9819`  
		Last Modified: Fri, 29 May 2026 23:07:23 GMT  
		Size: 39.4 KB (39411 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta-java17` - linux; s390x

```console
$ docker pull open-liberty@sha256:f93ebe64e0805c2d669d46161618e07996d7a52fde20544abc95b337ae5ef01a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.2 MB (493194286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921ee7a6a744a34cc8a3a8fca50afce40b97f744022694ca3e1c6ebcd9f07f7f`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 10 Apr 2026 06:50:27 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:50:29 GMT
ADD file:41defd98c44eed6fc946fd94496a94164879f2ad4f63d66a5c1e213cc2259ad1 in / 
# Fri, 10 Apr 2026 06:50:29 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:50:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:50:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:50:13 GMT
ENV JAVA_VERSION=17.0.19.0
# Thu, 30 Apr 2026 23:55:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3ce5bd7829e198408dd3e27825f096f79d19438ac1e96bc583a32d9580f1d3a6';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_aarch64_linux_17.0.19.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='2dc4cfb4256642cfbea7fbe0edc30e79f995e7f1e01408876b88517b52cae4ad';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_ppc64le_linux_17.0.19.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b40a28e68e84461607a5d802fe6ddb7376e4a3d8e477b32bbe5c1cdf5638a7ed';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_x64_linux_17.0.19.0.tar.gz';          ;;        s390x)          ESUM='a9abce59480d62967ffe4a6c4b176a3e22bbef7e9ec9dd4cb58d23d5881f4d58';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_s390x_linux_17.0.19.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Apr 2026 23:55:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:55:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Apr 2026 23:56:49 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54";     TOMCAT_VERSION="9.0.117";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 29 May 2026 23:03:04 GMT
USER root
# Fri, 29 May 2026 23:03:04 GMT
ARG LIBERTY_VERSION=26.0.0.6-beta
# Fri, 29 May 2026 23:03:04 GMT
ARG LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52
# Fri, 29 May 2026 23:03:04 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip
# Fri, 29 May 2026 23:03:04 GMT
ARG LIBERTY_BUILD_LABEL=cl260520260430-1602
# Fri, 29 May 2026 23:03:04 GMT
ARG OPENJ9_SCC=true
# Fri, 29 May 2026 23:03:04 GMT
ARG VERBOSE=false
# Fri, 29 May 2026 23:03:04 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260520260430-1602 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=26.0.0.6-beta liberty.version=26.0.0.6-beta io.openliberty.version=26.0.0.6-beta
# Fri, 29 May 2026 23:03:04 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Fri, 29 May 2026 23:03:04 GMT
COPY helpers /opt/ol/helpers # buildkit
# Fri, 29 May 2026 23:03:04 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Fri, 29 May 2026 23:03:05 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 29 May 2026 23:03:25 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Fri, 29 May 2026 23:03:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 29 May 2026 23:03:26 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 29 May 2026 23:03:26 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 29 May 2026 23:04:04 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Fri, 29 May 2026 23:04:04 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 29 May 2026 23:04:04 GMT
USER 1001
# Fri, 29 May 2026 23:04:04 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 29 May 2026 23:04:04 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 29 May 2026 23:04:04 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:ef1c26d09a5f9962879f732e212c4246a41e8473f6120efb435886357c85dd5a`  
		Last Modified: Fri, 10 Apr 2026 09:34:53 GMT  
		Size: 29.9 MB (29912147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a45433edaccf5d141e572facc743118ac3f34051bab72b31c6fffae6248562`  
		Last Modified: Wed, 15 Apr 2026 20:51:45 GMT  
		Size: 13.1 MB (13117615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0701e4b840e35cb8e3275f5fb084ffb2f54db6dbd06ca8c2e453994952427a44`  
		Last Modified: Thu, 30 Apr 2026 23:57:09 GMT  
		Size: 58.3 MB (58298181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb4c2b5431d5ede0be346c9b6d7ca7e7be7d0b9eb37d9fc69df71cd8f36eab6`  
		Last Modified: Thu, 30 Apr 2026 23:57:08 GMT  
		Size: 5.2 MB (5172082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614b75c21bea927fcf55648fb92ce163ea870854733456608991d094148e13bf`  
		Last Modified: Fri, 29 May 2026 23:04:46 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6064ad1eccdbd3d7ef71a841b2ff747d9cfc78ae3aac8a8d683691e74ae70d7d`  
		Last Modified: Fri, 29 May 2026 23:04:46 GMT  
		Size: 12.8 KB (12775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45df2e49982e04a6645f76fa11c0f5948a7832635767e9db85aaa44c47da29e1`  
		Last Modified: Fri, 29 May 2026 23:04:46 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4db638467617666d723a045677658cf975a7aa5144799ba2f3ea17a1f93efec`  
		Last Modified: Fri, 29 May 2026 23:03:38 GMT  
		Size: 33.1 KB (33112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0dc38ea14c70467ceced608b2f0ddb2f332596d4a1bf01e127113da77ce2ff`  
		Last Modified: Fri, 29 May 2026 23:04:56 GMT  
		Size: 371.4 MB (371400116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a631fc615abe879e8c02257b732693d415c721ad94bd30650193789cc1a6303`  
		Last Modified: Fri, 29 May 2026 23:04:48 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593a20065447efc861d92d8610555c1dcb70d7eead3125f137030b77e4dbb9ac`  
		Last Modified: Fri, 29 May 2026 23:04:48 GMT  
		Size: 14.2 KB (14217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e52e698a6e4295da0424a85534ef7fa8b9fd7b9d926feadc0ab1d12956f546`  
		Last Modified: Fri, 29 May 2026 23:04:49 GMT  
		Size: 15.2 MB (15231700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java17` - unknown; unknown

```console
$ docker pull open-liberty@sha256:53e3f1f0084580159c6b44224e1608468c638163b4c872f8c2759078d8d5d1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5254610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c7cb27dc1d177bf0a7ad58225685efbf8d12bb79e6263e0f10b315030ca9e64`

```dockerfile
```

-	Layers:
	-	`sha256:f3738ae1830d29dadb4db28089af95301541a00f83956f0e04f662581d187359`  
		Last Modified: Fri, 29 May 2026 23:04:48 GMT  
		Size: 5.2 MB (5215234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d721f59469c01faf3121d978de3e8f98e952fc4720b6a915e2294d5b73a2f68c`  
		Last Modified: Fri, 29 May 2026 23:04:47 GMT  
		Size: 39.4 KB (39376 bytes)  
		MIME: application/vnd.in-toto+json
