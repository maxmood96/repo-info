## `open-liberty:full-java8-openj9`

```console
$ docker pull open-liberty@sha256:2fe300e462039e2c15d9ab28a67bdb72d7c4850a23950651f99ebf2e7ea9c0d3
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

### `open-liberty:full-java8-openj9` - linux; amd64

```console
$ docker pull open-liberty@sha256:60994411d1426fd70acf6cf1cde46441e11a2d8a93f6aeb5d3109a1dd8c3e3bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.8 MB (447824061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3792fb8b74c8cb79a4e2b5ed6039c062601cbb9893dbe181697e435ef8e714`
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
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Thu, 13 Mar 2025 08:54:45 GMT
CMD ["/bin/bash"]
# Thu, 13 Mar 2025 08:54:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Mar 2025 08:54:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_VERSION=jdk8u442-b06_openj9-0.49.0
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='7975d93310af64c805c76b5bcab8b195121d76321ebf72d1ff9bb2bff2426277';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jre_aarch64_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='2c5acea578d59fdab41f8544beddfa6af0893d91cde4b92233ed158c35ac3397';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jre_ppc64le_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='d665f2e041c18de11f15955164c935961e7da0bf9358182769466611d83c5b32';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jre_x64_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='2af59a4f3600e41b7e0d6b8ab18006d852af0d81895902dc6d46feeab1f5b195';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jre_s390x_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcdf68f7fd6da502a0235d0da2d81ec81a432017f7d5e2ffe6ed8b82c1f5dfb`  
		Last Modified: Mon, 05 May 2025 16:35:42 GMT  
		Size: 12.2 MB (12172133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f120f72da7a8e17e6b16e584161af1e6c0c2e565ff2c923339d9ec3be389fd7`  
		Last Modified: Mon, 05 May 2025 16:35:43 GMT  
		Size: 50.4 MB (50438017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4134e48a51ae7fa8957b2d204a5f88955e19c50a668c2ed972e4440ee9db535f`  
		Last Modified: Mon, 05 May 2025 16:35:41 GMT  
		Size: 4.3 MB (4327278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc531de09b02dec22a8baeea1bd1f6cc65bdd043c70b8bf5a749c24896c0e2b`  
		Last Modified: Mon, 05 May 2025 17:05:08 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321053cb65afbe660aea99dc2d2b2385325b9fb9c989664d87af62b35ca1aa2a`  
		Last Modified: Mon, 05 May 2025 17:05:08 GMT  
		Size: 10.5 KB (10479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75955fefec25afbf7cd7fa5b68be888755c537f4e03496ab298c60ade6804919`  
		Last Modified: Mon, 05 May 2025 17:05:08 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42563e038edb451d18f128a005868c2ef0baef623aaf16b183141c87c47658b2`  
		Last Modified: Mon, 05 May 2025 17:04:08 GMT  
		Size: 31.7 KB (31748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb4f7df789922e83813047bcd867336a9ca462d3e8b09cdb3d023fa8f1a4f18`  
		Last Modified: Mon, 05 May 2025 17:05:44 GMT  
		Size: 337.5 MB (337486589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6620b9f7ab698bfd86c7c8e69f2143b5a1d4cc2d7de4abb51347b13c6e4d174`  
		Last Modified: Mon, 05 May 2025 17:05:09 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c51c3f52cca5f6202a885da85c019bea46937e561a35fc59cfbfae77cf46d94`  
		Last Modified: Mon, 05 May 2025 17:05:09 GMT  
		Size: 11.8 KB (11842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7e6e5b01b0c7c507f56bfc2f3e23dc16de4bd91f0fd618f3e2024786862711`  
		Last Modified: Mon, 05 May 2025 17:05:09 GMT  
		Size: 13.8 MB (13811016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java8-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:edb692bad230e919c0de77796cea28d5ee5828bb88924bafad542278296840e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5582762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cabf4a52312a18f42a2fc05fc0b2d03307248aef026d587033faabfc39adf05`

```dockerfile
```

-	Layers:
	-	`sha256:0d6a25be9a6b2ddbfb18c99a33019b5ed03364a5ff4ee44cb3b1da429981b674`  
		Last Modified: Mon, 05 May 2025 17:05:08 GMT  
		Size: 5.5 MB (5543446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55fc3772a45515d02f65b6ffc89bd4ee29e5d2c0b48b8734aa623125b1f2c654`  
		Last Modified: Mon, 05 May 2025 17:05:08 GMT  
		Size: 39.3 KB (39316 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java8-openj9` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:dba4d268ac299b6052b35f3b5166df67def9bca153d847cfd93be5823f36893c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **443.9 MB (443899929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3405247a524051abd5c099c26b89d2434ee58537d7383cae84221f579ba4e8f`
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
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Thu, 13 Mar 2025 08:54:45 GMT
CMD ["/bin/bash"]
# Thu, 13 Mar 2025 08:54:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Mar 2025 08:54:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_VERSION=jdk8u442-b06_openj9-0.49.0
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='7975d93310af64c805c76b5bcab8b195121d76321ebf72d1ff9bb2bff2426277';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jre_aarch64_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='2c5acea578d59fdab41f8544beddfa6af0893d91cde4b92233ed158c35ac3397';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jre_ppc64le_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='d665f2e041c18de11f15955164c935961e7da0bf9358182769466611d83c5b32';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jre_x64_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='2af59a4f3600e41b7e0d6b8ab18006d852af0d81895902dc6d46feeab1f5b195';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jre_s390x_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78892370879d09e257e1f423fb01169148aa714423fd175a7a3f0933ae6673e`  
		Last Modified: Mon, 05 May 2025 17:14:03 GMT  
		Size: 12.1 MB (12129417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59df2b621fc96906dc25834cb06ee334da647ac3cb1ecb6f88dbad968c307f7`  
		Last Modified: Mon, 05 May 2025 17:16:16 GMT  
		Size: 49.8 MB (49841682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de8c81bbe052f32a1aa295f37eb24d514255ba008270badfe77af3bcd88ae31`  
		Last Modified: Mon, 05 May 2025 17:16:15 GMT  
		Size: 4.1 MB (4050715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1c2b9650958c75a7e4ce600e61959c6ab15ba116c9a0cedcb5dc9d2d459a84`  
		Last Modified: Mon, 05 May 2025 22:08:51 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b395cffbe28c9e5e92f6b8af193c7155790e7a2a5348d1824dd782ef45ad92`  
		Last Modified: Mon, 05 May 2025 22:08:51 GMT  
		Size: 10.5 KB (10477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2f9e56a6c66a342b68a751edd9928b1d3e3ad75cf692e20fa5fb8d139b9eb5`  
		Last Modified: Mon, 05 May 2025 22:08:51 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ac302ddf5eae7df0e0913f740e9d6b8e35d99dff0a078f06fd9f8bca23de21`  
		Last Modified: Mon, 05 May 2025 22:15:32 GMT  
		Size: 42.3 KB (42326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac98c7f57f0627a3b0208907983cf3c8a849fe4acad98da2b3d056c07af9b978`  
		Last Modified: Mon, 05 May 2025 22:17:52 GMT  
		Size: 337.5 MB (337486507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0824499459633396763eb42633b3b7f0836018c3ce852a95b294237b0af41cc5`  
		Last Modified: Mon, 05 May 2025 22:15:32 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dc461da32e3d98278b60b63367ed34b04f6327b2649fa2c5852cf8756c9b22`  
		Last Modified: Mon, 05 May 2025 22:15:32 GMT  
		Size: 11.8 KB (11845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8080c10ee60fdeaef8ca4d3d22b284d9b0caecf6990c651b7423d092c725a6d`  
		Last Modified: Mon, 05 May 2025 22:15:34 GMT  
		Size: 13.0 MB (12970406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java8-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:ad08e8eaa64471e3861ef1cdc6b21058e78392e4c9afc7b9eca0d94501959412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5582728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5619276bcc8b89024eb146af57af00188643835b741b831057e548ab5a4d67a`

```dockerfile
```

-	Layers:
	-	`sha256:116110f757d0aa3b44acb266d3fae11552d6255837e27cf562d67ea7bbfcc70f`  
		Last Modified: Mon, 05 May 2025 22:15:32 GMT  
		Size: 5.5 MB (5543262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:013cc720653f0e974bd872a3dab297cca03b3b84d9d8ed34fc3e495cd6b53b2e`  
		Last Modified: Mon, 05 May 2025 22:15:32 GMT  
		Size: 39.5 KB (39466 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java8-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:61760b41caa3278f5784b33b0f6d991c5cf6a2e5be2eaefcd1123e2b9493a4d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.1 MB (452070697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ff90c62b93b9c8db28dc58451a11f54ec57d251d8eb49d70af0479480ce9e0`
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
ENV JAVA_VERSION=jdk8u442-b06_openj9-0.49.0
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='7975d93310af64c805c76b5bcab8b195121d76321ebf72d1ff9bb2bff2426277';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jre_aarch64_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='2c5acea578d59fdab41f8544beddfa6af0893d91cde4b92233ed158c35ac3397';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jre_ppc64le_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='d665f2e041c18de11f15955164c935961e7da0bf9358182769466611d83c5b32';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jre_x64_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='2af59a4f3600e41b7e0d6b8ab18006d852af0d81895902dc6d46feeab1f5b195';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jre_s390x_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:ac7f1e6f9278eb6e2aac3d7bb6780d7f9af8ee2f33d5375a103374858e42b3f6`  
		Last Modified: Mon, 05 May 2025 16:58:41 GMT  
		Size: 51.8 MB (51832713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e996ddf0d08e2e7e0461f8c6f71a89ac2562337175a6142bfa7a924ae0ec047`  
		Last Modified: Mon, 05 May 2025 16:58:40 GMT  
		Size: 3.5 MB (3466637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9137d00f49d2450ee4e92b295aceb49880c683f0325a22d12413cfd2065f113e`  
		Last Modified: Mon, 05 May 2025 19:38:17 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8ab01971df5385ddbb1af8f6f6c20768ab48dbd920da23ec5799b8d24d5125`  
		Last Modified: Mon, 05 May 2025 19:38:17 GMT  
		Size: 10.5 KB (10481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79775e7d2fa0c0584dc6e8f17c2ad5141213bd8375fd6e02473ce3d5a6479764`  
		Last Modified: Mon, 05 May 2025 19:38:17 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d029457e42ba4e6e017c53cc3c1a024ee65f3d1eeb15b170656ba385601179fd`  
		Last Modified: Mon, 05 May 2025 19:53:18 GMT  
		Size: 36.5 KB (36500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c997a304ad8c889c441e175dc086e52822f35f6b7120f6a91d231cda9ad7cc`  
		Last Modified: Mon, 05 May 2025 19:53:42 GMT  
		Size: 337.5 MB (337486737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c384078b1cb8bd3a4d5fc28d02e34d2c133181eaac14863c573d342fa3bf59e5`  
		Last Modified: Mon, 05 May 2025 19:53:18 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8d54f49de07c8e70cbafcd3fda580831c2fd0f1b961cd6df226e4ab8174324`  
		Last Modified: Mon, 05 May 2025 19:53:18 GMT  
		Size: 11.8 KB (11850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0085b2c9c0c84c1ebb0ab3a4a8e96d789fcada6ef43ccf8bf20e34f3b30ce9`  
		Last Modified: Mon, 05 May 2025 19:53:21 GMT  
		Size: 11.9 MB (11887198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java8-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:bd87ba273b31df56b50a1893d7e601e9c5319ca69de5677b5854af895523f32b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5587469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4341c65aedceea33474f1084ce9f525092430dd13eb90791ea92a757551f97d`

```dockerfile
```

-	Layers:
	-	`sha256:e6894ad7949d871b8abf3aa5d5c3c19a13cc048113d8f42cf75b0b746baf621e`  
		Last Modified: Mon, 05 May 2025 19:53:18 GMT  
		Size: 5.5 MB (5548107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e32aa31b6f0c02f637bf976afbc2bb9443aba91524f750a1e33942e70498377`  
		Last Modified: Mon, 05 May 2025 19:53:18 GMT  
		Size: 39.4 KB (39362 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java8-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:c71c3a6fb8dd7a9995a244507eebd21e5c3c4ac61dd5c08507564daed2e6dd4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.0 MB (446004204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21be8cf0647df53c685a199df890725b7877117a2e2d1d8ad76a3bf449688df`
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
ENV JAVA_VERSION=jdk8u442-b06_openj9-0.49.0
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='7975d93310af64c805c76b5bcab8b195121d76321ebf72d1ff9bb2bff2426277';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jre_aarch64_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='2c5acea578d59fdab41f8544beddfa6af0893d91cde4b92233ed158c35ac3397';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jre_ppc64le_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='d665f2e041c18de11f15955164c935961e7da0bf9358182769466611d83c5b32';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jre_x64_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='2af59a4f3600e41b7e0d6b8ab18006d852af0d81895902dc6d46feeab1f5b195';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jre_s390x_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:2265d2508866c764efaca5b22d90029a6ae6a2dbceb0b6bd6542a6724cc11099`  
		Last Modified: Mon, 05 May 2025 16:49:42 GMT  
		Size: 50.4 MB (50388931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31d038dd47544f8128526e703f2b450894bb57d1b358a061ecd5d6a85c7fe5d`  
		Last Modified: Mon, 05 May 2025 16:49:40 GMT  
		Size: 4.3 MB (4342528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ce9e00993cd3ad3325c5f49f7577e99594cb57928ca47a404bd3b63c711d53`  
		Last Modified: Mon, 05 May 2025 18:18:54 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820676044e61d3ed84a7e9ca6a62500fb08d14d2b0b6c0d0bc40be65a8ee399a`  
		Last Modified: Mon, 05 May 2025 18:18:54 GMT  
		Size: 10.5 KB (10481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2566c5d155e739c076ed70f88f6100b2a5a398419a02dfb22a431167afc681e6`  
		Last Modified: Mon, 05 May 2025 18:18:54 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6a8e28d2d3bc4f97df58e90e54e39484d3f47df4c2240117cddc649570f7af`  
		Last Modified: Mon, 05 May 2025 18:25:58 GMT  
		Size: 33.1 KB (33114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13878c342859f1ad1f8ef795201853503298742c3b944c4d9a6a40c875fb5aa`  
		Last Modified: Mon, 05 May 2025 18:26:05 GMT  
		Size: 337.5 MB (337486079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d39d428894f5706e52045c7130784e1ac7089ef246122ffb51e8a4e814cc68e`  
		Last Modified: Mon, 05 May 2025 18:25:58 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1aa8688b98caccf380b43775985457a16aa7635188b9524ae9e2f62f4f99ab`  
		Last Modified: Mon, 05 May 2025 18:25:58 GMT  
		Size: 11.8 KB (11844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ccf0395e6fbea499f135a12ec2778fb406324f37f96678b19f73675ab93ec0`  
		Last Modified: Mon, 05 May 2025 18:26:00 GMT  
		Size: 13.5 MB (13509696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java8-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:a0d52e34212fb893c4298a3046db6ad76fb18c178c97733e244221b1bebac9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5583778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:328cc4a57b4841696802e5dca3dabd2cb93b26dc1b3514801e107123b563b0d9`

```dockerfile
```

-	Layers:
	-	`sha256:029e04de51c73bbb68126fc02b0283a8dfec3c94694715ae326e2db87b0d6261`  
		Last Modified: Mon, 05 May 2025 18:25:58 GMT  
		Size: 5.5 MB (5544463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6581c393aed1a912123585201ee95e42f0de72260636ab6319c3f142cd1da6cd`  
		Last Modified: Mon, 05 May 2025 18:25:58 GMT  
		Size: 39.3 KB (39315 bytes)  
		MIME: application/vnd.in-toto+json
