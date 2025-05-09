## `open-liberty:full-java11-openj9`

```console
$ docker pull open-liberty@sha256:716ffa189c783dae8b6b4ab5cb9de4f350b1a460f6cb2aed59e7204ad9a925b0
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
$ docker pull open-liberty@sha256:bb21622e6a7dad7cb315fd3fddc4effddbfae61414a202b9e03599696c04627a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.1 MB (450057084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fefc1bf3e0f79c884b0029ebd6887b4279579ad7b3dde85c64f41dcb549e2aa2`
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
ENV JAVA_VERSION=jdk-11.0.27+6_openj9-0.51.0
# Wed, 23 Apr 2025 12:52:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7aa093df03eb825d62a72a64a60e238e9fde2d36ed18f6e5418e07318ad155a2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='81c7c9ee709939cc66d5122f096cd36a4d1630851d275881799746b8f9d050da';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='73b79ace5c4e01cf5b0c002799185a5db4a601b3158c690cb204e3b618ad7b6e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='1225935c404b2d3f788da9c7df81250a4519a3eb8b7fc39ddc8efe5845a02051';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 12:52:37 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 23 Apr 2025 12:52:37 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
USER root
# Wed, 23 Apr 2025 12:52:37 GMT
ARG LIBERTY_VERSION=25.0.0.4
# Wed, 23 Apr 2025 12:52:37 GMT
ARG LIBERTY_SHA=719ffc20a113a68f88dea0295fc366606a4c6028
# Wed, 23 Apr 2025 12:52:37 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.4/openliberty-runtime-25.0.0.4.zip
# Wed, 23 Apr 2025 12:52:37 GMT
ARG LIBERTY_BUILD_LABEL=cl250420250407-1902
# Wed, 23 Apr 2025 12:52:37 GMT
ARG OPENJ9_SCC=true
# Wed, 23 Apr 2025 12:52:37 GMT
ARG VERBOSE=false
# Wed, 23 Apr 2025 12:52:37 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250420250407-1902 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.4 liberty.version=25.0.0.4 io.openliberty.version=25.0.0.4
# Wed, 23 Apr 2025 12:52:37 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4 LIBERTY_SHA=719ffc20a113a68f88dea0295fc366606a4c6028 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.4/openliberty-runtime-25.0.0.4.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4 LIBERTY_SHA=719ffc20a113a68f88dea0295fc366606a4c6028 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.4/openliberty-runtime-25.0.0.4.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4 LIBERTY_SHA=719ffc20a113a68f88dea0295fc366606a4c6028 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.4/openliberty-runtime-25.0.0.4.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4 LIBERTY_SHA=719ffc20a113a68f88dea0295fc366606a4c6028 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.4/openliberty-runtime-25.0.0.4.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4 LIBERTY_SHA=719ffc20a113a68f88dea0295fc366606a4c6028 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.4/openliberty-runtime-25.0.0.4.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
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
	-	`sha256:e1aba4a94830318865573d0e54fdd738096d9fb1f25b59503c7dfbe9b8cd28e9`  
		Last Modified: Fri, 09 May 2025 16:43:49 GMT  
		Size: 12.2 MB (12172136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22da1132c6ae2a163c075a21e0e3d0161f38ed1fd9d2550b2c0ce958430920f5`  
		Last Modified: Fri, 09 May 2025 16:43:51 GMT  
		Size: 52.5 MB (52455999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b90c1a3e099b20a67ae2096d380f50ac8e1856cd2ce472d3834b1b160350dac`  
		Last Modified: Fri, 09 May 2025 16:43:49 GMT  
		Size: 4.5 MB (4466313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc8951e811b86b2e91f12e9e5b876af532562061b410a146fb9ff9f2c4aa3a7`  
		Last Modified: Fri, 09 May 2025 17:09:14 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c182ec1e59810356de3b6a67c3c6cea944945473315f4983aea733873b9393a9`  
		Last Modified: Fri, 09 May 2025 17:09:14 GMT  
		Size: 10.5 KB (10484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae330c8afec65c2bae8e5099e4d86447044ca976aa903207c2cfc3bf0770919`  
		Last Modified: Fri, 09 May 2025 17:09:14 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8307371204b58502483ad563bf3ca8ff7abb486149af58c1ba6e0cee61a83a`  
		Last Modified: Fri, 09 May 2025 17:08:20 GMT  
		Size: 31.7 KB (31746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c8df14eed9c371f27dd7b38a3b5697d97e4e4dc6e48f1959943eafffc32b12`  
		Last Modified: Fri, 09 May 2025 17:09:22 GMT  
		Size: 337.5 MB (337486619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929dc0c86fb6793c9bc5745b9e74623be2f07ad79e564780fe1432f007b8444c`  
		Last Modified: Fri, 09 May 2025 17:09:15 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c51cae3003737058f3e9e162c467979173ae9b3209b7bb531d768b6e5b9c78`  
		Last Modified: Fri, 09 May 2025 17:09:15 GMT  
		Size: 11.8 KB (11845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7534ba8ce4ba5913dae3eb358d42bcb97c962c5f0c5dcd1246686e075ebffa4f`  
		Last Modified: Fri, 09 May 2025 17:09:16 GMT  
		Size: 13.9 MB (13886980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:e795508ddf6a67b326879ef4a821b9f8fc26186d4dd0f6ccb714cd9f648c7958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5567008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544292ce4fae92854a2d3a4b31c52139803b40756c8fd87d6123e2535c825add`

```dockerfile
```

-	Layers:
	-	`sha256:b5fcf0f14d35ca7f82e476764d2432754c00d8c41fd13889cdbe260c86d289c0`  
		Last Modified: Fri, 09 May 2025 17:09:14 GMT  
		Size: 5.5 MB (5528294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1ade18ea5373718a84ab51c53d6869d459690f7ee1da71a3545067db8069b85`  
		Last Modified: Fri, 09 May 2025 17:09:13 GMT  
		Size: 38.7 KB (38714 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java11-openj9` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:eb8a78bf8f9126b3200087249da0824edda8d7bcaaa6001489cd858b796cf0dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **443.4 MB (443387618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5235815a0aba59f03ebe302830f7c4f83d9faf804cc42f3b86654df1564f4f`
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
ENV JAVA_VERSION=jdk-11.0.27+6_openj9-0.51.0
# Wed, 23 Apr 2025 12:52:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7aa093df03eb825d62a72a64a60e238e9fde2d36ed18f6e5418e07318ad155a2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='81c7c9ee709939cc66d5122f096cd36a4d1630851d275881799746b8f9d050da';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='73b79ace5c4e01cf5b0c002799185a5db4a601b3158c690cb204e3b618ad7b6e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='1225935c404b2d3f788da9c7df81250a4519a3eb8b7fc39ddc8efe5845a02051';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 12:52:37 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 23 Apr 2025 12:52:37 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
USER root
# Wed, 23 Apr 2025 12:52:37 GMT
ARG LIBERTY_VERSION=25.0.0.4
# Wed, 23 Apr 2025 12:52:37 GMT
ARG LIBERTY_SHA=719ffc20a113a68f88dea0295fc366606a4c6028
# Wed, 23 Apr 2025 12:52:37 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.4/openliberty-runtime-25.0.0.4.zip
# Wed, 23 Apr 2025 12:52:37 GMT
ARG LIBERTY_BUILD_LABEL=cl250420250407-1902
# Wed, 23 Apr 2025 12:52:37 GMT
ARG OPENJ9_SCC=true
# Wed, 23 Apr 2025 12:52:37 GMT
ARG VERBOSE=false
# Wed, 23 Apr 2025 12:52:37 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250420250407-1902 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.4 liberty.version=25.0.0.4 io.openliberty.version=25.0.0.4
# Wed, 23 Apr 2025 12:52:37 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4 LIBERTY_SHA=719ffc20a113a68f88dea0295fc366606a4c6028 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.4/openliberty-runtime-25.0.0.4.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4 LIBERTY_SHA=719ffc20a113a68f88dea0295fc366606a4c6028 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.4/openliberty-runtime-25.0.0.4.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4 LIBERTY_SHA=719ffc20a113a68f88dea0295fc366606a4c6028 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.4/openliberty-runtime-25.0.0.4.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4 LIBERTY_SHA=719ffc20a113a68f88dea0295fc366606a4c6028 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.4/openliberty-runtime-25.0.0.4.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4 LIBERTY_SHA=719ffc20a113a68f88dea0295fc366606a4c6028 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.4/openliberty-runtime-25.0.0.4.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
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
	-	`sha256:8ac61e1105185e15d0582c5260aeba5bbfaa3b95b8b650d56029725f4a55df82`  
		Last Modified: Fri, 09 May 2025 16:54:25 GMT  
		Size: 48.9 MB (48888727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42089243838a6d937791f1e97d65589176852b83c8876aadb53b43e379125092`  
		Last Modified: Fri, 09 May 2025 16:54:23 GMT  
		Size: 4.2 MB (4199269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2ad7241e7fe1c4c047d87ca3d4def57e3c28043c8796528230fd50c499f0d4`  
		Last Modified: Fri, 09 May 2025 17:12:15 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a620e1732dc76701a0dc1c0fdbf81c5bd776731d37bcff3c4e6fc118af225377`  
		Last Modified: Fri, 09 May 2025 17:12:15 GMT  
		Size: 10.5 KB (10482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4022889fbfd4e5e1f0af3e29d51ee0e8a61dfe7e6dd827f150a8a61d4d07ef7`  
		Last Modified: Fri, 09 May 2025 17:12:15 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07495ac8d5eb23f22a61e5f1584ae6377cfcf47bfdb49c36f1542650e552169f`  
		Last Modified: Fri, 09 May 2025 17:18:41 GMT  
		Size: 42.3 KB (42327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5764e23cc143365dc65243107d289351be1e5267ec48a59162a1270d057bbccf`  
		Last Modified: Fri, 09 May 2025 17:18:49 GMT  
		Size: 337.5 MB (337486574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32f41f16273589c5c703ec107faee0aef50a7ee24c71259c35a46435c837c7b`  
		Last Modified: Fri, 09 May 2025 17:18:41 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d5bd8fbf4ed31f6f53f81c2aa5e49b0924618fee5e19809b55928d19166f81`  
		Last Modified: Fri, 09 May 2025 17:18:41 GMT  
		Size: 11.9 KB (11861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34388680d07d4ea09939b06d5cf712bf054778ca350753cd2f50476d3d2abd4c`  
		Last Modified: Fri, 09 May 2025 17:18:43 GMT  
		Size: 13.3 MB (13262403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:8e0e69156f544435abcd6e5ccd0268e6ef8134dbd2f1aa760855cddd15d565ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5560470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f5ed713c914c6a4d9b451047cabe42d5075812df87833b89d5d6f11b509aef`

```dockerfile
```

-	Layers:
	-	`sha256:251c265446780622ad5abe6c16d87fe4734b485d181fd86b7b4b8332c52379e0`  
		Last Modified: Fri, 09 May 2025 17:18:41 GMT  
		Size: 5.5 MB (5521628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30d9f3a378e9e6bd540105f97c1f30e501e46a34481f81586f91c1727c916b8f`  
		Last Modified: Fri, 09 May 2025 17:18:41 GMT  
		Size: 38.8 KB (38842 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java11-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:b26bcf3a81fcb5707ce6e8ac058286e85b1c3151e7aef10d7620c71f16d17849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.0 MB (453959196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6523e1c3090778a208e3ce40a24287544da4a5d1a2c56f92a1c1d2c09a86d139`
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
ENV JAVA_VERSION=jdk-11.0.26+4_openj9-0.49.0
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2425d0daa7c0ef6603910c1c51ed7f3d8dbeb4dff8e1542957771ac5045fc21e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_aarch64_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d013d38e03a3455c6867b10544dc30041bf7afdb595d60ee09af43d46cdb5720';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_ppc64le_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='08586859b8a53aa9d5424a38838e8332664622049c3c33b1b0e5ea88b56ce2d9';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_x64_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='84232088178d3886d2c6dff2621f60406390bc12c36752a3305799a87cefc255';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_s390x_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
USER root
# Wed, 23 Apr 2025 12:52:37 GMT
ARG LIBERTY_VERSION=25.0.0.4
# Wed, 23 Apr 2025 12:52:37 GMT
ARG LIBERTY_SHA=719ffc20a113a68f88dea0295fc366606a4c6028
# Wed, 23 Apr 2025 12:52:37 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.4/openliberty-runtime-25.0.0.4.zip
# Wed, 23 Apr 2025 12:52:37 GMT
ARG LIBERTY_BUILD_LABEL=cl250420250407-1902
# Wed, 23 Apr 2025 12:52:37 GMT
ARG OPENJ9_SCC=true
# Wed, 23 Apr 2025 12:52:37 GMT
ARG VERBOSE=false
# Wed, 23 Apr 2025 12:52:37 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250420250407-1902 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.4 liberty.version=25.0.0.4 io.openliberty.version=25.0.0.4
# Wed, 23 Apr 2025 12:52:37 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4 LIBERTY_SHA=719ffc20a113a68f88dea0295fc366606a4c6028 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.4/openliberty-runtime-25.0.0.4.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4 LIBERTY_SHA=719ffc20a113a68f88dea0295fc366606a4c6028 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.4/openliberty-runtime-25.0.0.4.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4 LIBERTY_SHA=719ffc20a113a68f88dea0295fc366606a4c6028 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.4/openliberty-runtime-25.0.0.4.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4 LIBERTY_SHA=719ffc20a113a68f88dea0295fc366606a4c6028 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.4/openliberty-runtime-25.0.0.4.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4 LIBERTY_SHA=719ffc20a113a68f88dea0295fc366606a4c6028 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.4/openliberty-runtime-25.0.0.4.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
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
	-	`sha256:19fea521b9d93a6aa0ec0bbd75d28d34b18d661aad702b6ca1026cb3bc07cff9`  
		Last Modified: Mon, 05 May 2025 17:03:09 GMT  
		Size: 53.6 MB (53621117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9eab7d47823ff1c290d9842072f5014e816e37f2a306f28165b8a0f969a379`  
		Last Modified: Mon, 05 May 2025 17:03:08 GMT  
		Size: 3.4 MB (3420282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354d5b0c1882ac54fea1577eeea37bfda9c6bb27f1bb23ab5467cfb83792c5d7`  
		Last Modified: Mon, 05 May 2025 19:41:27 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efa2f133016e7576e980d3fca4e16cc92b939cd9bdb7723e70dd83bce2a0604`  
		Last Modified: Mon, 05 May 2025 19:41:28 GMT  
		Size: 10.5 KB (10483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796d575648e02aee5ba7990c5e05b1bdac9a8583e1cd7fe4efccb52dd1d8f886`  
		Last Modified: Mon, 05 May 2025 19:41:28 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5a0233d7b60292e8e1c58ceb79a6f76b0c98067ac5fe564d8d412f0aefa0e3`  
		Last Modified: Mon, 05 May 2025 19:56:13 GMT  
		Size: 36.5 KB (36500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6159e6cd45da620138a7b6f3818621c4ad4995a5efcd283067cca39a1f33e01a`  
		Last Modified: Mon, 05 May 2025 19:56:23 GMT  
		Size: 337.5 MB (337486739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55a86ac8a393c3011aef61606489d1ab7bc8e1ef23c0289cbaaa45eaec5d2e0`  
		Last Modified: Mon, 05 May 2025 19:56:13 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec20935d3a8e5f1dd081a1a7f93457d06378cd2fcfa001ca6eedd69009a9d16`  
		Last Modified: Mon, 05 May 2025 19:56:13 GMT  
		Size: 11.9 KB (11853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00294085818f5bebaf2888cd34cdc453f43bc6526c7a50c8be69f31b0e39b81b`  
		Last Modified: Mon, 05 May 2025 19:56:15 GMT  
		Size: 12.0 MB (12033633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:cab27cb6a6cdde18972864211d801019c869c42cbeeb56302caec6c126ba7715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5568433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9df94e9bd8c1e7ac0f996676d9e9a159231716093d5996476d87a8ce020454`

```dockerfile
```

-	Layers:
	-	`sha256:7e68c3484b0a78aca143e32ec49295ebe558c72139e6327d4e57e089383a1043`  
		Last Modified: Mon, 05 May 2025 19:56:14 GMT  
		Size: 5.5 MB (5529686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ff372018bd750422af7b07c509297d238fb06111c6421f7595361ea7bdf2298`  
		Last Modified: Mon, 05 May 2025 19:56:13 GMT  
		Size: 38.7 KB (38747 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java11-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:8befe9922a8638b8bcb44ff46fa48417a6564fffa65b397ed88f249a64c2ad88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.0 MB (447047694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c5c825b25818b9e639c413a85ba5039890fb4896b95085b83bcfbc48b80db9c`
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
ENV JAVA_VERSION=jdk-11.0.26+4_openj9-0.49.0
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2425d0daa7c0ef6603910c1c51ed7f3d8dbeb4dff8e1542957771ac5045fc21e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_aarch64_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d013d38e03a3455c6867b10544dc30041bf7afdb595d60ee09af43d46cdb5720';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_ppc64le_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='08586859b8a53aa9d5424a38838e8332664622049c3c33b1b0e5ea88b56ce2d9';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_x64_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='84232088178d3886d2c6dff2621f60406390bc12c36752a3305799a87cefc255';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_s390x_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
USER root
# Wed, 23 Apr 2025 12:52:37 GMT
ARG LIBERTY_VERSION=25.0.0.4
# Wed, 23 Apr 2025 12:52:37 GMT
ARG LIBERTY_SHA=719ffc20a113a68f88dea0295fc366606a4c6028
# Wed, 23 Apr 2025 12:52:37 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.4/openliberty-runtime-25.0.0.4.zip
# Wed, 23 Apr 2025 12:52:37 GMT
ARG LIBERTY_BUILD_LABEL=cl250420250407-1902
# Wed, 23 Apr 2025 12:52:37 GMT
ARG OPENJ9_SCC=true
# Wed, 23 Apr 2025 12:52:37 GMT
ARG VERBOSE=false
# Wed, 23 Apr 2025 12:52:37 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250420250407-1902 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.4 liberty.version=25.0.0.4 io.openliberty.version=25.0.0.4
# Wed, 23 Apr 2025 12:52:37 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4 LIBERTY_SHA=719ffc20a113a68f88dea0295fc366606a4c6028 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.4/openliberty-runtime-25.0.0.4.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4 LIBERTY_SHA=719ffc20a113a68f88dea0295fc366606a4c6028 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.4/openliberty-runtime-25.0.0.4.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4 LIBERTY_SHA=719ffc20a113a68f88dea0295fc366606a4c6028 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.4/openliberty-runtime-25.0.0.4.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4 LIBERTY_SHA=719ffc20a113a68f88dea0295fc366606a4c6028 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.4/openliberty-runtime-25.0.0.4.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Wed, 23 Apr 2025 12:52:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.4 LIBERTY_SHA=719ffc20a113a68f88dea0295fc366606a4c6028 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.4/openliberty-runtime-25.0.0.4.zip LIBERTY_BUILD_LABEL=cl250420250407-1902 OPENJ9_SCC=true VERBOSE=false
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
	-	`sha256:19666ee566048861bb08f6fb85fbc7e4cda75c6d9e19a1ae0a945026d01a8f95`  
		Last Modified: Mon, 05 May 2025 16:54:35 GMT  
		Size: 50.9 MB (50913940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d481153e134fd552ad4d61da959a43cf0f090531621678b03dcf70f7b80a0925`  
		Last Modified: Mon, 05 May 2025 16:54:33 GMT  
		Size: 4.5 MB (4547476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b45ebb68581786c271a37163bd6ff950dbb20d0ab29e3d9816ddf910398a9e`  
		Last Modified: Mon, 05 May 2025 18:20:39 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c51d89d4a2279f8455431a4c91ca65c9e3b82914e60623065384905206be13c`  
		Last Modified: Mon, 05 May 2025 18:20:39 GMT  
		Size: 10.5 KB (10483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75afef98c5c1cdec19e95a646b959329f8edea7a8b40e3449343c362002dbe70`  
		Last Modified: Mon, 05 May 2025 18:20:39 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a4fb129eb6dc5162eab187749dcd6965f00a1087474765577c35ca8a0daec3`  
		Last Modified: Mon, 05 May 2025 18:27:39 GMT  
		Size: 33.1 KB (33117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279a51050746d3f34691e475df3fc65aa574771007906e680b7b14a2128248a4`  
		Last Modified: Mon, 05 May 2025 18:27:45 GMT  
		Size: 337.5 MB (337486141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e39a40b287f0c88b082302262dc242ed1ae534fd9f38a15a8319a2ebc7fcd1e`  
		Last Modified: Mon, 05 May 2025 18:27:39 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b56b40639b50f8b1bd3036812de62009446b3cb5c96ba3b3417281c9e2d506`  
		Last Modified: Mon, 05 May 2025 18:27:39 GMT  
		Size: 11.8 KB (11844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6716254c12d047ecb085686ed3ae7fea6c754dfecd1d41ef1abc59d28e26945b`  
		Last Modified: Mon, 05 May 2025 18:27:41 GMT  
		Size: 13.8 MB (13823157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:0c24c6c0948de1662d7a47b2769c7c14a98a21a604b68a9c36fa0e9dde8a204c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5564934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78fda3cf670a324778c1271af02cc22673c489cfe20e178513af57a52223f203`

```dockerfile
```

-	Layers:
	-	`sha256:f90c32f8e2a938422c6a691fcfb81833b08af4a2069d816e668f26f4cb19e21e`  
		Last Modified: Mon, 05 May 2025 18:27:39 GMT  
		Size: 5.5 MB (5526220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d97dbccf98941b0723418143e3ea2ddc6d2f80085d0d453ae03d716b09f7499a`  
		Last Modified: Mon, 05 May 2025 18:27:39 GMT  
		Size: 38.7 KB (38714 bytes)  
		MIME: application/vnd.in-toto+json
