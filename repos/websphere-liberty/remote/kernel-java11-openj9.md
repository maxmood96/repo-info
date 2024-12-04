## `websphere-liberty:kernel-java11-openj9`

```console
$ docker pull websphere-liberty@sha256:393d389699191f2fc82ebf43813a25295abfdd64a7b9eb9b64f6cca33beef396
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

### `websphere-liberty:kernel-java11-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:3d944cc236170ca229b5491bbe82de8bcb9db20453033f48ee4ba244206c009f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118765351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2341baa2eb0b16e5cd0db7298616117fa64d8b2e24c22f1376fa3627a6ec2428`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

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
# Thu, 14 Nov 2024 10:27:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Nov 2024 10:27:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Nov 2024 10:27:45 GMT
ENV JAVA_VERSION=jdk-11.0.25+9_openj9-0.48.0
# Thu, 14 Nov 2024 10:27:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3ebe7dc3fc6d7a0145d8834d01ca5adda19c1812af9a4f63655bc4de463377b6';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_aarch64_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='451c6da5d286af654d857c2383698c19e9f05070b8e018f73f82ab1df1c51ba3';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_ppc64le_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7d8407bbc68303e84615d1981abbdda690236edfcff5535789dc7915a3c4f629';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_x64_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='28c3adeefd79d0054cd8f5b5de0a95277ae19a53e1f503a15d4955c38a9e715d';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_s390x_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 14 Nov 2024 10:27:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Nov 2024 10:27:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 14 Nov 2024 10:27:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="537dbbfc03b37312c2ec282c6906828298cb74e42aca6e3e6835d44bf6923fd8c5db77e98bf6ce9ef19e1922729de53b20546149176e07ac04087df786a62fd9";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.97/bin/apache-tomcat-9.0.97.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
USER root
# Tue, 03 Dec 2024 20:42:13 GMT
ARG VERBOSE=false
# Tue, 03 Dec 2024 20:42:13 GMT
ARG OPENJ9_SCC=true
# Tue, 03 Dec 2024 20:42:13 GMT
ARG LIBERTY_VERSION=24.0.0.12
# Tue, 03 Dec 2024 20:42:13 GMT
ARG LIBERTY_BUILD_LABEL=cl241220241119-0657
# Tue, 03 Dec 2024 20:42:13 GMT
ARG LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4
# Tue, 03 Dec 2024 20:42:13 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.12 org.opencontainers.image.revision=cl241220241119-0657 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Tue, 03 Dec 2024 20:42:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Tue, 03 Dec 2024 20:42:13 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.12 BuildLabel=cl241220241119-0657
# Tue, 03 Dec 2024 20:42:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.12 LIBERTY_BUILD_LABEL=cl241220241119-0657 LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
ARG LIBERTY_URL
# Tue, 03 Dec 2024 20:42:13 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 03 Dec 2024 20:42:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.12 LIBERTY_BUILD_LABEL=cl241220241119-0657 LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 03 Dec 2024 20:42:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.12 LIBERTY_BUILD_LABEL=cl241220241119-0657 LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.12 LIBERTY_BUILD_LABEL=cl241220241119-0657 LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.12 LIBERTY_BUILD_LABEL=cl241220241119-0657 LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 03 Dec 2024 20:42:13 GMT
USER 1001
# Tue, 03 Dec 2024 20:42:13 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 03 Dec 2024 20:42:13 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 03 Dec 2024 20:42:13 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a4199c8f2c5e2b0ae278966cfde14054e3ccd8774336763b3dd3def4309563`  
		Last Modified: Mon, 18 Nov 2024 19:05:55 GMT  
		Size: 12.2 MB (12175004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc2d2ffb2a260cd5dac60f3d3e71903937560fb78710bc70a17a827638d5b4c`  
		Last Modified: Mon, 18 Nov 2024 19:05:56 GMT  
		Size: 52.3 MB (52287848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c93bba8d2ba60bc13741b1c6380d8815dae95eb87f71e4bb537e02ab485dde`  
		Last Modified: Mon, 18 Nov 2024 19:05:55 GMT  
		Size: 4.4 MB (4447330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebeb4e3b806b8d9f018570943194024dc4c26178277e054a9fca0ce51b79722`  
		Last Modified: Tue, 03 Dec 2024 22:29:07 GMT  
		Size: 31.7 KB (31748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483b723c660252b93e479aa7163d4a4522b550ed281db5c54d3f6270e7b2c2b7`  
		Last Modified: Tue, 03 Dec 2024 22:29:08 GMT  
		Size: 17.4 MB (17446658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0a4eda07fe1f9327999b9f5bc84d19d8b14ed487a06f04dbde9b28a1467dd4`  
		Last Modified: Tue, 03 Dec 2024 22:29:07 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f98dbc6f8f0f9ffa49856e12cdfcf3fcda330000764b2345fab476f5f63f2c`  
		Last Modified: Tue, 03 Dec 2024 22:29:07 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2bc1962783c492df448a97f9de81e68b10526378549b25ddeca9bd6d0d37a6`  
		Last Modified: Tue, 03 Dec 2024 22:29:08 GMT  
		Size: 11.8 KB (11833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1162e98e8de0f20c39df30b14d7030afa852383ff95222883643f98efec429`  
		Last Modified: Tue, 03 Dec 2024 22:29:08 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a850811ca34912fb5c6a88a0f3d8dc25eb1baade70e2d7cd68853892fdce6d`  
		Last Modified: Tue, 03 Dec 2024 22:29:08 GMT  
		Size: 12.6 KB (12636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fae52330980dc1ceb919607dc857fe6d7953fcdc0cc0f50ff1149e8bdf7c0e0`  
		Last Modified: Tue, 03 Dec 2024 22:29:09 GMT  
		Size: 2.8 MB (2814358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:d689c7e31dc646ddc0a91f95a9825bca97276e5d44d767bc73d04a4b127440a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3780257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf55ad7d938293b9f91c0b531afb205615f35352577f4b4ce6b1234a9bc6e8b2`

```dockerfile
```

-	Layers:
	-	`sha256:7c8bc87db4341ad53cb0877456ff7c767cc8066c4e8b83321f778cf31fdbc3c8`  
		Last Modified: Tue, 03 Dec 2024 22:29:07 GMT  
		Size: 3.7 MB (3740265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6be6bdfd86246c136ebb66e947afd063be73b72ce4e78af8284a312bb49db4f6`  
		Last Modified: Tue, 03 Dec 2024 22:29:07 GMT  
		Size: 40.0 KB (39992 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java11-openj9` - linux; arm64 variant v8

```console
$ docker pull websphere-liberty@sha256:a3e60c92f6689f1aae6001a30489ce3aea35f9fb2a7f91e769c36fcb8630e7b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112308386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa644b3ecc0544517422bf0fd85d7ba1f3bccea34d594b89a13aed075e97576`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

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
# Wed, 06 Nov 2024 14:57:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Nov 2024 14:57:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
ENV JAVA_VERSION=jdk-11.0.25+9_openj9-0.48.0
# Wed, 06 Nov 2024 14:57:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3ebe7dc3fc6d7a0145d8834d01ca5adda19c1812af9a4f63655bc4de463377b6';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_aarch64_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='451c6da5d286af654d857c2383698c19e9f05070b8e018f73f82ab1df1c51ba3';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_ppc64le_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7d8407bbc68303e84615d1981abbdda690236edfcff5535789dc7915a3c4f629';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_x64_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='28c3adeefd79d0054cd8f5b5de0a95277ae19a53e1f503a15d4955c38a9e715d';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_s390x_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 14:57:10 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 06 Nov 2024 14:57:10 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="537dbbfc03b37312c2ec282c6906828298cb74e42aca6e3e6835d44bf6923fd8c5db77e98bf6ce9ef19e1922729de53b20546149176e07ac04087df786a62fd9";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.97/bin/apache-tomcat-9.0.97.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
USER root
# Wed, 06 Nov 2024 14:57:10 GMT
ARG VERBOSE=false
# Wed, 06 Nov 2024 14:57:10 GMT
ARG OPENJ9_SCC=true
# Wed, 06 Nov 2024 14:57:10 GMT
ARG LIBERTY_VERSION=24.0.0.11
# Wed, 06 Nov 2024 14:57:10 GMT
ARG LIBERTY_BUILD_LABEL=cl241120241021-1102
# Wed, 06 Nov 2024 14:57:10 GMT
ARG LIBERTY_SHA=cc5790346b45f63d093cf8d6a528a7730a1dc570
# Wed, 06 Nov 2024 14:57:10 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.11 org.opencontainers.image.revision=cl241120241021-1102 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 06 Nov 2024 14:57:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 06 Nov 2024 14:57:10 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.11 BuildLabel=cl241120241021-1102
# Wed, 06 Nov 2024 14:57:10 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.11 LIBERTY_BUILD_LABEL=cl241120241021-1102 LIBERTY_SHA=cc5790346b45f63d093cf8d6a528a7730a1dc570
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
ARG LIBERTY_URL
# Wed, 06 Nov 2024 14:57:10 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 06 Nov 2024 14:57:10 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.11 LIBERTY_BUILD_LABEL=cl241120241021-1102 LIBERTY_SHA=cc5790346b45f63d093cf8d6a528a7730a1dc570 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 06 Nov 2024 14:57:10 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.11 LIBERTY_BUILD_LABEL=cl241120241021-1102 LIBERTY_SHA=cc5790346b45f63d093cf8d6a528a7730a1dc570 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.11 LIBERTY_BUILD_LABEL=cl241120241021-1102 LIBERTY_SHA=cc5790346b45f63d093cf8d6a528a7730a1dc570 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.11 LIBERTY_BUILD_LABEL=cl241120241021-1102 LIBERTY_SHA=cc5790346b45f63d093cf8d6a528a7730a1dc570 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 06 Nov 2024 14:57:10 GMT
USER 1001
# Wed, 06 Nov 2024 14:57:10 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 06 Nov 2024 14:57:10 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 06 Nov 2024 14:57:10 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
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
	-	`sha256:b3509dfe81f20ff70265547e8cb2cf4e50fdef4f573c0c8ee3b091726899f2eb`  
		Last Modified: Mon, 18 Nov 2024 19:19:55 GMT  
		Size: 48.4 MB (48398548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bca6c8ad687898f8c4470c3ba7cfdad73f0af8e368950f191dd425f820c0d58`  
		Last Modified: Mon, 18 Nov 2024 19:19:54 GMT  
		Size: 4.2 MB (4153850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e791cd6c04a4f5cf9df7135f2661c8ff937d7571915814bdc71773f7300bb0`  
		Last Modified: Mon, 18 Nov 2024 21:31:39 GMT  
		Size: 42.3 KB (42325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41a9440c6a3ff3786aae07334867f9ff4ac93b60fd8417c893f4f828662add0`  
		Last Modified: Mon, 18 Nov 2024 21:31:41 GMT  
		Size: 17.4 MB (17435584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1932597cf2cd2c954055e2d7c2987e0a56ea6dd84b97570c4409cbd6064fc9`  
		Last Modified: Mon, 18 Nov 2024 21:31:39 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1deeb3b2e210216a60d8f8e9c7dda3a1aa7d4822e41967bc833c553dac0517`  
		Last Modified: Mon, 18 Nov 2024 21:31:39 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5763ea93be06e67d63a4764c0e0bca22cad85c4bb56969ca4374c36eed3c9da1`  
		Last Modified: Mon, 18 Nov 2024 21:31:40 GMT  
		Size: 11.8 KB (11833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370422a67726faf385699949eac3029677dc4743700dfd9f79111dd22e225544`  
		Last Modified: Mon, 18 Nov 2024 21:31:40 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15b25ee57725a658e5e4dee42a00d83606f61f7fe3fe4cb2cf7abaa0aa41063`  
		Last Modified: Mon, 18 Nov 2024 21:31:40 GMT  
		Size: 12.6 KB (12640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e616ddd516c88497052c2e3b6bde736f4018a2c62d195995922fd851d019012d`  
		Last Modified: Mon, 18 Nov 2024 21:31:41 GMT  
		Size: 2.8 MB (2764793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:39e2ddca9f56b1bdc6e7b7d1f33a1ead3cdab788f4621ffc069ab6b2b4686a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3771876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41a105d427b288532ecaf3982b5600ebdd13f18e414295cd76d3e4971824e9f`

```dockerfile
```

-	Layers:
	-	`sha256:63c8ddc37b908b7456e12021c9a9a0fde78f5672ec52206df3744c837711e4f0`  
		Last Modified: Mon, 18 Nov 2024 21:31:39 GMT  
		Size: 3.7 MB (3731742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4de071fc3ca30eccef1313b5def9b10759ae5fe3a0985c822cea1231e6010e98`  
		Last Modified: Mon, 18 Nov 2024 21:31:39 GMT  
		Size: 40.1 KB (40134 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java11-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:488dd7dd8f615d8842b10ab979e2ff89b91dd64f782c65f056b0f81d9ae674d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124550566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8998a19e7bd37e93288cd0f279cce90f108bafbd28d5ad93d35ae251b9e234e3`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

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
# Thu, 14 Nov 2024 10:27:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Nov 2024 10:27:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Nov 2024 10:27:45 GMT
ENV JAVA_VERSION=jdk-11.0.25+9_openj9-0.48.0
# Thu, 14 Nov 2024 10:27:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3ebe7dc3fc6d7a0145d8834d01ca5adda19c1812af9a4f63655bc4de463377b6';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_aarch64_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='451c6da5d286af654d857c2383698c19e9f05070b8e018f73f82ab1df1c51ba3';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_ppc64le_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7d8407bbc68303e84615d1981abbdda690236edfcff5535789dc7915a3c4f629';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_x64_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='28c3adeefd79d0054cd8f5b5de0a95277ae19a53e1f503a15d4955c38a9e715d';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_s390x_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 14 Nov 2024 10:27:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Nov 2024 10:27:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 14 Nov 2024 10:27:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="537dbbfc03b37312c2ec282c6906828298cb74e42aca6e3e6835d44bf6923fd8c5db77e98bf6ce9ef19e1922729de53b20546149176e07ac04087df786a62fd9";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.97/bin/apache-tomcat-9.0.97.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
USER root
# Tue, 03 Dec 2024 20:42:13 GMT
ARG VERBOSE=false
# Tue, 03 Dec 2024 20:42:13 GMT
ARG OPENJ9_SCC=true
# Tue, 03 Dec 2024 20:42:13 GMT
ARG LIBERTY_VERSION=24.0.0.12
# Tue, 03 Dec 2024 20:42:13 GMT
ARG LIBERTY_BUILD_LABEL=cl241220241119-0657
# Tue, 03 Dec 2024 20:42:13 GMT
ARG LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4
# Tue, 03 Dec 2024 20:42:13 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.12 org.opencontainers.image.revision=cl241220241119-0657 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Tue, 03 Dec 2024 20:42:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Tue, 03 Dec 2024 20:42:13 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.12 BuildLabel=cl241220241119-0657
# Tue, 03 Dec 2024 20:42:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.12 LIBERTY_BUILD_LABEL=cl241220241119-0657 LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
ARG LIBERTY_URL
# Tue, 03 Dec 2024 20:42:13 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 03 Dec 2024 20:42:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.12 LIBERTY_BUILD_LABEL=cl241220241119-0657 LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 03 Dec 2024 20:42:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.12 LIBERTY_BUILD_LABEL=cl241220241119-0657 LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.12 LIBERTY_BUILD_LABEL=cl241220241119-0657 LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.12 LIBERTY_BUILD_LABEL=cl241220241119-0657 LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 03 Dec 2024 20:42:13 GMT
USER 1001
# Tue, 03 Dec 2024 20:42:13 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 03 Dec 2024 20:42:13 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 03 Dec 2024 20:42:13 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
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
	-	`sha256:0bcc6c0cfcef2e3ac890c37eb33575f3292a278705265bc793d8fa463de4084e`  
		Last Modified: Mon, 18 Nov 2024 19:17:50 GMT  
		Size: 3.4 MB (3422807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410445f7f7f9bdb3c9314cf0c48019cf0b37b912fd3036bb6bfb840c04f591e2`  
		Last Modified: Wed, 04 Dec 2024 00:08:55 GMT  
		Size: 36.5 KB (36498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da79a5f27ebca260be4b44678e86b46dda128cafb1f9f25f6f2daaa24fccc2f`  
		Last Modified: Wed, 04 Dec 2024 00:08:58 GMT  
		Size: 17.4 MB (17447240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4876edae9e35c4fcff34cf4fdfdbcfaf63e01eee258ee3d6f2f0751e6cf03679`  
		Last Modified: Wed, 04 Dec 2024 00:08:55 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07890eabeef69ebde928e60e09b474cb1815481b82c36d8b713d97dfa50ae5e`  
		Last Modified: Wed, 04 Dec 2024 00:08:55 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc98a2f267d0f1303a5757b11e412781d7dc04aae1477efccc01d29215fbfac3`  
		Last Modified: Wed, 04 Dec 2024 00:08:55 GMT  
		Size: 11.8 KB (11831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eac48268e4433b6d2e15d56394a8dafe8cfcdcfb7f67a68e5a5ea4058ebbd1f`  
		Last Modified: Wed, 04 Dec 2024 00:08:56 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39037a3baff47ce6bd55b1c0ff88ede738713f99945a3a1b65c4a9c3314e95d`  
		Last Modified: Wed, 04 Dec 2024 00:08:56 GMT  
		Size: 12.6 KB (12639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480193be6a9502f89f5aaa4ec1d26ca0a2b295efd76fdfd7ed4bb3a0cb41ece3`  
		Last Modified: Wed, 04 Dec 2024 00:08:57 GMT  
		Size: 2.7 MB (2685037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:1bdbc464fda0ad02bf11a5c127dc70f1ebea4e52ce30f70c6ca25b705b6898be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3777040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b40e778e040e0da972c1388a74113a4228ba4e271118079b9f7175213631d6c9`

```dockerfile
```

-	Layers:
	-	`sha256:4d8b06d558b7bf39fa28728fc2901771e70e60fca554f4c717dddc7724ee6378`  
		Last Modified: Wed, 04 Dec 2024 00:08:55 GMT  
		Size: 3.7 MB (3737006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f43687316c8bb34f9c8a025b0bebe1c215c565b105612277d878a8cf898a835e`  
		Last Modified: Wed, 04 Dec 2024 00:08:55 GMT  
		Size: 40.0 KB (40034 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java11-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:5ae24efb16905a726b828b6f824f23cec908bf388a57a2fdfbea7382e385efd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (115963067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6960fc4d28d0df94461a6b460db4c624cab4f7a08a584e6d1f5d9357904454ed`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

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
# Thu, 14 Nov 2024 10:27:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Nov 2024 10:27:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Nov 2024 10:27:45 GMT
ENV JAVA_VERSION=jdk-11.0.25+9_openj9-0.48.0
# Thu, 14 Nov 2024 10:27:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3ebe7dc3fc6d7a0145d8834d01ca5adda19c1812af9a4f63655bc4de463377b6';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_aarch64_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='451c6da5d286af654d857c2383698c19e9f05070b8e018f73f82ab1df1c51ba3';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_ppc64le_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7d8407bbc68303e84615d1981abbdda690236edfcff5535789dc7915a3c4f629';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_x64_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='28c3adeefd79d0054cd8f5b5de0a95277ae19a53e1f503a15d4955c38a9e715d';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_s390x_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 14 Nov 2024 10:27:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Nov 2024 10:27:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 14 Nov 2024 10:27:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="537dbbfc03b37312c2ec282c6906828298cb74e42aca6e3e6835d44bf6923fd8c5db77e98bf6ce9ef19e1922729de53b20546149176e07ac04087df786a62fd9";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.97/bin/apache-tomcat-9.0.97.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
USER root
# Tue, 03 Dec 2024 20:42:13 GMT
ARG VERBOSE=false
# Tue, 03 Dec 2024 20:42:13 GMT
ARG OPENJ9_SCC=true
# Tue, 03 Dec 2024 20:42:13 GMT
ARG LIBERTY_VERSION=24.0.0.12
# Tue, 03 Dec 2024 20:42:13 GMT
ARG LIBERTY_BUILD_LABEL=cl241220241119-0657
# Tue, 03 Dec 2024 20:42:13 GMT
ARG LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4
# Tue, 03 Dec 2024 20:42:13 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.12 org.opencontainers.image.revision=cl241220241119-0657 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Tue, 03 Dec 2024 20:42:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Tue, 03 Dec 2024 20:42:13 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.12 BuildLabel=cl241220241119-0657
# Tue, 03 Dec 2024 20:42:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.12 LIBERTY_BUILD_LABEL=cl241220241119-0657 LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
ARG LIBERTY_URL
# Tue, 03 Dec 2024 20:42:13 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 03 Dec 2024 20:42:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.12 LIBERTY_BUILD_LABEL=cl241220241119-0657 LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 03 Dec 2024 20:42:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.12 LIBERTY_BUILD_LABEL=cl241220241119-0657 LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.12 LIBERTY_BUILD_LABEL=cl241220241119-0657 LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.12 LIBERTY_BUILD_LABEL=cl241220241119-0657 LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 03 Dec 2024 20:42:13 GMT
USER 1001
# Tue, 03 Dec 2024 20:42:13 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 03 Dec 2024 20:42:13 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 03 Dec 2024 20:42:13 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
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
	-	`sha256:8fe31ed1a1f1ca178fc57d38d5022f6e112e9ea0a3e2f553454620dc2aa44580`  
		Last Modified: Mon, 18 Nov 2024 19:40:33 GMT  
		Size: 50.9 MB (50865384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64452b582f5285409403cd423591914a3bdd025d56cb97a0173414cb612d1a4a`  
		Last Modified: Mon, 18 Nov 2024 19:40:32 GMT  
		Size: 4.6 MB (4563030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf9aac3549db737d950b9f0b64ebc9524746156dd29552d30b127c9d34ece70`  
		Last Modified: Tue, 03 Dec 2024 23:08:18 GMT  
		Size: 33.1 KB (33114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52dd3add9574240857eb1267b374ea91f35576a3430e1c0fcbfd071b29cd49ec`  
		Last Modified: Tue, 03 Dec 2024 23:08:18 GMT  
		Size: 17.4 MB (17446841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d39d7ba05b629af909f73e7a8dc7ec76d68557aceff0a7a999ed1afd9f56558`  
		Last Modified: Tue, 03 Dec 2024 23:08:18 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b860ffce4d0627bf27792353ad3ef97adf984fc4e5fc6b3f0c0db444501cb427`  
		Last Modified: Tue, 03 Dec 2024 23:08:18 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a1671e25daeeed41858fb6e1f94dff2306eb635f8e81e9fe2ac3844af1005f`  
		Last Modified: Tue, 03 Dec 2024 23:08:19 GMT  
		Size: 11.8 KB (11834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a074848658dad566653a563fee235a478d404e3cf2b214bca715ca2fc8ba87`  
		Last Modified: Tue, 03 Dec 2024 23:08:19 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07982d7ccf06175d702ac6158ab36e48e46b2ad81d0881fe8d19e5cc6592a871`  
		Last Modified: Tue, 03 Dec 2024 23:08:19 GMT  
		Size: 12.6 KB (12644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d742a7fb46d8d3e5116d3e7f47f6734afbd745f6e92667ccf9e2f94a5c5342`  
		Last Modified: Tue, 03 Dec 2024 23:08:20 GMT  
		Size: 2.8 MB (2822739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:8981fb9779c95a74b27b9d0e59d7598624bb80618a0f511c870ae0813f15fec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3773542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcdda8699687eae374bda086e6f9ed06423cbd3905d7dc2636ee034e1f55827e`

```dockerfile
```

-	Layers:
	-	`sha256:d4b5a50fff5eca4aad37860ebf8e23b25cb9e7d735a58bce7093ef9d90614097`  
		Last Modified: Tue, 03 Dec 2024 23:08:18 GMT  
		Size: 3.7 MB (3733548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fae2fe3a991c120c4b5fff1ba7699f113c61077278371686c36adb8be7f7370`  
		Last Modified: Tue, 03 Dec 2024 23:08:18 GMT  
		Size: 40.0 KB (39994 bytes)  
		MIME: application/vnd.in-toto+json
