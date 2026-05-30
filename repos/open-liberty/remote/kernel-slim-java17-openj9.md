## `open-liberty:kernel-slim-java17-openj9`

```console
$ docker pull open-liberty@sha256:3096b51a0a6774c0f414ae6f075fa7f1bae44cffed0532ee0a1a8f6e532ec9bf
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

### `open-liberty:kernel-slim-java17-openj9` - linux; amd64

```console
$ docker pull open-liberty@sha256:4086649c33d15f2ed7f16f6161b8cc93108eb69b50568e5c452a795ffd8337cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121720366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18aeb6ebe85ca6af6122e1b80c3867e3eacfdee8439ca3066886397f3fa14d5`
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
# Fri, 29 May 2026 23:04:34 GMT
USER root
# Fri, 29 May 2026 23:04:34 GMT
ARG LIBERTY_VERSION=26.0.0.5
# Fri, 29 May 2026 23:04:34 GMT
ARG LIBERTY_SHA=7af44d05ef0f0f04cd7e8baa26fa3bf227297a71
# Fri, 29 May 2026 23:04:34 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.5/openliberty-kernel-26.0.0.5.zip
# Fri, 29 May 2026 23:04:34 GMT
ARG LIBERTY_BUILD_LABEL=cl260520260430-1602
# Fri, 29 May 2026 23:04:34 GMT
ARG OPENJ9_SCC=true
# Fri, 29 May 2026 23:04:34 GMT
ARG VERBOSE=false
# Fri, 29 May 2026 23:04:34 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260520260430-1602 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=26.0.0.5 liberty.version=26.0.0.5 io.openliberty.version=26.0.0.5
# Fri, 29 May 2026 23:04:34 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Fri, 29 May 2026 23:04:34 GMT
COPY helpers /opt/ol/helpers # buildkit
# Fri, 29 May 2026 23:04:34 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Fri, 29 May 2026 23:04:34 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=7af44d05ef0f0f04cd7e8baa26fa3bf227297a71 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.5/openliberty-kernel-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 29 May 2026 23:04:40 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=7af44d05ef0f0f04cd7e8baa26fa3bf227297a71 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.5/openliberty-kernel-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Fri, 29 May 2026 23:04:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 29 May 2026 23:04:41 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=7af44d05ef0f0f04cd7e8baa26fa3bf227297a71 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.5/openliberty-kernel-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 29 May 2026 23:04:41 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=7af44d05ef0f0f04cd7e8baa26fa3bf227297a71 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.5/openliberty-kernel-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 29 May 2026 23:04:45 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=7af44d05ef0f0f04cd7e8baa26fa3bf227297a71 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.5/openliberty-kernel-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Fri, 29 May 2026 23:04:45 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 29 May 2026 23:04:45 GMT
USER 1001
# Fri, 29 May 2026 23:04:45 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 29 May 2026 23:04:45 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 29 May 2026 23:04:45 GMT
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
	-	`sha256:5258ac82f30729b986a3b85f63315fc0c6d5aec70a2b8d0daa11075d4134e967`  
		Last Modified: Fri, 29 May 2026 23:04:54 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d265c185455fcdade9155d6ff69332e6a2bc48ecbc0b8bc9b413ca8b99f3713`  
		Last Modified: Fri, 29 May 2026 23:04:54 GMT  
		Size: 11.9 KB (11884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbba8f0b00f1c7417f67173fb24bf0e79277d0aed02ab75c5fdd9155705255d`  
		Last Modified: Fri, 29 May 2026 23:04:54 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7337341fc912b0b17ebfae785b43671c1013b4e4525df9ee245d654a0dfc678`  
		Last Modified: Fri, 29 May 2026 23:04:54 GMT  
		Size: 31.7 KB (31748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b21f84f69095721b823203c7ae4f53f542c318d37ccfb5eb80204577c698172`  
		Last Modified: Fri, 29 May 2026 23:04:56 GMT  
		Size: 15.3 MB (15309977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27d93a18500c8a4985f2fb662a532648a672366e9c266c87813c076705de9a6`  
		Last Modified: Fri, 29 May 2026 23:04:55 GMT  
		Size: 736.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37a0fa4ead15064377826246c30c533aaaa56233ecad1d7aacb0e2e6d815eb0`  
		Last Modified: Fri, 29 May 2026 23:04:55 GMT  
		Size: 13.0 KB (12989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0b5b5ca1b131e957a274238534b2d83d6647fb73b0d6269f52760e50a92a72`  
		Last Modified: Fri, 29 May 2026 23:04:55 GMT  
		Size: 2.7 MB (2711853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:kernel-slim-java17-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:347d3e29167dafed970b74410924ad471ae10cb994bd3e361bfc1051767036dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3346654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf36d1a709d051f3d8ac2811d3943225f3d826529d501055b557e2d718afffd`

```dockerfile
```

-	Layers:
	-	`sha256:d04dfd47c5ebb697aab953a18d309308c6d8cd0c894ac75c7b229dab2e97b9d2`  
		Last Modified: Fri, 29 May 2026 23:04:54 GMT  
		Size: 3.3 MB (3307637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b21ba73cbbe569f70fe032e3f3f17ced4f5e8379d8a66c6af727c9a775277a2`  
		Last Modified: Fri, 29 May 2026 23:04:54 GMT  
		Size: 39.0 KB (39017 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:kernel-slim-java17-openj9` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:8b95c5d140a4b5f23e5a869cf19e8238f7ea1b289a4513df29be033ab1781ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118680718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9efdca87919597fbc72588e07af1a5bda82495f165de4b87966090b27d9516c7`
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
# Fri, 29 May 2026 23:04:37 GMT
USER root
# Fri, 29 May 2026 23:04:37 GMT
ARG LIBERTY_VERSION=26.0.0.5
# Fri, 29 May 2026 23:04:37 GMT
ARG LIBERTY_SHA=7af44d05ef0f0f04cd7e8baa26fa3bf227297a71
# Fri, 29 May 2026 23:04:37 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.5/openliberty-kernel-26.0.0.5.zip
# Fri, 29 May 2026 23:04:37 GMT
ARG LIBERTY_BUILD_LABEL=cl260520260430-1602
# Fri, 29 May 2026 23:04:37 GMT
ARG OPENJ9_SCC=true
# Fri, 29 May 2026 23:04:37 GMT
ARG VERBOSE=false
# Fri, 29 May 2026 23:04:37 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260520260430-1602 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=26.0.0.5 liberty.version=26.0.0.5 io.openliberty.version=26.0.0.5
# Fri, 29 May 2026 23:04:37 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Fri, 29 May 2026 23:04:37 GMT
COPY helpers /opt/ol/helpers # buildkit
# Fri, 29 May 2026 23:04:37 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Fri, 29 May 2026 23:04:37 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=7af44d05ef0f0f04cd7e8baa26fa3bf227297a71 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.5/openliberty-kernel-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 29 May 2026 23:04:47 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=7af44d05ef0f0f04cd7e8baa26fa3bf227297a71 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.5/openliberty-kernel-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Fri, 29 May 2026 23:04:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 29 May 2026 23:04:47 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=7af44d05ef0f0f04cd7e8baa26fa3bf227297a71 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.5/openliberty-kernel-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 29 May 2026 23:04:47 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=7af44d05ef0f0f04cd7e8baa26fa3bf227297a71 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.5/openliberty-kernel-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 29 May 2026 23:04:52 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=7af44d05ef0f0f04cd7e8baa26fa3bf227297a71 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.5/openliberty-kernel-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Fri, 29 May 2026 23:04:52 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 29 May 2026 23:04:52 GMT
USER 1001
# Fri, 29 May 2026 23:04:52 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 29 May 2026 23:04:52 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 29 May 2026 23:04:52 GMT
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
	-	`sha256:d14485c1becd8228622e390e69a5ab76e65d44ba25c67759efb58af60c1ba30c`  
		Last Modified: Fri, 29 May 2026 23:05:00 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deddaac587d6d30ed9562a8e978b2fa730d0e91f26745e0d3df5f3677ffa66a2`  
		Last Modified: Fri, 29 May 2026 23:05:01 GMT  
		Size: 11.9 KB (11892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c93e73ee8acfe036903114e1407e18b3feb9853065c7affe376f934c7f5b4d8`  
		Last Modified: Fri, 29 May 2026 23:05:01 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61918cfbaf7cf7d1e0dfe5582dd422292dd6b978707e51063a8a4292a01577f3`  
		Last Modified: Fri, 29 May 2026 23:05:00 GMT  
		Size: 42.3 KB (42325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973c831a05241073a2670b1a547df398fc82bb11c1d72c88d4cc8f316fa04f0b`  
		Last Modified: Fri, 29 May 2026 23:05:02 GMT  
		Size: 15.3 MB (15310131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be62c7aac8a4f383f0801f51450255e0beae3545025a93b7a98a39aa8c21eba4`  
		Last Modified: Fri, 29 May 2026 23:05:02 GMT  
		Size: 737.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a141246a7a8a66456f2e249664e1d23cd3b0a8f7df76461ab261378e2b0d2f35`  
		Last Modified: Fri, 29 May 2026 23:05:02 GMT  
		Size: 13.0 KB (12988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629d3c3a979034af790f4cf0d082460eaf3f3f2874fd24354f74f19ffc2bf461`  
		Last Modified: Fri, 29 May 2026 23:05:02 GMT  
		Size: 2.8 MB (2807045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:kernel-slim-java17-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:34794246aa709d1c58ba37f16d32489520ea3c5a2e44eb5ce1ef20bf54ed7c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3345312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbc8bcde519074e8e21518d9948dc2875ebe50803e31c0b5d14f2fd0b9ae9e9d`

```dockerfile
```

-	Layers:
	-	`sha256:b1814b5ac4ba57c3d028e418e183e8415652a98dde05b98762f0815d953da24c`  
		Last Modified: Fri, 29 May 2026 23:05:01 GMT  
		Size: 3.3 MB (3306167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d561c043474629fbd46a2ade2b60d8bd88ee974b566d129e3d0e394763115fed`  
		Last Modified: Fri, 29 May 2026 23:05:00 GMT  
		Size: 39.1 KB (39145 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:kernel-slim-java17-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:e196783b24a3af9a5c1e940d9c4ebf1fce8a933dc05d3c1f3b1859ce5d9ccb5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (128035206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f6d518e9e2e76d5fe16bbb08c2b6be740a956c625a17a9188f8a6cb52ff954c`
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
ARG LIBERTY_VERSION=26.0.0.5
# Fri, 29 May 2026 23:05:27 GMT
ARG LIBERTY_SHA=7af44d05ef0f0f04cd7e8baa26fa3bf227297a71
# Fri, 29 May 2026 23:05:27 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.5/openliberty-kernel-26.0.0.5.zip
# Fri, 29 May 2026 23:05:27 GMT
ARG LIBERTY_BUILD_LABEL=cl260520260430-1602
# Fri, 29 May 2026 23:05:27 GMT
ARG OPENJ9_SCC=true
# Fri, 29 May 2026 23:05:27 GMT
ARG VERBOSE=false
# Fri, 29 May 2026 23:05:27 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260520260430-1602 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=26.0.0.5 liberty.version=26.0.0.5 io.openliberty.version=26.0.0.5
# Fri, 29 May 2026 23:05:27 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Fri, 29 May 2026 23:07:20 GMT
COPY helpers /opt/ol/helpers # buildkit
# Fri, 29 May 2026 23:07:20 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Fri, 29 May 2026 23:07:21 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=7af44d05ef0f0f04cd7e8baa26fa3bf227297a71 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.5/openliberty-kernel-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 29 May 2026 23:07:33 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=7af44d05ef0f0f04cd7e8baa26fa3bf227297a71 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.5/openliberty-kernel-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Fri, 29 May 2026 23:07:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 29 May 2026 23:07:33 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=7af44d05ef0f0f04cd7e8baa26fa3bf227297a71 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.5/openliberty-kernel-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 29 May 2026 23:07:34 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=7af44d05ef0f0f04cd7e8baa26fa3bf227297a71 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.5/openliberty-kernel-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 29 May 2026 23:07:43 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=7af44d05ef0f0f04cd7e8baa26fa3bf227297a71 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.5/openliberty-kernel-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Fri, 29 May 2026 23:07:43 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 29 May 2026 23:07:43 GMT
USER 1001
# Fri, 29 May 2026 23:07:43 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 29 May 2026 23:07:43 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 29 May 2026 23:07:43 GMT
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
	-	`sha256:94dbe82b3ea1933a2f4d9f1e4e13b66ba5540085bf2551a15bff8d93bcf0db95`  
		Last Modified: Fri, 29 May 2026 23:07:59 GMT  
		Size: 11.9 KB (11888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e473b1738fd1f3fa1f387547adbc7c1aca9ce86db697c4cc9d4a1f9699c601`  
		Last Modified: Fri, 29 May 2026 23:07:59 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe132f646e3f2d1723f62a853fc52212159fd3105f61dd2f18c144729ebb3a6`  
		Last Modified: Fri, 29 May 2026 23:07:59 GMT  
		Size: 36.5 KB (36499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003a312b5ffc0e882f5a723083fe89215d81b6c721808d3ef6e5cb8d1e56c700`  
		Last Modified: Fri, 29 May 2026 23:07:59 GMT  
		Size: 15.3 MB (15310388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360d8b2ae15d6c147420a6e5cf5001d7555b42bc45577818b789a039635454e2`  
		Last Modified: Fri, 29 May 2026 23:08:00 GMT  
		Size: 739.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079c930d00a1badb89509eaef590b19560a66aa515ffa2df29ab453972408677`  
		Last Modified: Fri, 29 May 2026 23:08:00 GMT  
		Size: 13.0 KB (13004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec39f061dd4e7fe6a6748b75da0f4c131013b90272909a3bca8971198efea08a`  
		Last Modified: Fri, 29 May 2026 23:08:00 GMT  
		Size: 2.7 MB (2668831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:kernel-slim-java17-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:71caf8e637a3519b9430c2e6cc353524872f73c25f1362c65c2f01e534b59f04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3351310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0591b01f0c373aedcc0e3d3797a382337e5ed4a3568731deef87b41cb00fc7b6`

```dockerfile
```

-	Layers:
	-	`sha256:85f6ddc4b1f0a87a3c745156739e92b4dec379d27f7435b3095109a557380595`  
		Last Modified: Fri, 29 May 2026 23:07:59 GMT  
		Size: 3.3 MB (3312259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07077a58346022feaf760ee308821b1ecfd0cd4cc88337dae39e11f69fc00d37`  
		Last Modified: Fri, 29 May 2026 23:07:58 GMT  
		Size: 39.1 KB (39051 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:kernel-slim-java17-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:c2bb92829e952f96d2aab9b2e4c4fb92884e1d2cbf61268d608ccae99c200935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124697325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa9a1d5cab42fcd6c4ba8adcab4670fa61ee80d3e7fbcff9a243234c431ab72`
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
# Fri, 29 May 2026 23:04:55 GMT
USER root
# Fri, 29 May 2026 23:04:55 GMT
ARG LIBERTY_VERSION=26.0.0.5
# Fri, 29 May 2026 23:04:55 GMT
ARG LIBERTY_SHA=7af44d05ef0f0f04cd7e8baa26fa3bf227297a71
# Fri, 29 May 2026 23:04:55 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.5/openliberty-kernel-26.0.0.5.zip
# Fri, 29 May 2026 23:04:55 GMT
ARG LIBERTY_BUILD_LABEL=cl260520260430-1602
# Fri, 29 May 2026 23:04:55 GMT
ARG OPENJ9_SCC=true
# Fri, 29 May 2026 23:04:55 GMT
ARG VERBOSE=false
# Fri, 29 May 2026 23:04:55 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260520260430-1602 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=26.0.0.5 liberty.version=26.0.0.5 io.openliberty.version=26.0.0.5
# Fri, 29 May 2026 23:04:55 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Fri, 29 May 2026 23:04:55 GMT
COPY helpers /opt/ol/helpers # buildkit
# Fri, 29 May 2026 23:04:55 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Fri, 29 May 2026 23:04:56 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=7af44d05ef0f0f04cd7e8baa26fa3bf227297a71 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.5/openliberty-kernel-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 29 May 2026 23:05:03 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=7af44d05ef0f0f04cd7e8baa26fa3bf227297a71 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.5/openliberty-kernel-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Fri, 29 May 2026 23:05:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 29 May 2026 23:05:04 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=7af44d05ef0f0f04cd7e8baa26fa3bf227297a71 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.5/openliberty-kernel-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 29 May 2026 23:05:04 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=7af44d05ef0f0f04cd7e8baa26fa3bf227297a71 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.5/openliberty-kernel-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 29 May 2026 23:05:10 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=7af44d05ef0f0f04cd7e8baa26fa3bf227297a71 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.5/openliberty-kernel-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Fri, 29 May 2026 23:05:10 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 29 May 2026 23:05:10 GMT
USER 1001
# Fri, 29 May 2026 23:05:10 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 29 May 2026 23:05:10 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 29 May 2026 23:05:10 GMT
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
	-	`sha256:a08114bd20a2b8999b2cb12ecaa5ed7be83012d7dbccd05ab6ea7ead730d6649`  
		Last Modified: Fri, 29 May 2026 23:05:26 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004f635a0102deda1f73bc8a0ebb28085ad75520a5e51d59448580c7e9a24249`  
		Last Modified: Fri, 29 May 2026 23:05:26 GMT  
		Size: 11.9 KB (11888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f648b9710b320f1e0b776b31d85d558a618416a76da138ac96843bd4bd26c8`  
		Last Modified: Fri, 29 May 2026 23:05:26 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61b3708caa6ade52b0dcb13d81556003d459fe0874834c134ea0c2988e5ee62`  
		Last Modified: Fri, 29 May 2026 23:05:26 GMT  
		Size: 33.1 KB (33113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f483d1b83568264949a036962d036ea9c4c01ba8ec4796833f16c1748b80d5`  
		Last Modified: Fri, 29 May 2026 23:05:27 GMT  
		Size: 15.3 MB (15309819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41af8f35acc97789156201782f37243f72c43ec83bb0fdbcfc977f0f80d85add`  
		Last Modified: Fri, 29 May 2026 23:05:27 GMT  
		Size: 737.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af92d1ddab5120f776b5a93de6a9a336e1a9bf52d90828310f53bbf180acd869`  
		Last Modified: Fri, 29 May 2026 23:05:27 GMT  
		Size: 13.0 KB (12987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1431731c992870a978f273df4e2a404493e90a6449976c49382d761d00364050`  
		Last Modified: Fri, 29 May 2026 23:05:27 GMT  
		Size: 2.8 MB (2827466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:kernel-slim-java17-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:cd08f4c4d7c52863fbe9fcfd70b65afc67f9435933b3d1fdafc2c7d9d322c45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3347651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:778362af48dac0cf49f8c202d6aa7a77ee17062d0514cf71fb3a791be61b0b41`

```dockerfile
```

-	Layers:
	-	`sha256:cce21627a18e5c2638162655e680c5f55076335e60613190c83590a6abed5370`  
		Last Modified: Fri, 29 May 2026 23:05:26 GMT  
		Size: 3.3 MB (3308634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a76c585603d729175174e3a4f897afa5584e5ce56ea943b55e11f2ff86facae`  
		Last Modified: Fri, 29 May 2026 23:05:26 GMT  
		Size: 39.0 KB (39017 bytes)  
		MIME: application/vnd.in-toto+json
