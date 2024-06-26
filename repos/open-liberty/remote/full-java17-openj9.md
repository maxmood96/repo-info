## `open-liberty:full-java17-openj9`

```console
$ docker pull open-liberty@sha256:b5bf33eab48be3d0e3470cff690212d8ce9f621687c8a33c731abeb185c63002
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
$ docker pull open-liberty@sha256:6030fee251bfcdec528ca57919ecf4e2f83b28170b803e881ef0d6c02bff1478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.5 MB (441464957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:530226ea98341005964cdaeb1692de43a37a4e26c18bacbfac385463a5a9f9d9`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Tue, 04 Jun 2024 05:42:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jun 2024 05:42:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_VERSION=jdk-17.0.11+9_openj9-0.44.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6764398cdbcf824f2b99c095d58efb69b140d0c9824239560d58478f67bc15b';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='12a951e5353f4bccae5430de05a7204b6e1ad983780d3ecccacd2179936cc9ee';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='a47d3fabdf14c0f56561e5be24d689007f42cb079af0c89db235a58899fd4ab3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='049c6d6db4ba22fdfc7aaef3ee0af1bed1b71bda314b5c9ab27451d2c7392c1c';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
USER root
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_VERSION=24.0.0.6
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_BUILD_LABEL=cl240620240603-2001
# Tue, 18 Jun 2024 19:00:56 GMT
ARG OPENJ9_SCC=true
# Tue, 18 Jun 2024 19:00:56 GMT
ARG VERBOSE=false
# Tue, 18 Jun 2024 19:00:56 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240620240603-2001 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=24.0.0.6
# Tue, 18 Jun 2024 19:00:56 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 18 Jun 2024 19:00:56 GMT
USER 1001
# Tue, 18 Jun 2024 19:00:56 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 18 Jun 2024 19:00:56 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 18 Jun 2024 19:00:56 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1caed285279b70876339bbe014f88df1a0da4e59366aff9d1878be3db91715`  
		Last Modified: Tue, 25 Jun 2024 22:57:47 GMT  
		Size: 12.2 MB (12156356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21e2392004ab682d0b9861122ab369e70f7e2c63551d119b99fad5ef3f6bc80`  
		Last Modified: Tue, 25 Jun 2024 22:57:48 GMT  
		Size: 51.8 MB (51801996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bc69067995835417edb239a454b7c4c67c3b5b37aa130a374a7193a448c265`  
		Last Modified: Tue, 25 Jun 2024 22:57:47 GMT  
		Size: 4.9 MB (4945206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29cac7024831c3f20e87b47892d21682e53ffabcfc64064c648a8327d0a9ecf8`  
		Last Modified: Tue, 25 Jun 2024 23:56:52 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbafc5d050c38d78d4452df30f19f288d3c1b650939005d22ea038db2501bdc`  
		Last Modified: Tue, 25 Jun 2024 23:56:57 GMT  
		Size: 10.0 KB (9996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b45d562a1b8f90d8ed974aaa87db00384ae6cf7af6eca4ab59033b34193397`  
		Last Modified: Tue, 25 Jun 2024 23:56:57 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575aca4ee4c8ff52525742bdc99846f8c2ddaf1cffc766d19e7536faf3e461e3`  
		Last Modified: Tue, 25 Jun 2024 23:56:01 GMT  
		Size: 31.7 KB (31746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c48ce5750fc0f6795487100e408aef96e3444443d16c6579238e431f8fdac83`  
		Last Modified: Tue, 25 Jun 2024 23:57:06 GMT  
		Size: 329.0 MB (328967522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e0c43079a9196f1dcdade55cc06e2325f24a2276e49aaecb8b62ec86c3cea0`  
		Last Modified: Tue, 25 Jun 2024 23:56:58 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30bf7197d6ea9ebf77f6cef9411632c16ae144d2225192bc83f1c9666ad31ce`  
		Last Modified: Tue, 25 Jun 2024 23:56:59 GMT  
		Size: 11.3 KB (11344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03302ba67d8980b1375987b22a921be6df62bef0aa81a0d5acd12d7863fa084b`  
		Last Modified: Tue, 25 Jun 2024 23:56:59 GMT  
		Size: 14.0 MB (14004687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:0b99f1a5a19044bf2e71c7ecbf5977b38f6f1e04bed91ebd1b7c47c37f08cde0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:962e84c484f94394eba4a2c66b1481bff7854c600a09e9598f938560ab1ee4b8`

```dockerfile
```

-	Layers:
	-	`sha256:175487adbc2ccfcc06fb111eabea371b7c1aa06ada0482652434ded48290ffb0`  
		Last Modified: Tue, 25 Jun 2024 23:56:58 GMT  
		Size: 5.1 MB (5085125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b9bc4fbfe67423059cc9f6204e0a3b2b8eb0e05d4828896c9863a55939d639e`  
		Last Modified: Tue, 25 Jun 2024 23:56:57 GMT  
		Size: 38.5 KB (38539 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java17-openj9` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:ac53c6a6a923d09fd7fdf2b48ae4ffc26151b27e518bef206a37e6399a694fe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.2 MB (434154752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a244a42476179fc9257ef78cf7c9495ce6822a447022f0f71a0815dd89127b`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Tue, 04 Jun 2024 05:42:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jun 2024 05:42:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_VERSION=jdk-17.0.11+9_openj9-0.44.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6764398cdbcf824f2b99c095d58efb69b140d0c9824239560d58478f67bc15b';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='12a951e5353f4bccae5430de05a7204b6e1ad983780d3ecccacd2179936cc9ee';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='a47d3fabdf14c0f56561e5be24d689007f42cb079af0c89db235a58899fd4ab3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='049c6d6db4ba22fdfc7aaef3ee0af1bed1b71bda314b5c9ab27451d2c7392c1c';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
USER root
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_VERSION=24.0.0.6
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_BUILD_LABEL=cl240620240603-2001
# Tue, 18 Jun 2024 19:00:56 GMT
ARG OPENJ9_SCC=true
# Tue, 18 Jun 2024 19:00:56 GMT
ARG VERBOSE=false
# Tue, 18 Jun 2024 19:00:56 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240620240603-2001 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=24.0.0.6
# Tue, 18 Jun 2024 19:00:56 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 18 Jun 2024 19:00:56 GMT
USER 1001
# Tue, 18 Jun 2024 19:00:56 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 18 Jun 2024 19:00:56 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 18 Jun 2024 19:00:56 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ee6e790fe3be315f574c78a35fef5e2104480be37cd385884a99abf457a751`  
		Last Modified: Tue, 25 Jun 2024 23:02:58 GMT  
		Size: 12.1 MB (12115683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d41085751fa6c914fb77c7c988583d00a74ba2218addf424f76d86f10f5019`  
		Last Modified: Tue, 25 Jun 2024 23:21:26 GMT  
		Size: 47.8 MB (47819155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8816e6da8042c0a68bac948203274e471e1336e9c4fdcdd497b8b7f211483a`  
		Last Modified: Tue, 25 Jun 2024 23:21:24 GMT  
		Size: 4.6 MB (4630143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3fd868ceff83cff77b9285322c0b6b39845e53db5e1be2004c5c72e31fe17f`  
		Last Modified: Wed, 26 Jun 2024 00:48:54 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3361051a316fc5480344f48efbb895243790d4ac56544e1728d74bce51c2b2`  
		Last Modified: Wed, 26 Jun 2024 00:48:54 GMT  
		Size: 10.0 KB (9993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ed23949ce6c866ab3df5e812fda9c20e584177acfb7c38843b8f2c54d48e65`  
		Last Modified: Wed, 26 Jun 2024 00:48:54 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9d003b7e4a5a2db12ad5b63f5bc6946294a15c544ea761e9b0cf12a4c4c56e`  
		Last Modified: Wed, 26 Jun 2024 00:55:27 GMT  
		Size: 42.3 KB (42322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36b882dce8f86c95e94cc1e22105edb09e3b818591f05b86c43a98e375acdea`  
		Last Modified: Wed, 26 Jun 2024 00:55:35 GMT  
		Size: 329.0 MB (328968548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8b8316c37e54f52fde1ae87481466db312da475e58e0e3f08b7696a6c1d411`  
		Last Modified: Wed, 26 Jun 2024 00:55:27 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828a70cee61d772f0c6801fa8d95c8ddb0d1a8289bf727c48488e1d3dc88a371`  
		Last Modified: Wed, 26 Jun 2024 00:55:27 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05eabc8d30fb4d2a6f9f6dd5adc6694edc39e2ae2f37818e1717d6abe093066f`  
		Last Modified: Wed, 26 Jun 2024 00:55:29 GMT  
		Size: 13.2 MB (13193427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:634b7c276ea337fa75dadc34602e2352a8eb30c6d44f657792ddddb6ee6ec8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5124266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65fda5236cc96cff4629e03849668a2a2c871499e391764bdc57211be52ba883`

```dockerfile
```

-	Layers:
	-	`sha256:6565942022c7e8410cc7c41bda6cb0b32c5f1c92daa808e583bd44cb6c67dea8`  
		Last Modified: Wed, 26 Jun 2024 00:55:28 GMT  
		Size: 5.1 MB (5085378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5aace102cc86429add689ea6520accc93fd318fbfcb054612c1bb71931bce88`  
		Last Modified: Wed, 26 Jun 2024 00:55:27 GMT  
		Size: 38.9 KB (38888 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java17-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:3205a7835e768607e9a290eb7ac7e9f169ec3c077744a34b68725480ff14203f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.1 MB (445062450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f7752369b9370f2327871daf32cb9807939a0c3d9007e26762e79d214dd9f3`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 03 Jun 2024 10:34:18 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:34:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:34:22 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 10:34:22 GMT
CMD ["/bin/bash"]
# Tue, 04 Jun 2024 05:42:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jun 2024 05:42:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_VERSION=jdk-17.0.11+9_openj9-0.44.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6764398cdbcf824f2b99c095d58efb69b140d0c9824239560d58478f67bc15b';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='12a951e5353f4bccae5430de05a7204b6e1ad983780d3ecccacd2179936cc9ee';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='a47d3fabdf14c0f56561e5be24d689007f42cb079af0c89db235a58899fd4ab3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='049c6d6db4ba22fdfc7aaef3ee0af1bed1b71bda314b5c9ab27451d2c7392c1c';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
USER root
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_VERSION=24.0.0.6
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_BUILD_LABEL=cl240620240603-2001
# Tue, 18 Jun 2024 19:00:56 GMT
ARG OPENJ9_SCC=true
# Tue, 18 Jun 2024 19:00:56 GMT
ARG VERBOSE=false
# Tue, 18 Jun 2024 19:00:56 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240620240603-2001 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=24.0.0.6
# Tue, 18 Jun 2024 19:00:56 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 18 Jun 2024 19:00:56 GMT
USER 1001
# Tue, 18 Jun 2024 19:00:56 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 18 Jun 2024 19:00:56 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 18 Jun 2024 19:00:56 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c866879b3eaab6a2be320ab73cc032a3c43ef798a2582028559e9055cc257b5`  
		Last Modified: Tue, 25 Jun 2024 23:04:25 GMT  
		Size: 12.9 MB (12887989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebaea41eb46467f91bc1a0c2aa095d330e7ff290463f1bd03605a62b4e6a484c`  
		Last Modified: Tue, 25 Jun 2024 23:28:44 GMT  
		Size: 53.1 MB (53050484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3705f9048dbeab52321e0d7886d193b9829c25ee048a331efc16e0e6c459fd3`  
		Last Modified: Tue, 25 Jun 2024 23:28:42 GMT  
		Size: 3.8 MB (3791630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3eb1f0e41485bafd555518ba846aeff30ae8c5ad02cb2deb54b2f12420e07c5`  
		Last Modified: Wed, 26 Jun 2024 01:41:00 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2b5350f15a1f0263cb68e3e080130f3a3a4d7abbdba68332bf18a501dc3980`  
		Last Modified: Wed, 26 Jun 2024 01:41:00 GMT  
		Size: 10.0 KB (9996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7964dcffdbd220c01437298eb6449ee9897b778ec825004a8d801a2bbf92780e`  
		Last Modified: Wed, 26 Jun 2024 01:41:00 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d41de812a66e49f074f222370eada236ab9978a686f33903567ceb1c2617110`  
		Last Modified: Wed, 26 Jun 2024 01:51:50 GMT  
		Size: 36.5 KB (36496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea6297983dea71df50098287d2c8a440f5456dba134e52deb6d257ccf6d34b3`  
		Last Modified: Wed, 26 Jun 2024 01:52:17 GMT  
		Size: 329.0 MB (328967967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6fc92df2857fea638770f7acc81635f34d95ee9839a6c3818641da50607099`  
		Last Modified: Wed, 26 Jun 2024 01:51:50 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0282029231fd62983130bb1dde071149f24f69dad0d193596b923d82ccd65174`  
		Last Modified: Wed, 26 Jun 2024 01:51:50 GMT  
		Size: 11.4 KB (11366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92419e53808152e037305b67b9b1faa027dd677b9b3ef678debe3edf8c1a5cd`  
		Last Modified: Wed, 26 Jun 2024 01:51:52 GMT  
		Size: 11.8 MB (11843480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:1a5cd11a504a01f447cf92be42c1bab50d17dd941e6fd7ed872aaac651ed361d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5128180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55a629ae599e2eb59d0f8e79b1d76c38d7359630d551fd0fcb1342d3992d2cee`

```dockerfile
```

-	Layers:
	-	`sha256:483ab6bef2bb0f6a1758a1fe9c28d3a2cf431c433818d0d2241a1cf696f7f5c4`  
		Last Modified: Wed, 26 Jun 2024 01:51:50 GMT  
		Size: 5.1 MB (5089607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9c301e7f15991cc8fa12aeeea01f09946b9daa2e2f8bb8697fb28eb5702e7aa`  
		Last Modified: Wed, 26 Jun 2024 01:51:50 GMT  
		Size: 38.6 KB (38573 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java17-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:a1419d6ee2806e03f45406532a4047b94a14e2e963c27ea51b908d215d3c80ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.5 MB (438493185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3087f559f8365f33337cee17deec8d5617dbe03e89f545b059e2e96fbfd980`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 03 Jun 2024 10:29:44 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:29:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:29:47 GMT
ADD file:4fb908f3bd908a7abc338d7e2006cb2c97aa7f83aca415f3b86c0ae86d61fed1 in / 
# Mon, 03 Jun 2024 10:29:47 GMT
CMD ["/bin/bash"]
# Tue, 04 Jun 2024 05:42:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jun 2024 05:42:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_VERSION=jdk-17.0.11+9_openj9-0.44.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6764398cdbcf824f2b99c095d58efb69b140d0c9824239560d58478f67bc15b';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='12a951e5353f4bccae5430de05a7204b6e1ad983780d3ecccacd2179936cc9ee';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='a47d3fabdf14c0f56561e5be24d689007f42cb079af0c89db235a58899fd4ab3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='049c6d6db4ba22fdfc7aaef3ee0af1bed1b71bda314b5c9ab27451d2c7392c1c';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
USER root
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_VERSION=24.0.0.6
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_BUILD_LABEL=cl240620240603-2001
# Tue, 18 Jun 2024 19:00:56 GMT
ARG OPENJ9_SCC=true
# Tue, 18 Jun 2024 19:00:56 GMT
ARG VERBOSE=false
# Tue, 18 Jun 2024 19:00:56 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240620240603-2001 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=24.0.0.6
# Tue, 18 Jun 2024 19:00:56 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 18 Jun 2024 19:00:56 GMT
USER 1001
# Tue, 18 Jun 2024 19:00:56 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 18 Jun 2024 19:00:56 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 18 Jun 2024 19:00:56 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:22512bbfe178a8ec7b5e4e48135f8a3e1ad0245ed3ee6a47f89947ce7ffb5d4f`  
		Last Modified: Mon, 03 Jun 2024 10:47:11 GMT  
		Size: 28.0 MB (28000515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7a4135208bd6a1c83ef4006ee13da7687af58d5df19772a183b62d4757a473`  
		Last Modified: Tue, 25 Jun 2024 23:02:32 GMT  
		Size: 12.2 MB (12203759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d83ae276c53c6267bdec42bde076c74e0d614b076724bc3812c2a5ff252d09`  
		Last Modified: Tue, 25 Jun 2024 23:16:03 GMT  
		Size: 50.4 MB (50407672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa33da55c45e8fb4f7217d03d26b910533a5a898601451123298e231e29975c2`  
		Last Modified: Tue, 25 Jun 2024 23:16:02 GMT  
		Size: 5.1 MB (5102854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612f62b76f36f2956b81d0e919ac70e4c7bcee4340f1fe51f3a316bd7ee81429`  
		Last Modified: Wed, 26 Jun 2024 00:00:29 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027fbf749ae4622b77b4d2a2e71bdace49be9e585e630534a66369605157508b`  
		Last Modified: Wed, 26 Jun 2024 00:00:28 GMT  
		Size: 10.0 KB (9995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a41e20e0b8fb3310d550663d28149869f56cd6803cc3f50c654965886671ef`  
		Last Modified: Wed, 26 Jun 2024 00:00:28 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01fd2ba55c2f99ef01dbcaa26741cc12d02f43cd243f97657b7f6a802338c8e0`  
		Last Modified: Wed, 26 Jun 2024 00:08:19 GMT  
		Size: 33.1 KB (33109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6413e5409817d000f9392e0faecdccc33359b41940a7d37a13a054e8635485ae`  
		Last Modified: Wed, 26 Jun 2024 00:08:26 GMT  
		Size: 329.0 MB (328967750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b4c5bba695bdd91526216d7aa46f16683d749af954bf51f3e1de18d19e9b22`  
		Last Modified: Wed, 26 Jun 2024 00:08:20 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53d6690b2e08edcc63851eb06a1c11dbe8ed08a5ef2b9c031407b28a2361f51`  
		Last Modified: Wed, 26 Jun 2024 00:08:20 GMT  
		Size: 11.4 KB (11361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866a34df0c686d9d2e67637c9e10926d3f1b2d4cfabadbdaddebd6e938332f02`  
		Last Modified: Wed, 26 Jun 2024 00:08:21 GMT  
		Size: 13.8 MB (13753820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:cf6c58195c503cda796f638ff402915946282c5dff549dd38506fb177c7d5d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7243dbb37794ead7eb4758ebea668d2f6951168e9241dfceaa83a8210e0bc3aa`

```dockerfile
```

-	Layers:
	-	`sha256:1d16e371ff4c45bfefe0e3b7aa8b629025bf0d565c8de12ba3c89df40d8234ec`  
		Last Modified: Wed, 26 Jun 2024 00:08:19 GMT  
		Size: 5.1 MB (5085450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13bbacb449ec021f9491023dfad1a61e1b5917cd3b25764e5998ad0c653709ff`  
		Last Modified: Wed, 26 Jun 2024 00:08:19 GMT  
		Size: 38.5 KB (38539 bytes)  
		MIME: application/vnd.in-toto+json
