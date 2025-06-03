## `open-liberty:full-java17-openj9`

```console
$ docker pull open-liberty@sha256:0424ddae6eb8f97068b486b6288e3b322eaea892eae9ecbfabfec82c0d6156bd
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
$ docker pull open-liberty@sha256:ea8186eb49356b79bb8163694a971d3d8f5745647cd1f9759045d202994b2e5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.1 MB (450095034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8fd00e951365a2429771cd0966f396bb92a5a238d6b7c3f2e2e886674c71b3`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
CMD ["/bin/bash"]
# Wed, 07 May 2025 17:42:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 07 May 2025 17:42:21 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_VERSION=jdk-17.0.15+6_openj9-0.51.0
# Wed, 07 May 2025 17:42:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9a44da58055525719ddb87b2fe21a02562a0897b8b537a65b7a94b1ab28f7eb0';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e852a334a4a3f59bd8478ffe3190bbdb520fa37d8954e17fc7842ede979b15fa';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c4cc045bfd63fc6412251fef184c91a1acad76d74ee48561fd48c174fb1278d3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='6e1afeea17e8d9538bf65c0672482e3813f13a7d61ee74ad75b2372225df53ba';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 07 May 2025 17:42:21 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 21 May 2025 02:47:31 GMT
USER root
# Wed, 21 May 2025 02:47:31 GMT
ARG LIBERTY_VERSION=25.0.0.5
# Wed, 21 May 2025 02:47:31 GMT
ARG LIBERTY_SHA=fe82f9735584b01e9cfbf1eb71ce5eef479beecb
# Wed, 21 May 2025 02:47:31 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.5/openliberty-runtime-25.0.0.5.zip
# Wed, 21 May 2025 02:47:31 GMT
ARG LIBERTY_BUILD_LABEL=cl250520250504-1901
# Wed, 21 May 2025 02:47:31 GMT
ARG OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:31 GMT
ARG VERBOSE=false
# Wed, 21 May 2025 02:47:31 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250520250504-1901 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.5 liberty.version=25.0.0.5 io.openliberty.version=25.0.0.5
# Wed, 21 May 2025 02:47:31 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 21 May 2025 02:47:31 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 21 May 2025 02:47:31 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 21 May 2025 02:47:31 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5 LIBERTY_SHA=fe82f9735584b01e9cfbf1eb71ce5eef479beecb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.5/openliberty-runtime-25.0.0.5.zip LIBERTY_BUILD_LABEL=cl250520250504-1901 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 21 May 2025 02:47:31 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5 LIBERTY_SHA=fe82f9735584b01e9cfbf1eb71ce5eef479beecb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.5/openliberty-runtime-25.0.0.5.zip LIBERTY_BUILD_LABEL=cl250520250504-1901 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 21 May 2025 02:47:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:31 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5 LIBERTY_SHA=fe82f9735584b01e9cfbf1eb71ce5eef479beecb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.5/openliberty-runtime-25.0.0.5.zip LIBERTY_BUILD_LABEL=cl250520250504-1901 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 21 May 2025 02:47:31 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5 LIBERTY_SHA=fe82f9735584b01e9cfbf1eb71ce5eef479beecb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.5/openliberty-runtime-25.0.0.5.zip LIBERTY_BUILD_LABEL=cl250520250504-1901 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Wed, 21 May 2025 02:47:31 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5 LIBERTY_SHA=fe82f9735584b01e9cfbf1eb71ce5eef479beecb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.5/openliberty-runtime-25.0.0.5.zip LIBERTY_BUILD_LABEL=cl250520250504-1901 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 21 May 2025 02:47:31 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 21 May 2025 02:47:31 GMT
USER 1001
# Wed, 21 May 2025 02:47:31 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 21 May 2025 02:47:31 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 21 May 2025 02:47:31 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f177f5db89270b070e1644af124a467a0c875ee09cfc1fa9239b72eea64c0c`  
		Last Modified: Fri, 09 May 2025 16:44:19 GMT  
		Size: 12.2 MB (12172112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f688483665c04fc1d231ea5dbc2ea70ccbc9c8d122bfc6b7e099fb087cf466b2`  
		Last Modified: Fri, 09 May 2025 16:44:25 GMT  
		Size: 51.7 MB (51747279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b08cf00ef33c315cf466a143b8b007197e30ed1139cf5830bea6d5c390206b`  
		Last Modified: Fri, 09 May 2025 16:44:18 GMT  
		Size: 5.0 MB (4978829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc69627c0303734e6966c3b5156450293e25733f3fa0fcd06945ea411b914fe`  
		Last Modified: Wed, 21 May 2025 17:37:19 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6790e54b9165388c869ce966daecd8e4bac5ae4395a2ee604cbb922a711ba392`  
		Last Modified: Wed, 21 May 2025 17:38:15 GMT  
		Size: 10.5 KB (10481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163448fef28e8b264433b1d1d69a520689fb01ba67d83c10cfbcc104b80dd975`  
		Last Modified: Wed, 21 May 2025 17:37:19 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56001bafdc26ff961cfcc3dd59d25e7142c46ac0654205402ca3496c116285f4`  
		Last Modified: Wed, 21 May 2025 17:37:19 GMT  
		Size: 31.7 KB (31747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac657f65345bf489f23e4eeb4c5e0f21914445418ff61e3ffb5faa25a7335e10`  
		Last Modified: Wed, 21 May 2025 17:38:21 GMT  
		Size: 337.3 MB (337254034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e303229485478dbc6996e3050f72c21b0c37d699d5276fae42cafe25172b7c7`  
		Last Modified: Wed, 21 May 2025 17:38:16 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc456b73eb888f5125bc79e13fbe57bf053fb6d7519f60f035519488bc1f3ca`  
		Last Modified: Wed, 21 May 2025 17:38:16 GMT  
		Size: 11.8 KB (11844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877479881456764fd1a2df4388ec7c22d0c437e17bc6cf4fc808035e29d17c0f`  
		Last Modified: Wed, 21 May 2025 17:38:19 GMT  
		Size: 14.4 MB (14353747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:75fa9f8a7586bf5a32ce59e48b2fcfed80cc2ad6b4f6008f60081af948e00fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5597570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e33aa40ffe17a134eab875ce30c870fbb67657c5f31d0deb59f19e29c7dbaef`

```dockerfile
```

-	Layers:
	-	`sha256:b7bbc03ba1c3fdddf5d45987d428a69ae11fea4cca23e74643db31b39e886c18`  
		Last Modified: Wed, 21 May 2025 17:38:16 GMT  
		Size: 5.6 MB (5558857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e76a94a7b51c086ef63dfc4660844bb08a1290fbfd4b2f0c7b38a86a054e966`  
		Last Modified: Wed, 21 May 2025 17:38:15 GMT  
		Size: 38.7 KB (38713 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java17-openj9` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:14254140b05ba04f8b219ecd4ac96090925d47434d18fb1ccabdc0fe47c2d218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **443.0 MB (443041019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41bc0539a273585c695a8b2e0d7c231d8c6ae034e9d5b6abef9f4d968deac299`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 28 Apr 2025 09:46:27 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:46:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:46:30 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 28 Apr 2025 09:46:30 GMT
CMD ["/bin/bash"]
# Wed, 07 May 2025 17:42:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 07 May 2025 17:42:21 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_VERSION=jdk-17.0.15+6_openj9-0.51.0
# Wed, 07 May 2025 17:42:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9a44da58055525719ddb87b2fe21a02562a0897b8b537a65b7a94b1ab28f7eb0';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e852a334a4a3f59bd8478ffe3190bbdb520fa37d8954e17fc7842ede979b15fa';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c4cc045bfd63fc6412251fef184c91a1acad76d74ee48561fd48c174fb1278d3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='6e1afeea17e8d9538bf65c0672482e3813f13a7d61ee74ad75b2372225df53ba';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 07 May 2025 17:42:21 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 21 May 2025 02:47:31 GMT
USER root
# Wed, 21 May 2025 02:47:31 GMT
ARG LIBERTY_VERSION=25.0.0.5
# Wed, 21 May 2025 02:47:31 GMT
ARG LIBERTY_SHA=fe82f9735584b01e9cfbf1eb71ce5eef479beecb
# Wed, 21 May 2025 02:47:31 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.5/openliberty-runtime-25.0.0.5.zip
# Wed, 21 May 2025 02:47:31 GMT
ARG LIBERTY_BUILD_LABEL=cl250520250504-1901
# Wed, 21 May 2025 02:47:31 GMT
ARG OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:31 GMT
ARG VERBOSE=false
# Wed, 21 May 2025 02:47:31 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250520250504-1901 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.5 liberty.version=25.0.0.5 io.openliberty.version=25.0.0.5
# Wed, 21 May 2025 02:47:31 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 21 May 2025 02:47:31 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 21 May 2025 02:47:31 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 21 May 2025 02:47:31 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5 LIBERTY_SHA=fe82f9735584b01e9cfbf1eb71ce5eef479beecb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.5/openliberty-runtime-25.0.0.5.zip LIBERTY_BUILD_LABEL=cl250520250504-1901 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 21 May 2025 02:47:31 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5 LIBERTY_SHA=fe82f9735584b01e9cfbf1eb71ce5eef479beecb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.5/openliberty-runtime-25.0.0.5.zip LIBERTY_BUILD_LABEL=cl250520250504-1901 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 21 May 2025 02:47:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:31 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5 LIBERTY_SHA=fe82f9735584b01e9cfbf1eb71ce5eef479beecb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.5/openliberty-runtime-25.0.0.5.zip LIBERTY_BUILD_LABEL=cl250520250504-1901 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 21 May 2025 02:47:31 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5 LIBERTY_SHA=fe82f9735584b01e9cfbf1eb71ce5eef479beecb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.5/openliberty-runtime-25.0.0.5.zip LIBERTY_BUILD_LABEL=cl250520250504-1901 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Wed, 21 May 2025 02:47:31 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5 LIBERTY_SHA=fe82f9735584b01e9cfbf1eb71ce5eef479beecb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.5/openliberty-runtime-25.0.0.5.zip LIBERTY_BUILD_LABEL=cl250520250504-1901 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 21 May 2025 02:47:31 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 21 May 2025 02:47:31 GMT
USER 1001
# Wed, 21 May 2025 02:47:31 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 21 May 2025 02:47:31 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 21 May 2025 02:47:31 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78892370879d09e257e1f423fb01169148aa714423fd175a7a3f0933ae6673e`  
		Last Modified: Thu, 08 May 2025 17:57:19 GMT  
		Size: 12.1 MB (12129417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87dacafeafdeb88805872487016c74fd9df84de6f2f46dc3979ebbbf50389bf4`  
		Last Modified: Fri, 09 May 2025 17:01:24 GMT  
		Size: 48.2 MB (48190754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94a0d837c9514d458b3301307a2a14be1df802d94a9f125d286ae35ed868894`  
		Last Modified: Fri, 09 May 2025 17:01:12 GMT  
		Size: 4.8 MB (4759116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb54fa7f17369ddbf289c5bb326822dfb1c05f894a8f639458438001e2e9f953`  
		Last Modified: Fri, 09 May 2025 17:14:11 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0142c009df68b55029ab07336a8a9b5e7977a1cf22a27cc4f9c462400896e805`  
		Last Modified: Fri, 09 May 2025 17:14:11 GMT  
		Size: 10.5 KB (10482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c670c22b7a562692d167e26c14909b0d742b8fc18cc35f2bace8eadd980552c`  
		Last Modified: Fri, 09 May 2025 17:14:12 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62620eccd93258173a3c2efa3e1525c3579d8ec4c8bc7866144d711be808e3c0`  
		Last Modified: Wed, 21 May 2025 17:47:21 GMT  
		Size: 42.3 KB (42327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46a9aeb81fa906d1e4020594d19ea184bb4da0d493c02b66ed6dbafd601234b`  
		Last Modified: Wed, 21 May 2025 17:47:29 GMT  
		Size: 337.3 MB (337254028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddd8d1d28eb9b6344a870c41d77793bd9ef5017d4e18a9549c2b7ca6236412b`  
		Last Modified: Wed, 21 May 2025 17:47:21 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357f06e1e1c4205ea4b76dd7584765264cbe6fdd74fe8436fccdb64943c0860e`  
		Last Modified: Wed, 21 May 2025 17:47:21 GMT  
		Size: 11.9 KB (11857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f81dc982b124605ce4ec97414b746111ffd11bb9650a83f6afb7a67371333b`  
		Last Modified: Wed, 21 May 2025 17:47:23 GMT  
		Size: 13.3 MB (13286477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:4570238c847a2f832cc6937fab6e145a8fa7540e283a7a6476eb04bec9cbc70f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5591033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869f619cbd1bb6708ce81ac0a15b689c0a0a2504247b5a2abecbe3d45ea08362`

```dockerfile
```

-	Layers:
	-	`sha256:ee206a96a85861e85754bab2be2389f88abb7d0399abdacf8e12345979622526`  
		Last Modified: Wed, 21 May 2025 17:47:22 GMT  
		Size: 5.6 MB (5552191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:389c3e5f285b4eaf433e9e520899380e203527c0c939224d720f6939d1e811b2`  
		Last Modified: Wed, 21 May 2025 17:47:21 GMT  
		Size: 38.8 KB (38842 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java17-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:a87c2c6bf1103a1594007441b0e6b1a030da7b29df8dac5928c297de939d23bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.8 MB (453846682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de50ad4914f27a73ed848658ae9f3542847074839024e8b0ca33d9269361fca`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 28 Apr 2025 09:45:54 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:45:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:45:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:45:58 GMT
ADD file:f6d72fdda03fb8754d82331b1f726d49b6b7d2d850ad2d1dfc2de6e1b365251b in / 
# Mon, 28 Apr 2025 09:45:59 GMT
CMD ["/bin/bash"]
# Wed, 07 May 2025 17:42:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 07 May 2025 17:42:21 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_VERSION=jdk-17.0.15+6_openj9-0.51.0
# Wed, 07 May 2025 17:42:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9a44da58055525719ddb87b2fe21a02562a0897b8b537a65b7a94b1ab28f7eb0';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e852a334a4a3f59bd8478ffe3190bbdb520fa37d8954e17fc7842ede979b15fa';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c4cc045bfd63fc6412251fef184c91a1acad76d74ee48561fd48c174fb1278d3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='6e1afeea17e8d9538bf65c0672482e3813f13a7d61ee74ad75b2372225df53ba';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 07 May 2025 17:42:21 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 21 May 2025 02:47:31 GMT
USER root
# Wed, 21 May 2025 02:47:31 GMT
ARG LIBERTY_VERSION=25.0.0.5
# Wed, 21 May 2025 02:47:31 GMT
ARG LIBERTY_SHA=fe82f9735584b01e9cfbf1eb71ce5eef479beecb
# Wed, 21 May 2025 02:47:31 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.5/openliberty-runtime-25.0.0.5.zip
# Wed, 21 May 2025 02:47:31 GMT
ARG LIBERTY_BUILD_LABEL=cl250520250504-1901
# Wed, 21 May 2025 02:47:31 GMT
ARG OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:31 GMT
ARG VERBOSE=false
# Wed, 21 May 2025 02:47:31 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250520250504-1901 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.5 liberty.version=25.0.0.5 io.openliberty.version=25.0.0.5
# Wed, 21 May 2025 02:47:31 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 21 May 2025 02:47:31 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 21 May 2025 02:47:31 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 21 May 2025 02:47:31 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5 LIBERTY_SHA=fe82f9735584b01e9cfbf1eb71ce5eef479beecb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.5/openliberty-runtime-25.0.0.5.zip LIBERTY_BUILD_LABEL=cl250520250504-1901 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 21 May 2025 02:47:31 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5 LIBERTY_SHA=fe82f9735584b01e9cfbf1eb71ce5eef479beecb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.5/openliberty-runtime-25.0.0.5.zip LIBERTY_BUILD_LABEL=cl250520250504-1901 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 21 May 2025 02:47:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:31 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5 LIBERTY_SHA=fe82f9735584b01e9cfbf1eb71ce5eef479beecb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.5/openliberty-runtime-25.0.0.5.zip LIBERTY_BUILD_LABEL=cl250520250504-1901 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 21 May 2025 02:47:31 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5 LIBERTY_SHA=fe82f9735584b01e9cfbf1eb71ce5eef479beecb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.5/openliberty-runtime-25.0.0.5.zip LIBERTY_BUILD_LABEL=cl250520250504-1901 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Wed, 21 May 2025 02:47:31 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5 LIBERTY_SHA=fe82f9735584b01e9cfbf1eb71ce5eef479beecb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.5/openliberty-runtime-25.0.0.5.zip LIBERTY_BUILD_LABEL=cl250520250504-1901 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 21 May 2025 02:47:31 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 21 May 2025 02:47:31 GMT
USER 1001
# Wed, 21 May 2025 02:47:31 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 21 May 2025 02:47:31 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 21 May 2025 02:47:31 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:95ba4619a43d3f4f7f5ee2c8fbe313d19bb9c0e9ca5fa9efeb7b93f942dcf377`  
		Last Modified: Thu, 08 May 2025 17:15:30 GMT  
		Size: 34.4 MB (34443215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a64c9f5a72745f3bafe1231a1d79f060f125195fbcd3f510afac643f962e127`  
		Last Modified: Fri, 09 May 2025 09:51:07 GMT  
		Size: 12.9 MB (12893020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190e6ee8a32dac2fb076f7645a0a113debd4b90af043fc447fe5e6e1c8d31868`  
		Last Modified: Fri, 09 May 2025 17:12:00 GMT  
		Size: 53.4 MB (53352875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd62acbf6795d22ba91011f6f0cf82c1f69a670578ca56391061054ea0aa2f41`  
		Last Modified: Fri, 09 May 2025 17:11:55 GMT  
		Size: 3.8 MB (3838355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc6fafdf71d3eb05870a3064c62f517438abe522a228d2b44a7ac4964ebc7b3`  
		Last Modified: Fri, 09 May 2025 18:13:51 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb94a708df261ed0d4ca6f944cea673c3096117ac58b0fad3ee62d87b799522`  
		Last Modified: Fri, 09 May 2025 18:13:51 GMT  
		Size: 10.5 KB (10479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185cdc52da9c8f8f7cadcf33a8de5c43d4d3e35001e786a94715d711cab839e2`  
		Last Modified: Fri, 09 May 2025 18:13:51 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f6b869863199e417dacbe4fd28257dbdd93fd55da9a5306195b5d524541a4e`  
		Last Modified: Wed, 21 May 2025 17:57:04 GMT  
		Size: 36.5 KB (36500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed07ae27f72046bf8ec408d42c5d058dff3a9fa0b79dbcb30f4f4d1d8dd0e69`  
		Last Modified: Wed, 21 May 2025 17:57:17 GMT  
		Size: 337.3 MB (337254213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ee9a1dd34ac032faaf2726c6c20880504d4a99976b64f786ee81cc4e93d201`  
		Last Modified: Wed, 21 May 2025 17:57:04 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c565dce587529fdb3abfddf6262fd4461a3fbacf99411e5c65540b32dee299c`  
		Last Modified: Wed, 21 May 2025 17:57:04 GMT  
		Size: 11.9 KB (11874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf40d812dbf52cbb9555f845baf73ee2d4c5037740d39eb922fcb806eb15b47`  
		Last Modified: Wed, 21 May 2025 17:57:06 GMT  
		Size: 12.0 MB (12003797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:9b3b42afe92880b782c7fd1de8f53ff066aba2139aae745ae56f9d966e023c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5602225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd409c98bc5134c3054f0d07db6d9b29bb824f707bbf3a0118a469f2b05460d6`

```dockerfile
```

-	Layers:
	-	`sha256:12173eca12c84fe67a175b0d10f3442b203bdf30c6d0cbafb8d49fe5e82c7640`  
		Last Modified: Wed, 21 May 2025 17:57:05 GMT  
		Size: 5.6 MB (5563478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1e60a6fe6dfc3ed1a06ff87362096047d9073c93aa93bb15b61b71acfbc461a`  
		Last Modified: Wed, 21 May 2025 17:57:04 GMT  
		Size: 38.7 KB (38747 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java17-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:06ebea2c2595d67b61af01af46872a485f116a0f5eb1c40e5e6f2d843843437d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.9 MB (447902335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277c6b1cf76efd1ffe314e86457e347a785b58ef742f6b38eb9d9bbcad428012`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 28 Apr 2025 09:45:02 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:45:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:45:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:45:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:45:04 GMT
ADD file:4be5dde78df6dfb2332aa60bf4714ecf19075f664a5fac89ff50019cbee5434d in / 
# Mon, 28 Apr 2025 09:45:04 GMT
CMD ["/bin/bash"]
# Wed, 07 May 2025 17:42:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 07 May 2025 17:42:21 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_VERSION=jdk-17.0.15+6_openj9-0.51.0
# Wed, 07 May 2025 17:42:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9a44da58055525719ddb87b2fe21a02562a0897b8b537a65b7a94b1ab28f7eb0';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e852a334a4a3f59bd8478ffe3190bbdb520fa37d8954e17fc7842ede979b15fa';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c4cc045bfd63fc6412251fef184c91a1acad76d74ee48561fd48c174fb1278d3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='6e1afeea17e8d9538bf65c0672482e3813f13a7d61ee74ad75b2372225df53ba';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 07 May 2025 17:42:21 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 21 May 2025 02:47:31 GMT
USER root
# Wed, 21 May 2025 02:47:31 GMT
ARG LIBERTY_VERSION=25.0.0.5
# Wed, 21 May 2025 02:47:31 GMT
ARG LIBERTY_SHA=fe82f9735584b01e9cfbf1eb71ce5eef479beecb
# Wed, 21 May 2025 02:47:31 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.5/openliberty-runtime-25.0.0.5.zip
# Wed, 21 May 2025 02:47:31 GMT
ARG LIBERTY_BUILD_LABEL=cl250520250504-1901
# Wed, 21 May 2025 02:47:31 GMT
ARG OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:31 GMT
ARG VERBOSE=false
# Wed, 21 May 2025 02:47:31 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250520250504-1901 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.5 liberty.version=25.0.0.5 io.openliberty.version=25.0.0.5
# Wed, 21 May 2025 02:47:31 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 21 May 2025 02:47:31 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 21 May 2025 02:47:31 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 21 May 2025 02:47:31 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5 LIBERTY_SHA=fe82f9735584b01e9cfbf1eb71ce5eef479beecb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.5/openliberty-runtime-25.0.0.5.zip LIBERTY_BUILD_LABEL=cl250520250504-1901 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 21 May 2025 02:47:31 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5 LIBERTY_SHA=fe82f9735584b01e9cfbf1eb71ce5eef479beecb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.5/openliberty-runtime-25.0.0.5.zip LIBERTY_BUILD_LABEL=cl250520250504-1901 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 21 May 2025 02:47:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:31 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5 LIBERTY_SHA=fe82f9735584b01e9cfbf1eb71ce5eef479beecb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.5/openliberty-runtime-25.0.0.5.zip LIBERTY_BUILD_LABEL=cl250520250504-1901 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 21 May 2025 02:47:31 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5 LIBERTY_SHA=fe82f9735584b01e9cfbf1eb71ce5eef479beecb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.5/openliberty-runtime-25.0.0.5.zip LIBERTY_BUILD_LABEL=cl250520250504-1901 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Wed, 21 May 2025 02:47:31 GMT
# ARGS: LIBERTY_VERSION=25.0.0.5 LIBERTY_SHA=fe82f9735584b01e9cfbf1eb71ce5eef479beecb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.5/openliberty-runtime-25.0.0.5.zip LIBERTY_BUILD_LABEL=cl250520250504-1901 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 21 May 2025 02:47:31 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 21 May 2025 02:47:31 GMT
USER 1001
# Wed, 21 May 2025 02:47:31 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 21 May 2025 02:47:31 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 21 May 2025 02:47:31 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:64d717faaf8dba48ef4989d39eb6faef5fe680871a4064f1753d9cc21de5bc3c`  
		Last Modified: Thu, 08 May 2025 17:06:03 GMT  
		Size: 28.0 MB (27999984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573305c63c6b8034a976ad865f575e2879ba561788a75b917f925a7f6f45b358`  
		Last Modified: Fri, 09 May 2025 07:53:46 GMT  
		Size: 12.2 MB (12219201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c722eb1e516a736ab709561aaa1b82a951c0d4904e0d46a859b928acffa44a`  
		Last Modified: Fri, 09 May 2025 17:06:04 GMT  
		Size: 51.1 MB (51093317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670c467b8956cc0ad8f37d6a013e09e17d8d05f76375bb59636f4848010d0197`  
		Last Modified: Fri, 09 May 2025 17:05:52 GMT  
		Size: 5.2 MB (5177039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc0becdd23f629eb9105449831938e39f16c11dc939db1cde04518ab54ffc86`  
		Last Modified: Fri, 09 May 2025 18:31:00 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f06880355395f0e7f343ed12ed2f7a1d0b8705f58e6863be5421ee2a6735fc`  
		Last Modified: Fri, 09 May 2025 18:31:01 GMT  
		Size: 10.5 KB (10485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc4170dda2c9ee1a942b12569c914b684306948a05c22180b3b658d8dd5e411`  
		Last Modified: Fri, 09 May 2025 18:31:01 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c614651763cb11a29a0818ccfe531a7dd3f828f7914484d88dfa1b6cf94a5560`  
		Last Modified: Wed, 21 May 2025 18:01:35 GMT  
		Size: 33.1 KB (33115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f168c7f37e540dadd2dd972c74d6feb6648bca0ef095b4225e3e7c93240c56`  
		Last Modified: Wed, 21 May 2025 18:01:40 GMT  
		Size: 337.3 MB (337253598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014d1c460f1bddf98b0648f5068fe37178e2396c4ceecb2c10fa015bdd8adf44`  
		Last Modified: Wed, 21 May 2025 18:01:35 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73142d245e1dab0ddff652f02750ecf1563772827fc522b8a4ffccff4f8d4f58`  
		Last Modified: Wed, 21 May 2025 18:01:35 GMT  
		Size: 11.9 KB (11858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2b6aacc5e160a6faa81552ca366515da8a8fc037362e67c5fa1a203cd5e96d`  
		Last Modified: Wed, 21 May 2025 18:01:38 GMT  
		Size: 14.1 MB (14101389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:a0e9e58b7570346ae48c59d9ddf83291783a7e934bbe127c5dc1e17436906c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c3de4b9a1f84b7196e424ef0be0d59962332a29d13a54b58233dc04100f182`

```dockerfile
```

-	Layers:
	-	`sha256:a726d288c7be3f9d7cd095bd87e03ccf9fb532fb5a6328dc779ff66ae234febd`  
		Last Modified: Wed, 21 May 2025 18:01:35 GMT  
		Size: 5.6 MB (5559874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cb1548e1318fc97bda62b527334ea15f50aefb1fa36f3720e34cf3cc0ba2655`  
		Last Modified: Wed, 21 May 2025 18:01:35 GMT  
		Size: 38.7 KB (38714 bytes)  
		MIME: application/vnd.in-toto+json
