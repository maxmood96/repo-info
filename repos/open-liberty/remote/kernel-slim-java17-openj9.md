## `open-liberty:kernel-slim-java17-openj9`

```console
$ docker pull open-liberty@sha256:4be51530029c4dfa1f3383c2bd7c0cd9ae2965d7a6f2d440dba00d3bdf6300fb
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
$ docker pull open-liberty@sha256:70e8d09f39f418b7ac47971e1183d37310f00a10c9df6caae2623b8991502fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 MB (115557329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767e8d4a8e38cc01d74b7847e34ba2e942db767eeb5f11964061bc3778c21494`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 11 Sep 2024 13:43:23 GMT
ARG RELEASE
# Wed, 11 Sep 2024 13:43:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 13:43:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 13:43:23 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 13:43:23 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 13:43:23 GMT
CMD ["/bin/bash"]
# Wed, 11 Sep 2024 13:43:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 11 Sep 2024 13:43:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
ENV JAVA_VERSION=jdk-17.0.12+7_openj9-0.46.1
# Wed, 11 Sep 2024 13:43:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cb2bfe44358158dcaa903e1f9aeb3e895adc1d5ace1f764e0dc1b1aeb4ffb77e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_aarch64_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='29f969c56c1e82587e0fcb1c0253dec413538c9599eaec9fcdb3983d181aad96';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_ppc64le_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='f218a8e1596197a3e89e9eff3ef4dc3e56ff41d7e293261e02cbc589a418998e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_x64_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='1490c54b365dc1c4bfea47412433df79ebfd2c3f85c9f7b1c88ce2d7ae7dee75';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_s390x_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Sep 2024 13:43:23 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 11 Sep 2024 13:43:23 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.95/bin/apache-tomcat-9.0.95.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
USER root
# Wed, 11 Sep 2024 13:43:23 GMT
ARG LIBERTY_VERSION=24.0.0.9
# Wed, 11 Sep 2024 13:43:23 GMT
ARG LIBERTY_SHA=416a2f8dd37d676b9e60c37463f536974a31d2ef
# Wed, 11 Sep 2024 13:43:23 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.9/openliberty-kernel-24.0.0.9.zip
# Wed, 11 Sep 2024 13:43:23 GMT
ARG LIBERTY_BUILD_LABEL=cl241020240827-1743
# Wed, 11 Sep 2024 13:43:23 GMT
ARG OPENJ9_SCC=true
# Wed, 11 Sep 2024 13:43:23 GMT
ARG VERBOSE=false
# Wed, 11 Sep 2024 13:43:23 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl241020240827-1743 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=24.0.0.9
# Wed, 11 Sep 2024 13:43:23 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
# ARGS: LIBERTY_VERSION=24.0.0.9 LIBERTY_SHA=416a2f8dd37d676b9e60c37463f536974a31d2ef LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.9/openliberty-kernel-24.0.0.9.zip LIBERTY_BUILD_LABEL=cl241020240827-1743 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
# ARGS: LIBERTY_VERSION=24.0.0.9 LIBERTY_SHA=416a2f8dd37d676b9e60c37463f536974a31d2ef LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.9/openliberty-kernel-24.0.0.9.zip LIBERTY_BUILD_LABEL=cl241020240827-1743 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 11 Sep 2024 13:43:23 GMT
# ARGS: LIBERTY_VERSION=24.0.0.9 LIBERTY_SHA=416a2f8dd37d676b9e60c37463f536974a31d2ef LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.9/openliberty-kernel-24.0.0.9.zip LIBERTY_BUILD_LABEL=cl241020240827-1743 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
# ARGS: LIBERTY_VERSION=24.0.0.9 LIBERTY_SHA=416a2f8dd37d676b9e60c37463f536974a31d2ef LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.9/openliberty-kernel-24.0.0.9.zip LIBERTY_BUILD_LABEL=cl241020240827-1743 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
# ARGS: LIBERTY_VERSION=24.0.0.9 LIBERTY_SHA=416a2f8dd37d676b9e60c37463f536974a31d2ef LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.9/openliberty-kernel-24.0.0.9.zip LIBERTY_BUILD_LABEL=cl241020240827-1743 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 11 Sep 2024 13:43:23 GMT
USER 1001
# Wed, 11 Sep 2024 13:43:23 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 11 Sep 2024 13:43:23 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 11 Sep 2024 13:43:23 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2164747e1ff2ca7eac681bf32f49a500610ebae6a7ec62604a1f098051d7b765`  
		Last Modified: Thu, 19 Sep 2024 20:01:39 GMT  
		Size: 12.2 MB (12156493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb949f759267157c8c5b6da2affd1e2fbb45890cb425c73a09ff662b46558b1e`  
		Last Modified: Thu, 19 Sep 2024 20:01:39 GMT  
		Size: 51.5 MB (51534126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a965409154c3ffae601b19ee5aaead25c0246b90b6f423b74baa889aaf1ef80d`  
		Last Modified: Thu, 19 Sep 2024 20:01:39 GMT  
		Size: 4.9 MB (4898019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13fcc190136f1edb0b40afc7a879bcce6aa6fd85b82da2195325b50600410e3`  
		Last Modified: Thu, 19 Sep 2024 21:00:23 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf37b12e76c899949d411d207bda824b59e04908d7386cdd44b6c82974379f7`  
		Last Modified: Thu, 19 Sep 2024 21:00:23 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d049e90be950d4c0495283a5884c62e8ec28dcec54dd050b60bc50853e83e60`  
		Last Modified: Thu, 19 Sep 2024 21:00:24 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebffafb08936613e8610239d1961e3873587cf01df3cd5080da5a6cc5f2d4b69`  
		Last Modified: Thu, 19 Sep 2024 21:00:23 GMT  
		Size: 31.7 KB (31745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9edf4e9092d86e6cac3d1e4be8e2d41b84707784bbc0fb405860c5d836275d`  
		Last Modified: Thu, 19 Sep 2024 21:00:24 GMT  
		Size: 14.6 MB (14605593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84be5c3db02112179705ed285c7ab3d8b8ba3aa2d19cb552764b9ea92dd174d9`  
		Last Modified: Thu, 19 Sep 2024 21:00:24 GMT  
		Size: 737.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001b4d92f6ab42c557ef1bdc21cc539c38fbe3aa11edf22cc43284d419badd73`  
		Last Modified: Thu, 19 Sep 2024 21:00:24 GMT  
		Size: 10.5 KB (10544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61db7bba4e9f041967cf10f375a940abd73e88cbb604fa4cc34d6fc361449971`  
		Last Modified: Thu, 19 Sep 2024 21:00:24 GMT  
		Size: 2.8 MB (2773565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:kernel-slim-java17-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:e68c4d6eaac315138bba010e64c2b544a46a3213aed2fb4cfb06c8717ad0f8c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 KB (40420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be8791db5142f352d21bfa9febf3f5ecc85d13ad2ef95aa72fcaa33986de1286`

```dockerfile
```

-	Layers:
	-	`sha256:237df13afa2eec7d9203259445be81eb467c775ac873d1add228535a54a34ca5`  
		Last Modified: Thu, 19 Sep 2024 21:00:23 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54918eb73c11f3b037a12650aba20c796a8729d1b98e5689f8756f61bb0eb843`  
		Last Modified: Thu, 19 Sep 2024 21:00:23 GMT  
		Size: 38.7 KB (38663 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:kernel-slim-java17-openj9` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:817f5193f1f02621aa33a0e8759a4ddea73c8ea3ff5de1c851babefe3938de35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.4 MB (109411272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eac6c7eb4caa742eb56c6663a7be68716be62ce34d97a09c99807a99c51bb9c`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 11 Sep 2024 13:43:23 GMT
ARG RELEASE
# Wed, 11 Sep 2024 13:43:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 13:43:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 13:43:23 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 13:43:23 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 13:43:23 GMT
CMD ["/bin/bash"]
# Wed, 11 Sep 2024 13:43:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 11 Sep 2024 13:43:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
ENV JAVA_VERSION=jdk-17.0.12+7_openj9-0.46.1
# Wed, 11 Sep 2024 13:43:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cb2bfe44358158dcaa903e1f9aeb3e895adc1d5ace1f764e0dc1b1aeb4ffb77e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_aarch64_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='29f969c56c1e82587e0fcb1c0253dec413538c9599eaec9fcdb3983d181aad96';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_ppc64le_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='f218a8e1596197a3e89e9eff3ef4dc3e56ff41d7e293261e02cbc589a418998e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_x64_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='1490c54b365dc1c4bfea47412433df79ebfd2c3f85c9f7b1c88ce2d7ae7dee75';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_s390x_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Sep 2024 13:43:23 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 11 Sep 2024 13:43:23 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.95/bin/apache-tomcat-9.0.95.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
USER root
# Wed, 11 Sep 2024 13:43:23 GMT
ARG LIBERTY_VERSION=24.0.0.9
# Wed, 11 Sep 2024 13:43:23 GMT
ARG LIBERTY_SHA=416a2f8dd37d676b9e60c37463f536974a31d2ef
# Wed, 11 Sep 2024 13:43:23 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.9/openliberty-kernel-24.0.0.9.zip
# Wed, 11 Sep 2024 13:43:23 GMT
ARG LIBERTY_BUILD_LABEL=cl241020240827-1743
# Wed, 11 Sep 2024 13:43:23 GMT
ARG OPENJ9_SCC=true
# Wed, 11 Sep 2024 13:43:23 GMT
ARG VERBOSE=false
# Wed, 11 Sep 2024 13:43:23 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl241020240827-1743 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=24.0.0.9
# Wed, 11 Sep 2024 13:43:23 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
# ARGS: LIBERTY_VERSION=24.0.0.9 LIBERTY_SHA=416a2f8dd37d676b9e60c37463f536974a31d2ef LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.9/openliberty-kernel-24.0.0.9.zip LIBERTY_BUILD_LABEL=cl241020240827-1743 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
# ARGS: LIBERTY_VERSION=24.0.0.9 LIBERTY_SHA=416a2f8dd37d676b9e60c37463f536974a31d2ef LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.9/openliberty-kernel-24.0.0.9.zip LIBERTY_BUILD_LABEL=cl241020240827-1743 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 11 Sep 2024 13:43:23 GMT
# ARGS: LIBERTY_VERSION=24.0.0.9 LIBERTY_SHA=416a2f8dd37d676b9e60c37463f536974a31d2ef LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.9/openliberty-kernel-24.0.0.9.zip LIBERTY_BUILD_LABEL=cl241020240827-1743 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
# ARGS: LIBERTY_VERSION=24.0.0.9 LIBERTY_SHA=416a2f8dd37d676b9e60c37463f536974a31d2ef LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.9/openliberty-kernel-24.0.0.9.zip LIBERTY_BUILD_LABEL=cl241020240827-1743 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
# ARGS: LIBERTY_VERSION=24.0.0.9 LIBERTY_SHA=416a2f8dd37d676b9e60c37463f536974a31d2ef LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.9/openliberty-kernel-24.0.0.9.zip LIBERTY_BUILD_LABEL=cl241020240827-1743 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 11 Sep 2024 13:43:23 GMT
USER 1001
# Wed, 11 Sep 2024 13:43:23 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 11 Sep 2024 13:43:23 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 11 Sep 2024 13:43:23 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3831940244be8baa42f9d6629360ed0326dedeb7d18134cfa77184874d97bf6f`  
		Last Modified: Tue, 17 Sep 2024 02:06:03 GMT  
		Size: 12.1 MB (12114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20642fa5f40650d3b2d9c9ff8d86ea87930c0b986bfbbd31aa92bf919ad6154d`  
		Last Modified: Tue, 17 Sep 2024 02:11:45 GMT  
		Size: 47.9 MB (47916904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc107faa922311b6d5ade0aa99f19705957ab2a4030ddfc64d3951188f41172`  
		Last Modified: Thu, 19 Sep 2024 20:11:28 GMT  
		Size: 4.7 MB (4663030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc11180321c53aa19c0843898c0ec3b3734b1b555ac13b7473f6177898375a02`  
		Last Modified: Thu, 19 Sep 2024 21:04:30 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad6102321415f34c5796bb74597384cd42408a3f5288a0d0348ce043d95cd05`  
		Last Modified: Thu, 19 Sep 2024 21:06:29 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4526e09714f2205ce9aa3c5e42a1572fffd8f658a0772039ce1208412a8d5183`  
		Last Modified: Thu, 19 Sep 2024 21:06:29 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e83cf553140471846407acd0b740a14927ef951ff467a0760944124201191c22`  
		Last Modified: Thu, 19 Sep 2024 21:06:29 GMT  
		Size: 42.3 KB (42324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0aac9da0bf1248dc9878734ed98774231cda325ed5f9a607b70a7b1e0bd8fe6`  
		Last Modified: Thu, 19 Sep 2024 21:06:30 GMT  
		Size: 14.6 MB (14605873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb762beced100bcc3ef52dcb847cf33b1d3a76bc5142b9246a31e9d5077aac2`  
		Last Modified: Thu, 19 Sep 2024 21:06:30 GMT  
		Size: 740.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d236daf05ef048d7aeb4f4c1fa9081f824d4c32704122391ff72d7750c7ec32`  
		Last Modified: Thu, 19 Sep 2024 21:06:30 GMT  
		Size: 10.5 KB (10544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a091970c226343c3c32a7ce07484fe78ab3a4a0b3581ac1a4142b862b31acef`  
		Last Modified: Thu, 19 Sep 2024 21:06:31 GMT  
		Size: 2.7 MB (2688405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:kernel-slim-java17-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:41386825a60619788a5f5bb4e747e5848426035146b1e86b7bca46550483e866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c024b758ea8ad81d440c90e223241d6c2e7c571f5e4df6266e7a6f08957818a5`

```dockerfile
```

-	Layers:
	-	`sha256:dadeb1c91cbeb2a30d957c5d1677518a94eddbc8f2ba7e02a2d203525e2cd1df`  
		Last Modified: Thu, 19 Sep 2024 21:06:29 GMT  
		Size: 3.6 MB (3586178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca5368248a188ab389c2566b84be9997531e8093d016899b1ec47789bc29a64`  
		Last Modified: Thu, 19 Sep 2024 21:06:29 GMT  
		Size: 39.0 KB (39024 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:kernel-slim-java17-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:6b0fcfc91b49453c3f1b08c1b12a71f5aae1f9fae0f380ba756712efa94093ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.5 MB (121500910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666737680c0c44117f5801dac4e127457523f6bc3829c189762a10cbcca93f4c`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 11 Sep 2024 13:43:23 GMT
ARG RELEASE
# Wed, 11 Sep 2024 13:43:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 13:43:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 13:43:23 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 13:43:23 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 13:43:23 GMT
CMD ["/bin/bash"]
# Wed, 11 Sep 2024 13:43:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 11 Sep 2024 13:43:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
ENV JAVA_VERSION=jdk-17.0.12+7_openj9-0.46.1
# Wed, 11 Sep 2024 13:43:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cb2bfe44358158dcaa903e1f9aeb3e895adc1d5ace1f764e0dc1b1aeb4ffb77e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_aarch64_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='29f969c56c1e82587e0fcb1c0253dec413538c9599eaec9fcdb3983d181aad96';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_ppc64le_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='f218a8e1596197a3e89e9eff3ef4dc3e56ff41d7e293261e02cbc589a418998e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_x64_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='1490c54b365dc1c4bfea47412433df79ebfd2c3f85c9f7b1c88ce2d7ae7dee75';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_s390x_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Sep 2024 13:43:23 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 11 Sep 2024 13:43:23 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
USER root
# Wed, 11 Sep 2024 13:43:23 GMT
ARG LIBERTY_VERSION=24.0.0.9
# Wed, 11 Sep 2024 13:43:23 GMT
ARG LIBERTY_SHA=416a2f8dd37d676b9e60c37463f536974a31d2ef
# Wed, 11 Sep 2024 13:43:23 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.9/openliberty-kernel-24.0.0.9.zip
# Wed, 11 Sep 2024 13:43:23 GMT
ARG LIBERTY_BUILD_LABEL=cl241020240827-1743
# Wed, 11 Sep 2024 13:43:23 GMT
ARG OPENJ9_SCC=true
# Wed, 11 Sep 2024 13:43:23 GMT
ARG VERBOSE=false
# Wed, 11 Sep 2024 13:43:23 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl241020240827-1743 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=24.0.0.9
# Wed, 11 Sep 2024 13:43:23 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
# ARGS: LIBERTY_VERSION=24.0.0.9 LIBERTY_SHA=416a2f8dd37d676b9e60c37463f536974a31d2ef LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.9/openliberty-kernel-24.0.0.9.zip LIBERTY_BUILD_LABEL=cl241020240827-1743 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
# ARGS: LIBERTY_VERSION=24.0.0.9 LIBERTY_SHA=416a2f8dd37d676b9e60c37463f536974a31d2ef LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.9/openliberty-kernel-24.0.0.9.zip LIBERTY_BUILD_LABEL=cl241020240827-1743 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 11 Sep 2024 13:43:23 GMT
# ARGS: LIBERTY_VERSION=24.0.0.9 LIBERTY_SHA=416a2f8dd37d676b9e60c37463f536974a31d2ef LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.9/openliberty-kernel-24.0.0.9.zip LIBERTY_BUILD_LABEL=cl241020240827-1743 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
# ARGS: LIBERTY_VERSION=24.0.0.9 LIBERTY_SHA=416a2f8dd37d676b9e60c37463f536974a31d2ef LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.9/openliberty-kernel-24.0.0.9.zip LIBERTY_BUILD_LABEL=cl241020240827-1743 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
# ARGS: LIBERTY_VERSION=24.0.0.9 LIBERTY_SHA=416a2f8dd37d676b9e60c37463f536974a31d2ef LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.9/openliberty-kernel-24.0.0.9.zip LIBERTY_BUILD_LABEL=cl241020240827-1743 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 11 Sep 2024 13:43:23 GMT
USER 1001
# Wed, 11 Sep 2024 13:43:23 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 11 Sep 2024 13:43:23 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 11 Sep 2024 13:43:23 GMT
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
	-	`sha256:3e956f85db15bc3def81b35a583203cdacb3b7c13fc265dacab2f17dd60df77d`  
		Last Modified: Tue, 17 Sep 2024 01:23:56 GMT  
		Size: 53.1 MB (53116177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc43e2388662f4cf6daa94c3976105ece62b24da62d716f0aceefb4fbb97183e`  
		Last Modified: Tue, 17 Sep 2024 01:23:55 GMT  
		Size: 3.8 MB (3775444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b6346dbccaeaf183896d7a3257afc04fde6ae8fef8c33e1671ea91186b9cdf3`  
		Last Modified: Tue, 17 Sep 2024 03:46:48 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43fae0e50fc22d510d8a2449bc2a7d8a9a94e66252b01e17cf9a1945aa61435`  
		Last Modified: Tue, 17 Sep 2024 03:50:02 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22d56c735473188b3ac74618619d33835a90b0fefc4d21e303ff4a7d2a2b475`  
		Last Modified: Tue, 17 Sep 2024 03:50:02 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea15d2c5780ae57a3df2ee8e7a5aaae12ecc8287e0dafe9b641cf46d46f7469`  
		Last Modified: Tue, 17 Sep 2024 03:50:02 GMT  
		Size: 36.5 KB (36495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2a7e2c2ad3a233843ab8f5c69e96278c184ddb7f574371ac9b979c67d20842`  
		Last Modified: Tue, 17 Sep 2024 03:50:03 GMT  
		Size: 14.6 MB (14606163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e519362832f50925df0808825d5d2fc1e303487a0777227867d39e27f4eb632`  
		Last Modified: Tue, 17 Sep 2024 03:50:03 GMT  
		Size: 740.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9747c2728fe6722aa14572ec18f739d62661a4130be21dfde27adde47fcadb25`  
		Last Modified: Tue, 17 Sep 2024 03:50:03 GMT  
		Size: 10.6 KB (10558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a2f38d95673da369eb5bb451255bb7be2f955459fa3178b3135536616c4f06`  
		Last Modified: Tue, 17 Sep 2024 03:50:03 GMT  
		Size: 2.6 MB (2608128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:kernel-slim-java17-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:e23671cdd594b351e38055482bf671828ebd6c4e5dd889218b618e8cd233bc5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7144216404d4aec508b87cbf804afe1f0d3bbcbb51509812dec245c593a0908`

```dockerfile
```

-	Layers:
	-	`sha256:93749c1d1dcad7f2b6f89979bf9f8b4d122dd86b7e5e0d80b41162b3301d8054`  
		Last Modified: Tue, 17 Sep 2024 03:50:02 GMT  
		Size: 3.6 MB (3590401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cef10bddce8e69b18c5de94087a1780d03bd9fc2d5e4f59716be7a8aa6dab648`  
		Last Modified: Tue, 17 Sep 2024 03:50:01 GMT  
		Size: 38.7 KB (38703 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:kernel-slim-java17-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:af79519d33da30a0aabdc179cb853cef2f938f381c721b0724963cfe124cd75d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113114236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa03059c065718c01dc47b7d2f73efc145276cd3f8da57d6695e17fc8f36402`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 11 Sep 2024 13:43:23 GMT
ARG RELEASE
# Wed, 11 Sep 2024 13:43:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 13:43:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 13:43:23 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 13:43:23 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 11 Sep 2024 13:43:23 GMT
CMD ["/bin/bash"]
# Wed, 11 Sep 2024 13:43:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 11 Sep 2024 13:43:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
ENV JAVA_VERSION=jdk-17.0.12+7_openj9-0.46.1
# Wed, 11 Sep 2024 13:43:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cb2bfe44358158dcaa903e1f9aeb3e895adc1d5ace1f764e0dc1b1aeb4ffb77e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_aarch64_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='29f969c56c1e82587e0fcb1c0253dec413538c9599eaec9fcdb3983d181aad96';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_ppc64le_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='f218a8e1596197a3e89e9eff3ef4dc3e56ff41d7e293261e02cbc589a418998e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_x64_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='1490c54b365dc1c4bfea47412433df79ebfd2c3f85c9f7b1c88ce2d7ae7dee75';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_s390x_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Sep 2024 13:43:23 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 11 Sep 2024 13:43:23 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.95/bin/apache-tomcat-9.0.95.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
USER root
# Wed, 11 Sep 2024 13:43:23 GMT
ARG LIBERTY_VERSION=24.0.0.9
# Wed, 11 Sep 2024 13:43:23 GMT
ARG LIBERTY_SHA=416a2f8dd37d676b9e60c37463f536974a31d2ef
# Wed, 11 Sep 2024 13:43:23 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.9/openliberty-kernel-24.0.0.9.zip
# Wed, 11 Sep 2024 13:43:23 GMT
ARG LIBERTY_BUILD_LABEL=cl241020240827-1743
# Wed, 11 Sep 2024 13:43:23 GMT
ARG OPENJ9_SCC=true
# Wed, 11 Sep 2024 13:43:23 GMT
ARG VERBOSE=false
# Wed, 11 Sep 2024 13:43:23 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl241020240827-1743 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=24.0.0.9
# Wed, 11 Sep 2024 13:43:23 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
# ARGS: LIBERTY_VERSION=24.0.0.9 LIBERTY_SHA=416a2f8dd37d676b9e60c37463f536974a31d2ef LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.9/openliberty-kernel-24.0.0.9.zip LIBERTY_BUILD_LABEL=cl241020240827-1743 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
# ARGS: LIBERTY_VERSION=24.0.0.9 LIBERTY_SHA=416a2f8dd37d676b9e60c37463f536974a31d2ef LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.9/openliberty-kernel-24.0.0.9.zip LIBERTY_BUILD_LABEL=cl241020240827-1743 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 11 Sep 2024 13:43:23 GMT
# ARGS: LIBERTY_VERSION=24.0.0.9 LIBERTY_SHA=416a2f8dd37d676b9e60c37463f536974a31d2ef LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.9/openliberty-kernel-24.0.0.9.zip LIBERTY_BUILD_LABEL=cl241020240827-1743 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
# ARGS: LIBERTY_VERSION=24.0.0.9 LIBERTY_SHA=416a2f8dd37d676b9e60c37463f536974a31d2ef LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.9/openliberty-kernel-24.0.0.9.zip LIBERTY_BUILD_LABEL=cl241020240827-1743 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
# ARGS: LIBERTY_VERSION=24.0.0.9 LIBERTY_SHA=416a2f8dd37d676b9e60c37463f536974a31d2ef LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.9/openliberty-kernel-24.0.0.9.zip LIBERTY_BUILD_LABEL=cl241020240827-1743 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 11 Sep 2024 13:43:23 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 11 Sep 2024 13:43:23 GMT
USER 1001
# Wed, 11 Sep 2024 13:43:23 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 11 Sep 2024 13:43:23 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 11 Sep 2024 13:43:23 GMT
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
	-	`sha256:bf306d6b55fcd4409a3d7914177a321a344e69fa7c2a2b6fcbfa5871e82a7fab`  
		Last Modified: Tue, 17 Sep 2024 02:04:33 GMT  
		Size: 50.5 MB (50470509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b37cc8f8b8f9d1c5741bfa4a1e93d8c6659c980ab4c801503926c834f02cb30`  
		Last Modified: Thu, 19 Sep 2024 20:15:44 GMT  
		Size: 5.0 MB (5033582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33f7f20e080c0b139bdbc72734b8b7126c907707670b744422071c85b1380db`  
		Last Modified: Thu, 19 Sep 2024 21:06:11 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7f8f8a2edb13723d925270bd2a54b2fee22f09c19e1bdc60469c4b6911dae5`  
		Last Modified: Thu, 19 Sep 2024 21:09:13 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9737b65c967000f1d4709499546744ef1f46c086e2609eba75e0a55da6eb09f6`  
		Last Modified: Thu, 19 Sep 2024 21:09:13 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0caa479ea23988854d078cb4e58aa03d364f561fa180f3d0c42f20414702f167`  
		Last Modified: Thu, 19 Sep 2024 21:09:13 GMT  
		Size: 33.1 KB (33111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e7b57e882fb6b690e8a8c3fdea00453c1871d1a3efc4cd16b3484038aee12a`  
		Last Modified: Thu, 19 Sep 2024 21:09:14 GMT  
		Size: 14.6 MB (14605783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8dd8922fa3fff05cd143f3148d814be6db596762ab99668766c727d2b227e07`  
		Last Modified: Thu, 19 Sep 2024 21:09:14 GMT  
		Size: 738.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160710539d2d751f570f5a0f90cc65bc5b4549890c777f99ce7e198304da07fb`  
		Last Modified: Thu, 19 Sep 2024 21:09:14 GMT  
		Size: 10.5 KB (10549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940f6b02e97388cc1ea0424fb7b9c9998468a1b14876f031b014189f7440ad09`  
		Last Modified: Thu, 19 Sep 2024 21:09:14 GMT  
		Size: 2.7 MB (2743912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:kernel-slim-java17-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:7ae3e43bf095746904ed8766e98ed2932880e25fd670e3524ce9f58971569618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3624615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e656e09acd1c5dd83f1a3d255859f18c0e5e8cc963890f20c0b0ec64c8eb7c3`

```dockerfile
```

-	Layers:
	-	`sha256:e85f2ecba6753acb54376ab3f04475f9d59e3c09bc7760fc393891ed2d539e70`  
		Last Modified: Thu, 19 Sep 2024 21:09:13 GMT  
		Size: 3.6 MB (3585952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be9a97600d278e289b5e44631c9c3da3bc323b4758538b3c143e1441b8e69166`  
		Last Modified: Thu, 19 Sep 2024 21:09:13 GMT  
		Size: 38.7 KB (38663 bytes)  
		MIME: application/vnd.in-toto+json
