## `open-liberty:beta-java17`

```console
$ docker pull open-liberty@sha256:9063b6a18be21fb5177cee2f1d305ad6f2ff0b0eac3f44f91cec9a55c9cb3cf9
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
$ docker pull open-liberty@sha256:a7242d5cbdd75ff35cb66a72dcff8074619510df23ec7f00c53e67843cc15790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.7 MB (473716215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a025feffbb7bb4f5016d04a812ae718f73a5905a8d00cce9af41c3ff7286599e`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 23 Apr 2025 12:52:37 GMT
ARG RELEASE
# Wed, 23 Apr 2025 12:52:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 12:52:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 12:52:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 12:52:37 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Wed, 23 Apr 2025 12:52:37 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 12:52:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 12:52:37 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
ENV JAVA_VERSION=jdk-17.0.15+6_openj9-0.51.0
# Wed, 23 Apr 2025 12:52:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9a44da58055525719ddb87b2fe21a02562a0897b8b537a65b7a94b1ab28f7eb0';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e852a334a4a3f59bd8478ffe3190bbdb520fa37d8954e17fc7842ede979b15fa';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c4cc045bfd63fc6412251fef184c91a1acad76d74ee48561fd48c174fb1278d3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='6e1afeea17e8d9538bf65c0672482e3813f13a7d61ee74ad75b2372225df53ba';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 12:52:37 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 23 Apr 2025 12:52:37 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
USER root
# Wed, 23 Apr 2025 12:52:37 GMT
ARG LIBERTY_VERSION=25.0.0.5-beta
# Wed, 23 Apr 2025 12:52:37 GMT
ARG LIBERTY_SHA=51a9331cbd038b2a1fb21ee6b2e45c69cedf9487
# Wed, 23 Apr 2025 12:52:37 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.5-beta/openliberty-runtime-25.0.0.5-beta.zip
# Wed, 23 Apr 2025 12:52:37 GMT
ARG LIBERTY_BUILD_LABEL=cl250420250407-1902
# Wed, 23 Apr 2025 12:52:37 GMT
ARG OPENJ9_SCC=true
# Wed, 23 Apr 2025 12:52:37 GMT
ARG VERBOSE=false
# Wed, 23 Apr 2025 12:52:37 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250420250407-1902 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=25.0.0.5-beta liberty.version=25.0.0.5-beta io.openliberty.version=25.0.0.5-beta
# Wed, 23 Apr 2025 12:52:37 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5-beta LIBERTY_SHA=51a9331cbd038b2a1fb21ee6b2e45c69cedf9487 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.5-beta/openliberty-runtime-25.0.0.5-beta.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5-beta LIBERTY_SHA=51a9331cbd038b2a1fb21ee6b2e45c69cedf9487 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.5-beta/openliberty-runtime-25.0.0.5-beta.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5-beta LIBERTY_SHA=51a9331cbd038b2a1fb21ee6b2e45c69cedf9487 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.5-beta/openliberty-runtime-25.0.0.5-beta.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5-beta LIBERTY_SHA=51a9331cbd038b2a1fb21ee6b2e45c69cedf9487 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.5-beta/openliberty-runtime-25.0.0.5-beta.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5-beta LIBERTY_SHA=51a9331cbd038b2a1fb21ee6b2e45c69cedf9487 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.5-beta/openliberty-runtime-25.0.0.5-beta.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 23 Apr 2025 12:52:37 GMT
USER 1001
# Wed, 23 Apr 2025 12:52:37 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 23 Apr 2025 12:52:37 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 23 Apr 2025 12:52:37 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f177f5db89270b070e1644af124a467a0c875ee09cfc1fa9239b72eea64c0c`  
		Last Modified: Fri, 09 May 2025 16:43:44 GMT  
		Size: 12.2 MB (12172112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f688483665c04fc1d231ea5dbc2ea70ccbc9c8d122bfc6b7e099fb087cf466b2`  
		Last Modified: Fri, 09 May 2025 16:43:45 GMT  
		Size: 51.7 MB (51747279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b08cf00ef33c315cf466a143b8b007197e30ed1139cf5830bea6d5c390206b`  
		Last Modified: Fri, 09 May 2025 16:43:44 GMT  
		Size: 5.0 MB (4978829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe7ab016b7a9d487aa9d3393e32271696c8cd75d317973da0d5c7ab4a73efb4`  
		Last Modified: Fri, 09 May 2025 17:09:10 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1103830adbd9410584da1b43cd84b640e7ad94cb3018cfa6cee193e60a87778d`  
		Last Modified: Fri, 09 May 2025 17:09:10 GMT  
		Size: 10.5 KB (10486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07707d52b1cdf4f7f1add21757b01bfe3aa0c345599aedfcc951c82b236dd87f`  
		Last Modified: Fri, 09 May 2025 17:09:10 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd85124ecf5a674a908fe4af11a2ca65caacf75e7e70750540b132206e70485`  
		Last Modified: Fri, 09 May 2025 17:08:07 GMT  
		Size: 31.7 KB (31748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe09736e1fb2184c25639b3d3bafbd5f09c02e938cac5fada18f4ec583f70b60`  
		Last Modified: Fri, 09 May 2025 17:09:20 GMT  
		Size: 361.4 MB (361362357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d1ecbee2211771d4e584f922a832a774a4b89f126b2b2a656f76fb6d6471cf`  
		Last Modified: Fri, 09 May 2025 17:09:11 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbfb609be94203d7d6822c5f4a38123eef3135ee20a0d745b79db34b657821c`  
		Last Modified: Fri, 09 May 2025 17:09:11 GMT  
		Size: 11.8 KB (11837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff362f2e69f3e78d4e0ab2f2d2af4ef8a068be93f3c647e9fa4d865b309ad29a`  
		Last Modified: Fri, 09 May 2025 17:09:12 GMT  
		Size: 13.9 MB (13866606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java17` - unknown; unknown

```console
$ docker pull open-liberty@sha256:cb5172447578059c7b52bfc16f6b153e7bd55a5f7f537458a331939a6e1d9af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5636024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4b59292a384c1098325e2b3d064b32d19de57f5f42bcf1e63f4328e4b9fa71`

```dockerfile
```

-	Layers:
	-	`sha256:7d0c7ae53cede6ef68b5ba205b94f77cd2d21f6dc0a47f859b1a62b2b0bbbc68`  
		Last Modified: Fri, 09 May 2025 17:09:10 GMT  
		Size: 5.6 MB (5597188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a314264abb6582990274978c18c030e63e3f62084e546941281b63011c4c60f6`  
		Last Modified: Fri, 09 May 2025 17:09:10 GMT  
		Size: 38.8 KB (38836 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta-java17` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:f9eb59b8ecec76d761f59281163299ced66a54a92ba50ef7eef8393519dc7ce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.3 MB (467286266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c050cda0884cf6157e84cdcf142fe565dc72ab92d7127524e10f70d67e79bed9`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 23 Apr 2025 12:52:37 GMT
ARG RELEASE
# Wed, 23 Apr 2025 12:52:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 12:52:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 12:52:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 12:52:37 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Wed, 23 Apr 2025 12:52:37 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 12:52:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 12:52:37 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
ENV JAVA_VERSION=jdk-17.0.15+6_openj9-0.51.0
# Wed, 23 Apr 2025 12:52:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9a44da58055525719ddb87b2fe21a02562a0897b8b537a65b7a94b1ab28f7eb0';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e852a334a4a3f59bd8478ffe3190bbdb520fa37d8954e17fc7842ede979b15fa';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c4cc045bfd63fc6412251fef184c91a1acad76d74ee48561fd48c174fb1278d3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='6e1afeea17e8d9538bf65c0672482e3813f13a7d61ee74ad75b2372225df53ba';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 12:52:37 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 23 Apr 2025 12:52:37 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
USER root
# Wed, 23 Apr 2025 12:52:37 GMT
ARG LIBERTY_VERSION=25.0.0.5-beta
# Wed, 23 Apr 2025 12:52:37 GMT
ARG LIBERTY_SHA=51a9331cbd038b2a1fb21ee6b2e45c69cedf9487
# Wed, 23 Apr 2025 12:52:37 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.5-beta/openliberty-runtime-25.0.0.5-beta.zip
# Wed, 23 Apr 2025 12:52:37 GMT
ARG LIBERTY_BUILD_LABEL=cl250420250407-1902
# Wed, 23 Apr 2025 12:52:37 GMT
ARG OPENJ9_SCC=true
# Wed, 23 Apr 2025 12:52:37 GMT
ARG VERBOSE=false
# Wed, 23 Apr 2025 12:52:37 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250420250407-1902 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=25.0.0.5-beta liberty.version=25.0.0.5-beta io.openliberty.version=25.0.0.5-beta
# Wed, 23 Apr 2025 12:52:37 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5-beta LIBERTY_SHA=51a9331cbd038b2a1fb21ee6b2e45c69cedf9487 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.5-beta/openliberty-runtime-25.0.0.5-beta.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5-beta LIBERTY_SHA=51a9331cbd038b2a1fb21ee6b2e45c69cedf9487 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.5-beta/openliberty-runtime-25.0.0.5-beta.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5-beta LIBERTY_SHA=51a9331cbd038b2a1fb21ee6b2e45c69cedf9487 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.5-beta/openliberty-runtime-25.0.0.5-beta.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5-beta LIBERTY_SHA=51a9331cbd038b2a1fb21ee6b2e45c69cedf9487 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.5-beta/openliberty-runtime-25.0.0.5-beta.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5-beta LIBERTY_SHA=51a9331cbd038b2a1fb21ee6b2e45c69cedf9487 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.5-beta/openliberty-runtime-25.0.0.5-beta.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 23 Apr 2025 12:52:37 GMT
USER 1001
# Wed, 23 Apr 2025 12:52:37 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 23 Apr 2025 12:52:37 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 23 Apr 2025 12:52:37 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78892370879d09e257e1f423fb01169148aa714423fd175a7a3f0933ae6673e`  
		Last Modified: Mon, 05 May 2025 17:14:03 GMT  
		Size: 12.1 MB (12129417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87dacafeafdeb88805872487016c74fd9df84de6f2f46dc3979ebbbf50389bf4`  
		Last Modified: Fri, 09 May 2025 17:00:59 GMT  
		Size: 48.2 MB (48190754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94a0d837c9514d458b3301307a2a14be1df802d94a9f125d286ae35ed868894`  
		Last Modified: Fri, 09 May 2025 17:00:58 GMT  
		Size: 4.8 MB (4759116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb54fa7f17369ddbf289c5bb326822dfb1c05f894a8f639458438001e2e9f953`  
		Last Modified: Fri, 09 May 2025 17:13:50 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0142c009df68b55029ab07336a8a9b5e7977a1cf22a27cc4f9c462400896e805`  
		Last Modified: Fri, 09 May 2025 17:13:50 GMT  
		Size: 10.5 KB (10482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c670c22b7a562692d167e26c14909b0d742b8fc18cc35f2bace8eadd980552c`  
		Last Modified: Fri, 09 May 2025 17:13:50 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1332320a5905cec0edb6899a2673902a0ad648e4afbd662f2b02eb7c03aef611`  
		Last Modified: Fri, 09 May 2025 17:13:50 GMT  
		Size: 42.3 KB (42327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d192379051a88167b1e212351e2a5686c9298162f1321148dd6a9788b5e2170`  
		Last Modified: Fri, 09 May 2025 17:14:02 GMT  
		Size: 361.4 MB (361362330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc3a67c7e90e00a24547e531f794d5a9abccff5843baf4037ec3eb8d577e52e`  
		Last Modified: Fri, 09 May 2025 17:13:51 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7be9044746ddc274fdd8aa566de59c575e9671be18482918d573b9891065ade`  
		Last Modified: Fri, 09 May 2025 17:13:51 GMT  
		Size: 11.8 KB (11840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847d424159ea8a997c4e40b09f85fe3a4770922cf2200f5c7cc0f726cddf80f1`  
		Last Modified: Fri, 09 May 2025 17:13:52 GMT  
		Size: 13.4 MB (13423444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java17` - unknown; unknown

```console
$ docker pull open-liberty@sha256:e9ec52464fa07504c8b38d7218b6fc955d7939bac3f2296abeff6c2782bddcae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5629486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439136cfeb899f191b7af2dc15b37ce06ee73f608eec31734d3044334f32648f`

```dockerfile
```

-	Layers:
	-	`sha256:3c996c1d8cb708c763ec8462d9eb42935e7ee03225e95cf5db927231b1e80951`  
		Last Modified: Fri, 09 May 2025 17:13:50 GMT  
		Size: 5.6 MB (5590522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7da98e973916c6773ed763b5d20f408f184ca40578316fb055458c4ab9d56dc`  
		Last Modified: Fri, 09 May 2025 17:13:50 GMT  
		Size: 39.0 KB (38964 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta-java17` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:3c5d7ef9c6cd7a1ad84633c1c60ecdf8f8ed576382c208f03f97a52304cb2788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.4 MB (477400230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db949ebe7cfe75d21a5af723f7f062460843ec9628a252dc43776f782a48cd79`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 13 Mar 2025 08:54:45 GMT
ARG RELEASE
# Thu, 13 Mar 2025 08:54:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Mar 2025 08:54:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Mar 2025 08:54:45 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 13 Mar 2025 08:54:45 GMT
ADD file:f6d72fdda03fb8754d82331b1f726d49b6b7d2d850ad2d1dfc2de6e1b365251b in / 
# Thu, 13 Mar 2025 08:54:45 GMT
CMD ["/bin/bash"]
# Thu, 13 Mar 2025 08:54:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Mar 2025 08:54:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_VERSION=jdk-17.0.14+7_openj9-0.49.0
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f26b2b2d8654a09fade4c0ce5819e72e00f1e751bb11a4731537e834900c3282';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_aarch64_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='578a651e9e26de4ec30612afbd69c2530c8ed37db2c46bc62eb6a39dfa35c080';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_ppc64le_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='e2469f16a616ee467d6a590ec043ee9464b039d2f9859327dd36d50953cd60bf';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_x64_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='e96268d4daa6c5c2526f477ac563ef4851f0156ec67696fb855080704a5fd5c5';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_s390x_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
USER root
# Wed, 23 Apr 2025 12:52:37 GMT
ARG LIBERTY_VERSION=25.0.0.5-beta
# Wed, 23 Apr 2025 12:52:37 GMT
ARG LIBERTY_SHA=51a9331cbd038b2a1fb21ee6b2e45c69cedf9487
# Wed, 23 Apr 2025 12:52:37 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.5-beta/openliberty-runtime-25.0.0.5-beta.zip
# Wed, 23 Apr 2025 12:52:37 GMT
ARG LIBERTY_BUILD_LABEL=cl250420250407-1902
# Wed, 23 Apr 2025 12:52:37 GMT
ARG OPENJ9_SCC=true
# Wed, 23 Apr 2025 12:52:37 GMT
ARG VERBOSE=false
# Wed, 23 Apr 2025 12:52:37 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250420250407-1902 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=25.0.0.5-beta liberty.version=25.0.0.5-beta io.openliberty.version=25.0.0.5-beta
# Wed, 23 Apr 2025 12:52:37 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5-beta LIBERTY_SHA=51a9331cbd038b2a1fb21ee6b2e45c69cedf9487 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.5-beta/openliberty-runtime-25.0.0.5-beta.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5-beta LIBERTY_SHA=51a9331cbd038b2a1fb21ee6b2e45c69cedf9487 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.5-beta/openliberty-runtime-25.0.0.5-beta.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5-beta LIBERTY_SHA=51a9331cbd038b2a1fb21ee6b2e45c69cedf9487 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.5-beta/openliberty-runtime-25.0.0.5-beta.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5-beta LIBERTY_SHA=51a9331cbd038b2a1fb21ee6b2e45c69cedf9487 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.5-beta/openliberty-runtime-25.0.0.5-beta.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5-beta LIBERTY_SHA=51a9331cbd038b2a1fb21ee6b2e45c69cedf9487 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.5-beta/openliberty-runtime-25.0.0.5-beta.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 23 Apr 2025 12:52:37 GMT
USER 1001
# Wed, 23 Apr 2025 12:52:37 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 23 Apr 2025 12:52:37 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 23 Apr 2025 12:52:37 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:95ba4619a43d3f4f7f5ee2c8fbe313d19bb9c0e9ca5fa9efeb7b93f942dcf377`  
		Last Modified: Mon, 28 Apr 2025 10:44:03 GMT  
		Size: 34.4 MB (34443215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a64c9f5a72745f3bafe1231a1d79f060f125195fbcd3f510afac643f962e127`  
		Last Modified: Mon, 05 May 2025 16:55:41 GMT  
		Size: 12.9 MB (12893020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9677fdeccfd840c657a0c5ca3aedec08f8e081f57d3eb19db5b023f0b4fde11`  
		Last Modified: Mon, 05 May 2025 17:09:08 GMT  
		Size: 52.8 MB (52766896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbec2888281f0d01bc1fda642914961fe37b10e676c0891102ed29ac29ca743`  
		Last Modified: Mon, 05 May 2025 17:09:06 GMT  
		Size: 3.8 MB (3796640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c465616d8e5703ac347e66bcfb2944ea644fe85d176b942bfc122cbf699e9e6d`  
		Last Modified: Mon, 05 May 2025 19:44:28 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6272fd511399cd0e46bcfe1a7bf64e69d63fcd2295d523ea2bd2e6e4d536906b`  
		Last Modified: Mon, 05 May 2025 19:44:28 GMT  
		Size: 10.5 KB (10477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b081e5b39a592004b99bc2bff7225e5d134a49f555ba3477060fb336fbac4fa`  
		Last Modified: Mon, 05 May 2025 19:44:28 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc81bfad591a221f71fc007931942dc16f5b1b8cbf8f3d42f91fa15c15a8ece3`  
		Last Modified: Mon, 05 May 2025 19:44:29 GMT  
		Size: 36.5 KB (36499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e87ef2d785744ed2d02777164aed0a8d7ddeabbb7b0bf53b23cb6bf4e3b6158`  
		Last Modified: Mon, 05 May 2025 19:44:43 GMT  
		Size: 361.4 MB (361362514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63afe949d68be6eaf77ff7ab7b031ecd5d25c436a4e2fcfb7de643874958038`  
		Last Modified: Mon, 05 May 2025 19:44:29 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e05fae2cbf65cefc56d6875b61a761a3f02a73fce9688264da8d09031dff28`  
		Last Modified: Mon, 05 May 2025 19:44:30 GMT  
		Size: 11.9 KB (11853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b2894b8229876f2c086f59398ea05b65d2ad85aa52f5cb0242ef0cac4e88de`  
		Last Modified: Mon, 05 May 2025 19:44:30 GMT  
		Size: 12.1 MB (12076774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java17` - unknown; unknown

```console
$ docker pull open-liberty@sha256:6ee03ffbbf1f8e01c3a0c84e6edf5db5ac24bfbfa8754f06d4c963137be86320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5637450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce2efd61de3edbeba792320bba09f5f39427898357a7766971968b3aaeac3334`

```dockerfile
```

-	Layers:
	-	`sha256:3c4654a189f03b511d1c474b5e5505a9b89745f59e4dda0393bff07f468d6a01`  
		Last Modified: Mon, 05 May 2025 19:44:29 GMT  
		Size: 5.6 MB (5598580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf1e258da61cebb928b3c1e46079316994d91ba9ea42612cf01d685a87a539d8`  
		Last Modified: Mon, 05 May 2025 19:44:28 GMT  
		Size: 38.9 KB (38870 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta-java17` - linux; s390x

```console
$ docker pull open-liberty@sha256:96ded4213a5d86bb43c2125f18afa7539782811c9129bfccac82048af260dc2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **471.2 MB (471192709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676d7f66f42e29638a3dab2e287df9b743fb440be6a67eb0cbfcb957cb6be30a`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 13 Mar 2025 08:54:45 GMT
ARG RELEASE
# Thu, 13 Mar 2025 08:54:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Mar 2025 08:54:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Mar 2025 08:54:45 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 13 Mar 2025 08:54:45 GMT
ADD file:4be5dde78df6dfb2332aa60bf4714ecf19075f664a5fac89ff50019cbee5434d in / 
# Thu, 13 Mar 2025 08:54:45 GMT
CMD ["/bin/bash"]
# Thu, 13 Mar 2025 08:54:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Mar 2025 08:54:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_VERSION=jdk-17.0.14+7_openj9-0.49.0
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f26b2b2d8654a09fade4c0ce5819e72e00f1e751bb11a4731537e834900c3282';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_aarch64_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='578a651e9e26de4ec30612afbd69c2530c8ed37db2c46bc62eb6a39dfa35c080';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_ppc64le_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='e2469f16a616ee467d6a590ec043ee9464b039d2f9859327dd36d50953cd60bf';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_x64_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='e96268d4daa6c5c2526f477ac563ef4851f0156ec67696fb855080704a5fd5c5';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_s390x_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
USER root
# Wed, 23 Apr 2025 12:52:37 GMT
ARG LIBERTY_VERSION=25.0.0.5-beta
# Wed, 23 Apr 2025 12:52:37 GMT
ARG LIBERTY_SHA=51a9331cbd038b2a1fb21ee6b2e45c69cedf9487
# Wed, 23 Apr 2025 12:52:37 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.5-beta/openliberty-runtime-25.0.0.5-beta.zip
# Wed, 23 Apr 2025 12:52:37 GMT
ARG LIBERTY_BUILD_LABEL=cl250420250407-1902
# Wed, 23 Apr 2025 12:52:37 GMT
ARG OPENJ9_SCC=true
# Wed, 23 Apr 2025 12:52:37 GMT
ARG VERBOSE=false
# Wed, 23 Apr 2025 12:52:37 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250420250407-1902 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=25.0.0.5-beta liberty.version=25.0.0.5-beta io.openliberty.version=25.0.0.5-beta
# Wed, 23 Apr 2025 12:52:37 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5-beta LIBERTY_SHA=51a9331cbd038b2a1fb21ee6b2e45c69cedf9487 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.5-beta/openliberty-runtime-25.0.0.5-beta.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5-beta LIBERTY_SHA=51a9331cbd038b2a1fb21ee6b2e45c69cedf9487 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.5-beta/openliberty-runtime-25.0.0.5-beta.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5-beta LIBERTY_SHA=51a9331cbd038b2a1fb21ee6b2e45c69cedf9487 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.5-beta/openliberty-runtime-25.0.0.5-beta.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5-beta LIBERTY_SHA=51a9331cbd038b2a1fb21ee6b2e45c69cedf9487 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.5-beta/openliberty-runtime-25.0.0.5-beta.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5-beta LIBERTY_SHA=51a9331cbd038b2a1fb21ee6b2e45c69cedf9487 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.5-beta/openliberty-runtime-25.0.0.5-beta.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 23 Apr 2025 12:52:37 GMT
USER 1001
# Wed, 23 Apr 2025 12:52:37 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 23 Apr 2025 12:52:37 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 23 Apr 2025 12:52:37 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:64d717faaf8dba48ef4989d39eb6faef5fe680871a4064f1753d9cc21de5bc3c`  
		Last Modified: Mon, 28 Apr 2025 10:44:16 GMT  
		Size: 28.0 MB (27999984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573305c63c6b8034a976ad865f575e2879ba561788a75b917f925a7f6f45b358`  
		Last Modified: Mon, 05 May 2025 16:47:08 GMT  
		Size: 12.2 MB (12219201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150e1bd3f256bac3fd04c5a82f84852bc1c5aca99a3f0c02bed52977b5e6aa72`  
		Last Modified: Mon, 05 May 2025 16:59:31 GMT  
		Size: 50.6 MB (50552919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e93befd326802b4b155038790fcfecafd4dd0154ea2346980b4cb9ba89a6e5`  
		Last Modified: Mon, 05 May 2025 16:59:30 GMT  
		Size: 5.1 MB (5116929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34978599e11ab28a150074df3b70c683621018176de70ead7b48673746ee507b`  
		Last Modified: Mon, 05 May 2025 18:22:25 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054a7b8a2ca047063f2999a74f6da46652b31da607407cc386930e0f82ac23f0`  
		Last Modified: Mon, 05 May 2025 18:22:25 GMT  
		Size: 10.5 KB (10480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53939851ca89182912e723606058d3794a6d3f233eff0afa1963e7238de50771`  
		Last Modified: Mon, 05 May 2025 18:22:25 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ff32387e7344190ee1c27663c83a49f98619bb52f96f63eb53e19241b76584`  
		Last Modified: Mon, 05 May 2025 18:22:25 GMT  
		Size: 33.1 KB (33111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b81249c5262dbaeb01cb89263c24e3c1651df6fb9f82959d99af51e5eb0985`  
		Last Modified: Mon, 05 May 2025 18:22:32 GMT  
		Size: 361.4 MB (361361873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc5d31f95233d56ebbb266fa8b632ecd934558409cec482d9c61f1f15ba0e3d`  
		Last Modified: Mon, 05 May 2025 18:22:26 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099006fc471bab55133eba3df1803f979b613ae7332e5c92e09a813aa2a2887e`  
		Last Modified: Mon, 05 May 2025 18:22:26 GMT  
		Size: 11.8 KB (11840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a081837c0a51515ba7f054d3cfa9f1791a92ba51290cade73e2a1260703d1371`  
		Last Modified: Mon, 05 May 2025 18:22:28 GMT  
		Size: 13.9 MB (13884027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java17` - unknown; unknown

```console
$ docker pull open-liberty@sha256:217b566461085edb27d7d0d0c8450847bcf118932c5d95d3af4f3faab47bd063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5633950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a570a6a5d6e13468578a69e0cd867888d67a3516a2bb9b423ce425aac8ba2808`

```dockerfile
```

-	Layers:
	-	`sha256:4a2328bbb66a59c8da4d618abc7aaa31bd2a6f3d89d6f83eb1f22b1a5c614d6e`  
		Last Modified: Mon, 05 May 2025 18:22:25 GMT  
		Size: 5.6 MB (5595114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60413a3d6ae853cb73720f2e74582d65ceffe14e33a4c350642e02dd453bf289`  
		Last Modified: Mon, 05 May 2025 18:22:24 GMT  
		Size: 38.8 KB (38836 bytes)  
		MIME: application/vnd.in-toto+json
