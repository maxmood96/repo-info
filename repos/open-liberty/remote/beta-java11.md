## `open-liberty:beta-java11`

```console
$ docker pull open-liberty@sha256:556993eec4dad2faa1b9f7d921dcd4d6c7befca53ad7a8cbe868f267e18432b3
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

### `open-liberty:beta-java11` - linux; amd64

```console
$ docker pull open-liberty@sha256:d4ca4463a7066faf16ec760eff6c04cb764ba7b39b57f33e9acf0758ac63eb03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.9 MB (483923274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d090517e1a7124832635a943842bac8176ddbf19bdbbb8b24e6610a636ad7b`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 18:57:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Oct 2025 18:57:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 18:57:14 GMT
ENV JAVA_VERSION=jdk-11.0.29+7_openj9-0.56.0
# Thu, 30 Oct 2025 18:57:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9fd5b1e5f18c80d945570cd86db46f737fdecbdcd8978d502c4a601f704c6676';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='16289eb013673a686abfef6631570e5b08c6171a1f7cf79fd495759d53393c38';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='474acb3b9c1ba608efe0c3aa0321a271cfbe2044e89d73e7129b0b013eb484df';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='42c7324f112975abc6a36c1cacad8f7515924cc60c21ac45e5985e7908d2c931';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Oct 2025 18:57:17 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Oct 2025 18:57:17 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Oct 2025 18:57:48 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba";     TOMCAT_VERSION="9.0.111";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 30 Oct 2025 19:12:10 GMT
USER root
# Thu, 30 Oct 2025 19:12:10 GMT
ARG LIBERTY_VERSION=25.0.0.11-beta
# Thu, 30 Oct 2025 19:12:10 GMT
ARG LIBERTY_SHA=ad751b0af9e656d1bb9e477d01b63ae8faa60908
# Thu, 30 Oct 2025 19:12:10 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.11-beta/openliberty-runtime-25.0.0.11-beta.zip
# Thu, 30 Oct 2025 19:12:10 GMT
ARG LIBERTY_BUILD_LABEL=cl251020250923-1355
# Thu, 30 Oct 2025 19:12:10 GMT
ARG OPENJ9_SCC=true
# Thu, 30 Oct 2025 19:12:10 GMT
ARG VERBOSE=false
# Thu, 30 Oct 2025 19:12:10 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251020250923-1355 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=25.0.0.11-beta liberty.version=25.0.0.11-beta io.openliberty.version=25.0.0.11-beta
# Thu, 30 Oct 2025 19:12:10 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Thu, 30 Oct 2025 19:12:10 GMT
COPY helpers /opt/ol/helpers # buildkit
# Thu, 30 Oct 2025 19:12:10 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Thu, 30 Oct 2025 19:12:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11-beta LIBERTY_SHA=ad751b0af9e656d1bb9e477d01b63ae8faa60908 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.11-beta/openliberty-runtime-25.0.0.11-beta.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Thu, 30 Oct 2025 19:12:30 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11-beta LIBERTY_SHA=ad751b0af9e656d1bb9e477d01b63ae8faa60908 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.11-beta/openliberty-runtime-25.0.0.11-beta.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Thu, 30 Oct 2025 19:12:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 30 Oct 2025 19:12:30 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11-beta LIBERTY_SHA=ad751b0af9e656d1bb9e477d01b63ae8faa60908 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.11-beta/openliberty-runtime-25.0.0.11-beta.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 30 Oct 2025 19:12:30 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11-beta LIBERTY_SHA=ad751b0af9e656d1bb9e477d01b63ae8faa60908 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.11-beta/openliberty-runtime-25.0.0.11-beta.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Thu, 30 Oct 2025 19:12:53 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11-beta LIBERTY_SHA=ad751b0af9e656d1bb9e477d01b63ae8faa60908 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.11-beta/openliberty-runtime-25.0.0.11-beta.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Thu, 30 Oct 2025 19:12:53 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 30 Oct 2025 19:12:53 GMT
USER 1001
# Thu, 30 Oct 2025 19:12:53 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 30 Oct 2025 19:12:53 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 30 Oct 2025 19:12:53 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974be5de89f7216537fde0b3a5e08956e0e9824621147c8726917b833c20facf`  
		Last Modified: Thu, 30 Oct 2025 18:58:10 GMT  
		Size: 12.2 MB (12171646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29696f404a7dca35a5c964284fe247d031701f6d03e253a2f6c1ee48960ed82`  
		Last Modified: Thu, 30 Oct 2025 18:58:17 GMT  
		Size: 55.4 MB (55434640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20933a95bdc2c483315b6f60683445356b8222c959b12d8d7dc3883f9482fdab`  
		Last Modified: Thu, 30 Oct 2025 18:58:08 GMT  
		Size: 4.4 MB (4411847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da37d19f08702a62dfbfa67abac821a6f4c11396d02daeda094b0eb42d973d2`  
		Last Modified: Thu, 30 Oct 2025 19:13:38 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2aba24e95d3fdf5c75dfaa36bd40b56a1f1be7d6d47feecf15e7fafbdb8f0e9`  
		Last Modified: Thu, 30 Oct 2025 19:13:38 GMT  
		Size: 12.6 KB (12564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea91f890aaa748730fd6f24947cd9b41c58ef059c91988bea20c74eb86ad927a`  
		Last Modified: Thu, 30 Oct 2025 19:13:38 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c828046edeb0a81273bb13e5addab7c10b10931e2a7c68de2c968abb77b84b9c`  
		Last Modified: Thu, 30 Oct 2025 19:13:38 GMT  
		Size: 31.7 KB (31746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182fbafdf941548c0371aec164de1b2f23597baf4790513c8a7d5302c6251954`  
		Last Modified: Thu, 30 Oct 2025 22:25:12 GMT  
		Size: 367.6 MB (367616149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2722bd2df6d6c99f7e457c267c33b75a4d3caa887dae37c0905e947e0e48ed70`  
		Last Modified: Thu, 30 Oct 2025 19:13:38 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e760da9be5d66aad61b2e4b63c3c61d880390ffb7d511076cfd8c17477ecef2`  
		Last Modified: Thu, 30 Oct 2025 19:13:38 GMT  
		Size: 14.0 KB (14000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57cb21e182db0e465c63896160cb1a45a0c2c655628a5af2834babbfade6e64`  
		Last Modified: Thu, 30 Oct 2025 19:13:39 GMT  
		Size: 14.7 MB (14691518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java11` - unknown; unknown

```console
$ docker pull open-liberty@sha256:8bb47b10d86454868b1b8c7f04f79ad560a5807bb9083905fd60a120d11f19f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5837099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d334388b70bf45109f98b335c1c84c4bcc7e67a622cde3b6348376a75f74c7f`

```dockerfile
```

-	Layers:
	-	`sha256:7a3e5305ecfef25691824a2b8883ed58b9956a7c233bca5dbf03b6f6620c38c0`  
		Last Modified: Thu, 30 Oct 2025 20:50:18 GMT  
		Size: 5.8 MB (5797617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3f73b7299960fb9e94c48bd5e6c7743d7bcf9401c18379a15334e6061571cad`  
		Last Modified: Thu, 30 Oct 2025 20:50:19 GMT  
		Size: 39.5 KB (39482 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta-java11` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:24d05cee7d4d752c56ed417f5f7cf65d084dc2b9870492cdd58cbe0aad3dc669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **479.4 MB (479390663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2ffa9a84c42d1bf486fb031aebe3b0a3cb9912afb5193a447c379020c95fa7`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 18:55:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Oct 2025 18:55:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 18:55:10 GMT
ENV JAVA_VERSION=jdk-11.0.29+7_openj9-0.56.0
# Thu, 30 Oct 2025 18:55:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9fd5b1e5f18c80d945570cd86db46f737fdecbdcd8978d502c4a601f704c6676';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='16289eb013673a686abfef6631570e5b08c6171a1f7cf79fd495759d53393c38';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='474acb3b9c1ba608efe0c3aa0321a271cfbe2044e89d73e7129b0b013eb484df';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='42c7324f112975abc6a36c1cacad8f7515924cc60c21ac45e5985e7908d2c931';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Oct 2025 18:55:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Oct 2025 18:55:13 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Oct 2025 18:55:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba";     TOMCAT_VERSION="9.0.111";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 30 Oct 2025 19:52:24 GMT
USER root
# Thu, 30 Oct 2025 19:52:24 GMT
ARG LIBERTY_VERSION=25.0.0.11-beta
# Thu, 30 Oct 2025 19:52:24 GMT
ARG LIBERTY_SHA=ad751b0af9e656d1bb9e477d01b63ae8faa60908
# Thu, 30 Oct 2025 19:52:24 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.11-beta/openliberty-runtime-25.0.0.11-beta.zip
# Thu, 30 Oct 2025 19:52:24 GMT
ARG LIBERTY_BUILD_LABEL=cl251020250923-1355
# Thu, 30 Oct 2025 19:52:24 GMT
ARG OPENJ9_SCC=true
# Thu, 30 Oct 2025 19:52:24 GMT
ARG VERBOSE=false
# Thu, 30 Oct 2025 19:52:24 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251020250923-1355 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=25.0.0.11-beta liberty.version=25.0.0.11-beta io.openliberty.version=25.0.0.11-beta
# Thu, 30 Oct 2025 19:52:24 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Thu, 30 Oct 2025 19:52:24 GMT
COPY helpers /opt/ol/helpers # buildkit
# Thu, 30 Oct 2025 19:52:24 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Thu, 30 Oct 2025 19:52:24 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11-beta LIBERTY_SHA=ad751b0af9e656d1bb9e477d01b63ae8faa60908 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.11-beta/openliberty-runtime-25.0.0.11-beta.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Thu, 30 Oct 2025 19:52:46 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11-beta LIBERTY_SHA=ad751b0af9e656d1bb9e477d01b63ae8faa60908 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.11-beta/openliberty-runtime-25.0.0.11-beta.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Thu, 30 Oct 2025 19:52:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 30 Oct 2025 19:52:46 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11-beta LIBERTY_SHA=ad751b0af9e656d1bb9e477d01b63ae8faa60908 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.11-beta/openliberty-runtime-25.0.0.11-beta.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 30 Oct 2025 19:52:46 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11-beta LIBERTY_SHA=ad751b0af9e656d1bb9e477d01b63ae8faa60908 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.11-beta/openliberty-runtime-25.0.0.11-beta.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Thu, 30 Oct 2025 19:53:12 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11-beta LIBERTY_SHA=ad751b0af9e656d1bb9e477d01b63ae8faa60908 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.11-beta/openliberty-runtime-25.0.0.11-beta.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Thu, 30 Oct 2025 19:53:12 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 30 Oct 2025 19:53:12 GMT
USER 1001
# Thu, 30 Oct 2025 19:53:12 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 30 Oct 2025 19:53:12 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 30 Oct 2025 19:53:12 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040f67fa4eec83079a9633f2a50173b1e0cc6661a6a0c66fe958356446d2f619`  
		Last Modified: Thu, 30 Oct 2025 18:56:06 GMT  
		Size: 12.1 MB (12129845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8d3614cb3b275944d132487f6a1f8496c160f1fb54db750ce208ff92079b28`  
		Last Modified: Thu, 30 Oct 2025 18:56:09 GMT  
		Size: 53.7 MB (53713602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39424a13d5cea5d6c2f00edc7a0068e27c337906865d2ad07030dec7a373a5d3`  
		Last Modified: Thu, 30 Oct 2025 18:56:06 GMT  
		Size: 4.2 MB (4215277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c876ad38f1806be68d345df71f7939ba894cbde6d5a3455ae4b09e6d0d385adf`  
		Last Modified: Thu, 30 Oct 2025 19:53:52 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81000946f747bee6df9c4ba94016d8668820d81633024483382409e375c6ff4b`  
		Last Modified: Thu, 30 Oct 2025 19:53:52 GMT  
		Size: 12.6 KB (12570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ad86886258b24b0932da80916ea0afafe14d1ce0d94daa11e7b5eef6d2cfea`  
		Last Modified: Thu, 30 Oct 2025 19:53:52 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5f990cdccdf1414dbf3fd047d4cf5b7fea390dffe17adea2ad32720e3a0cfd`  
		Last Modified: Thu, 30 Oct 2025 19:53:52 GMT  
		Size: 42.3 KB (42326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42479fdf845a33f6ab95fa684cbe4a8bb483705a3e3b4cdff39a7a84a716d2cc`  
		Last Modified: Thu, 30 Oct 2025 19:53:47 GMT  
		Size: 367.6 MB (367616364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39196d4408ccf00a25f27b3d44515c9b43fa7082e66854245a01d69ebdfa8d1`  
		Last Modified: Thu, 30 Oct 2025 19:53:53 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6c6ae667b7e34d7d871749a838ed87b7b85830dcc89d027a66cf2c065bd26b`  
		Last Modified: Thu, 30 Oct 2025 19:53:53 GMT  
		Size: 14.0 KB (14003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084a3fbf9da714c2e7f392a2bfc0daf5eb5d8ab20f27887b43790977e92e4fc5`  
		Last Modified: Thu, 30 Oct 2025 19:53:57 GMT  
		Size: 14.3 MB (14261223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java11` - unknown; unknown

```console
$ docker pull open-liberty@sha256:77e58248370bc59356b518763bdb789a85ee5bf53df3a5b8d089b9a5bf3eb24e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5835587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9c0072f79ffc697540328cc02d7696c765bf02a10288a7257b61a578929902`

```dockerfile
```

-	Layers:
	-	`sha256:9486d5766eb67f0587b2a8cf06e5a3aa6610818555b4e5426dba2fa1e3b139c3`  
		Last Modified: Thu, 30 Oct 2025 20:50:25 GMT  
		Size: 5.8 MB (5795977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:581b4ce6d312715233b7478d41f43ff8100d0d276b03c8a89f3dd7b51eaeb04d`  
		Last Modified: Thu, 30 Oct 2025 20:50:26 GMT  
		Size: 39.6 KB (39610 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta-java11` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:a7b301bc1ee5efd16d0a090a930e070da5f948a116c81f8229666f28a6a45b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.8 MB (488837376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751ad6db42a32c64039d59f1dadd30e7b794e6516cd6eb14eff193106b65268d`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 01 Oct 2025 07:06:37 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:06:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:06:42 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Wed, 01 Oct 2025 07:06:43 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 18:52:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Oct 2025 18:52:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 18:52:43 GMT
ENV JAVA_VERSION=jdk-11.0.29+7_openj9-0.56.0
# Thu, 30 Oct 2025 19:02:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9fd5b1e5f18c80d945570cd86db46f737fdecbdcd8978d502c4a601f704c6676';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='16289eb013673a686abfef6631570e5b08c6171a1f7cf79fd495759d53393c38';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='474acb3b9c1ba608efe0c3aa0321a271cfbe2044e89d73e7129b0b013eb484df';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='42c7324f112975abc6a36c1cacad8f7515924cc60c21ac45e5985e7908d2c931';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Oct 2025 19:02:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Oct 2025 19:02:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Oct 2025 19:02:39 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba";     TOMCAT_VERSION="9.0.111";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 30 Oct 2025 19:32:10 GMT
USER root
# Thu, 30 Oct 2025 19:32:10 GMT
ARG LIBERTY_VERSION=25.0.0.11-beta
# Thu, 30 Oct 2025 19:32:10 GMT
ARG LIBERTY_SHA=ad751b0af9e656d1bb9e477d01b63ae8faa60908
# Thu, 30 Oct 2025 19:32:10 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.11-beta/openliberty-runtime-25.0.0.11-beta.zip
# Thu, 30 Oct 2025 19:32:10 GMT
ARG LIBERTY_BUILD_LABEL=cl251020250923-1355
# Thu, 30 Oct 2025 19:32:10 GMT
ARG OPENJ9_SCC=true
# Thu, 30 Oct 2025 19:32:10 GMT
ARG VERBOSE=false
# Thu, 30 Oct 2025 19:32:10 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251020250923-1355 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=25.0.0.11-beta liberty.version=25.0.0.11-beta io.openliberty.version=25.0.0.11-beta
# Thu, 30 Oct 2025 19:32:10 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Thu, 30 Oct 2025 19:32:10 GMT
COPY helpers /opt/ol/helpers # buildkit
# Thu, 30 Oct 2025 19:32:11 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Thu, 30 Oct 2025 19:32:12 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11-beta LIBERTY_SHA=ad751b0af9e656d1bb9e477d01b63ae8faa60908 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.11-beta/openliberty-runtime-25.0.0.11-beta.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Thu, 30 Oct 2025 19:32:38 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11-beta LIBERTY_SHA=ad751b0af9e656d1bb9e477d01b63ae8faa60908 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.11-beta/openliberty-runtime-25.0.0.11-beta.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Thu, 30 Oct 2025 19:32:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 30 Oct 2025 19:32:39 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11-beta LIBERTY_SHA=ad751b0af9e656d1bb9e477d01b63ae8faa60908 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.11-beta/openliberty-runtime-25.0.0.11-beta.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 30 Oct 2025 19:32:39 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11-beta LIBERTY_SHA=ad751b0af9e656d1bb9e477d01b63ae8faa60908 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.11-beta/openliberty-runtime-25.0.0.11-beta.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Thu, 30 Oct 2025 19:33:21 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11-beta LIBERTY_SHA=ad751b0af9e656d1bb9e477d01b63ae8faa60908 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.11-beta/openliberty-runtime-25.0.0.11-beta.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Thu, 30 Oct 2025 19:33:21 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 30 Oct 2025 19:33:21 GMT
USER 1001
# Thu, 30 Oct 2025 19:33:21 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 30 Oct 2025 19:33:21 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 30 Oct 2025 19:33:21 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d05c427cc331d7b6dd9baffe91a10981b54840825b7525c3636088e5c3447a5`  
		Last Modified: Thu, 30 Oct 2025 18:54:22 GMT  
		Size: 12.9 MB (12893771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84d91243995e4da3caeea42a02c003c34e01fba10c017640845d5bc43efa1f4`  
		Last Modified: Thu, 30 Oct 2025 21:16:41 GMT  
		Size: 57.3 MB (57283294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afafd816ee78735ecf393921e856df65b71512fb406db56048f2910a0348614f`  
		Last Modified: Thu, 30 Oct 2025 19:50:34 GMT  
		Size: 3.5 MB (3489405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803cf59e8a0df7310c084498b3ac460e31f54a4872256df6761afb13330b5769`  
		Last Modified: Thu, 30 Oct 2025 19:34:39 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95240f4afb288719f2bcab753cd3800d104c7f9f13aa5c53ee78a20bb712d96`  
		Last Modified: Thu, 30 Oct 2025 19:34:39 GMT  
		Size: 12.6 KB (12565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f636fdbd86bbc797807036aedaff82dcf0de6f3ea302f127ff9521b0a899d27`  
		Last Modified: Thu, 30 Oct 2025 19:34:39 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980fd435d0890cd3de79c1b256a78980108c872369de78efecedc5bb7362d915`  
		Last Modified: Thu, 30 Oct 2025 19:34:39 GMT  
		Size: 36.5 KB (36496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012a9a1c8db44040652592f71168cc1e5aa7ba68827a0e6b27cbe922ff266595`  
		Last Modified: Thu, 30 Oct 2025 22:23:57 GMT  
		Size: 367.6 MB (367616552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef446d48c20fd81361e7aad24034970dc775f7b74959e97c04377b2e84134e1b`  
		Last Modified: Thu, 30 Oct 2025 19:34:39 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237bf7978d1a4558c3e2abbaad21498b5031c67c5d114f2d985307eddb7bb778`  
		Last Modified: Thu, 30 Oct 2025 19:34:39 GMT  
		Size: 14.0 KB (14007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475d334359f1a6f5c1724d87027750598eef0ba561eb5d0968198fd90b359ebc`  
		Last Modified: Thu, 30 Oct 2025 19:34:41 GMT  
		Size: 13.0 MB (13042148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java11` - unknown; unknown

```console
$ docker pull open-liberty@sha256:0978c52e5f1694f65de56fa7f0730ec1ad9eb3f4f6bc4b712c2504d6fbbc211a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5841754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2bf25a478366c813b104d149881de0505f064790ff2af197fd029f4dd4b2602`

```dockerfile
```

-	Layers:
	-	`sha256:27a1a6fe957958092cab8969759d8f8754aa7c64ac0b8a79b94bb71f919fce28`  
		Last Modified: Thu, 30 Oct 2025 20:50:31 GMT  
		Size: 5.8 MB (5802238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d92a5d1024cfef1c96627a6b69ce9c94e89cae9346f6a53ac4fc6ffba087020e`  
		Last Modified: Thu, 30 Oct 2025 20:50:32 GMT  
		Size: 39.5 KB (39516 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta-java11` - linux; s390x

```console
$ docker pull open-liberty@sha256:ff536ef9a639b3be61e1f32de21f88d3caf80b8bd87c799ca1fa8bcd6330d40d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **481.8 MB (481776005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d64638af0916b64e29ab8fc2e42e78b9c9466dfebae5afa529b08c1deea45d`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:26 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:28 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Wed, 01 Oct 2025 07:05:28 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 18:53:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Oct 2025 18:53:24 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 18:53:24 GMT
ENV JAVA_VERSION=jdk-11.0.29+7_openj9-0.56.0
# Thu, 30 Oct 2025 19:05:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9fd5b1e5f18c80d945570cd86db46f737fdecbdcd8978d502c4a601f704c6676';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='16289eb013673a686abfef6631570e5b08c6171a1f7cf79fd495759d53393c38';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='474acb3b9c1ba608efe0c3aa0321a271cfbe2044e89d73e7129b0b013eb484df';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='42c7324f112975abc6a36c1cacad8f7515924cc60c21ac45e5985e7908d2c931';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Oct 2025 19:05:04 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Oct 2025 19:05:04 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Oct 2025 19:05:39 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba";     TOMCAT_VERSION="9.0.111";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 30 Oct 2025 19:50:14 GMT
USER root
# Thu, 30 Oct 2025 19:50:14 GMT
ARG LIBERTY_VERSION=25.0.0.11-beta
# Thu, 30 Oct 2025 19:50:14 GMT
ARG LIBERTY_SHA=ad751b0af9e656d1bb9e477d01b63ae8faa60908
# Thu, 30 Oct 2025 19:50:14 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.11-beta/openliberty-runtime-25.0.0.11-beta.zip
# Thu, 30 Oct 2025 19:50:14 GMT
ARG LIBERTY_BUILD_LABEL=cl251020250923-1355
# Thu, 30 Oct 2025 19:50:14 GMT
ARG OPENJ9_SCC=true
# Thu, 30 Oct 2025 19:50:14 GMT
ARG VERBOSE=false
# Thu, 30 Oct 2025 19:50:14 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251020250923-1355 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=25.0.0.11-beta liberty.version=25.0.0.11-beta io.openliberty.version=25.0.0.11-beta
# Thu, 30 Oct 2025 19:50:14 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Thu, 30 Oct 2025 19:50:15 GMT
COPY helpers /opt/ol/helpers # buildkit
# Thu, 30 Oct 2025 19:50:15 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Thu, 30 Oct 2025 19:50:16 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11-beta LIBERTY_SHA=ad751b0af9e656d1bb9e477d01b63ae8faa60908 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.11-beta/openliberty-runtime-25.0.0.11-beta.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Thu, 30 Oct 2025 19:50:51 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11-beta LIBERTY_SHA=ad751b0af9e656d1bb9e477d01b63ae8faa60908 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.11-beta/openliberty-runtime-25.0.0.11-beta.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Thu, 30 Oct 2025 19:50:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 30 Oct 2025 19:50:52 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11-beta LIBERTY_SHA=ad751b0af9e656d1bb9e477d01b63ae8faa60908 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.11-beta/openliberty-runtime-25.0.0.11-beta.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 30 Oct 2025 19:50:53 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11-beta LIBERTY_SHA=ad751b0af9e656d1bb9e477d01b63ae8faa60908 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.11-beta/openliberty-runtime-25.0.0.11-beta.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Thu, 30 Oct 2025 19:51:42 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11-beta LIBERTY_SHA=ad751b0af9e656d1bb9e477d01b63ae8faa60908 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.11-beta/openliberty-runtime-25.0.0.11-beta.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Thu, 30 Oct 2025 19:51:42 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 30 Oct 2025 19:51:42 GMT
USER 1001
# Thu, 30 Oct 2025 19:51:42 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 30 Oct 2025 19:51:42 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 30 Oct 2025 19:51:42 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:e4a5a322dd65d010805129ca793d5d5e6b07872cbc2f41d566a84091b39c794e`  
		Last Modified: Thu, 02 Oct 2025 00:25:04 GMT  
		Size: 28.0 MB (28003413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85ec275e8f24c28d1884cb863f6a811d464cfb2b0e274ec7e8be26978e82f3c`  
		Last Modified: Thu, 30 Oct 2025 18:55:24 GMT  
		Size: 12.2 MB (12219687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf143b346acde13c74277f365d5da4888bb48d1c60bfa2e141fad8feab58c1e`  
		Last Modified: Thu, 30 Oct 2025 19:06:36 GMT  
		Size: 54.4 MB (54423360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd2b6ac9e379c7c1f18f3aeb5c880f8b300627339b391506ddad56a56aba178`  
		Last Modified: Thu, 30 Oct 2025 19:06:27 GMT  
		Size: 4.6 MB (4625483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4ab7de4a63050a78d14ae68efe7dcccca605b20840514d702631606f052d45`  
		Last Modified: Thu, 30 Oct 2025 19:53:53 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964dc13857825efea64b8beaa24d82281c4a0c06811c651798b6c22ede76a546`  
		Last Modified: Thu, 30 Oct 2025 19:53:53 GMT  
		Size: 12.6 KB (12567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023d930a754e2dded973424df97e46856c10696ea6089e28803c114d6a394d5e`  
		Last Modified: Thu, 30 Oct 2025 19:53:53 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1797a654534854b19f435ac55edd864def0ceb0920ebe6f6928c8fda92cfe065`  
		Last Modified: Thu, 30 Oct 2025 19:53:53 GMT  
		Size: 33.1 KB (33112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84cd4f4d3909b73be175f03e7443593dc9f448fba060ebd06fd5705a33e5ec4`  
		Last Modified: Thu, 30 Oct 2025 22:20:52 GMT  
		Size: 367.6 MB (367616068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb118325da233d7d0b8a6299798b57fea8c55fcccf2fb36b731cf17f046ea2a9`  
		Last Modified: Thu, 30 Oct 2025 19:53:54 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59eb22e34a5cbb33bf410772dd669dbc10aa471b06f4771ee652b60e5fdd3111`  
		Last Modified: Thu, 30 Oct 2025 19:53:54 GMT  
		Size: 14.0 KB (14012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1569a5a189a2031b7deb6174e54bf6ec0086128f1de2724d613bf50dc34bda12`  
		Last Modified: Thu, 30 Oct 2025 19:53:55 GMT  
		Size: 14.8 MB (14825957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java11` - unknown; unknown

```console
$ docker pull open-liberty@sha256:e6700941fa5320f159b2d2fe8352270da4c11d130568ec950a393eb9ec34f128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5838115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb7dd781085133367cb310a14ba5c28f22f24e028c7965c86e622a56afbbd03`

```dockerfile
```

-	Layers:
	-	`sha256:b32483bcd5c2158de568cd660dfe348637e971aaf83e1eefa65d0264c761ae54`  
		Last Modified: Thu, 30 Oct 2025 20:50:38 GMT  
		Size: 5.8 MB (5798634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36c99bc59d766f35fa2fee0d2f7897cb51532e90213135324a9f6c1df4ba0214`  
		Last Modified: Thu, 30 Oct 2025 20:50:39 GMT  
		Size: 39.5 KB (39481 bytes)  
		MIME: application/vnd.in-toto+json
