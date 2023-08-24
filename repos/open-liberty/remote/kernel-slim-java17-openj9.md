## `open-liberty:kernel-slim-java17-openj9`

```console
$ docker pull open-liberty@sha256:d5eb9d45aefa7a167dbb460be4092f2f10127114f7b48a0c9edfeb46ee878b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `open-liberty:kernel-slim-java17-openj9` - linux; amd64

```console
$ docker pull open-liberty@sha256:470c78cabc1e5ded0cc0e8c369a07fe8132fb8918353919d44054213a3677e0a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112981617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dbf3bdb1dc1cca10ddaf2dc11095976ac65246a44329a7de321826522f50c7a`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 04 Aug 2023 04:52:57 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:52:59 GMT
ADD file:bb1fa1d9d012ae826908afdce8c9fa2feebf221b2ab032e1535255905144411a in / 
# Fri, 04 Aug 2023 04:53:00 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 15:47:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 16 Aug 2023 15:47:56 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 23 Aug 2023 20:49:06 GMT
ENV JAVA_VERSION=jdk-17.0.8+7_openj9-0.40.0
# Wed, 23 Aug 2023 20:52:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b8904df2fee0797e493e3482fddb873b25d1e05f27053a2d96a25310c2dce3d4';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.8%2B7_openj9-0.40.0/ibm-semeru-open-jre_aarch64_linux_17.0.8_7_openj9-0.40.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='0986b451944deac0832c2905f1497fddb3ab7c0f63cd9fad707072381c9948a1';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.8%2B7_openj9-0.40.0/ibm-semeru-open-jre_ppc64le_linux_17.0.8_7_openj9-0.40.0.tar.gz';          ;;        amd64|x86_64)          ESUM='461aab09409b3ac26ded0ca921171e141c6b1400a17d8026e924109518b365d4';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.8%2B7_openj9-0.40.0/ibm-semeru-open-jre_x64_linux_17.0.8_7_openj9-0.40.0.tar.gz';          ;;        s390x)          ESUM='c759ed79d237d2e308869b9c1db12f8af4210d2ba08d293ad5d0f90b5eb1ead1';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.8%2B7_openj9-0.40.0/ibm-semeru-open-jre_s390x_linux_17.0.8_7_openj9-0.40.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 23 Aug 2023 20:52:08 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Aug 2023 20:52:08 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 23 Aug 2023 20:52:44 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 23 Aug 2023 21:24:42 GMT
USER root
# Wed, 23 Aug 2023 23:44:48 GMT
ARG LIBERTY_VERSION=23.0.0.8
# Wed, 23 Aug 2023 23:44:48 GMT
ARG LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a
# Wed, 23 Aug 2023 23:44:48 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip
# Wed, 23 Aug 2023 23:44:48 GMT
ARG LIBERTY_BUILD_LABEL=cl230820230807-0401
# Wed, 23 Aug 2023 23:44:48 GMT
ARG OPENJ9_SCC=true
# Wed, 23 Aug 2023 23:44:49 GMT
ARG VERBOSE=false
# Wed, 23 Aug 2023 23:44:49 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl230820230807-0401 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=23.0.0.8
# Wed, 23 Aug 2023 23:44:49 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Wed, 23 Aug 2023 23:44:49 GMT
COPY dir:a51a46b81cfa5e03910d4f938a784aacd5cb102fab83ec37bb694f14e7486355 in /opt/ol/helpers 
# Wed, 23 Aug 2023 23:44:49 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Wed, 23 Aug 2023 23:44:50 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Wed, 23 Aug 2023 23:44:56 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Wed, 23 Aug 2023 23:44:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 23 Aug 2023 23:44:57 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Wed, 23 Aug 2023 23:44:58 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Wed, 23 Aug 2023 23:45:03 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Wed, 23 Aug 2023 23:45:03 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 23 Aug 2023 23:45:03 GMT
USER 1001
# Wed, 23 Aug 2023 23:45:03 GMT
EXPOSE 9080 9443
# Wed, 23 Aug 2023 23:45:04 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 23 Aug 2023 23:45:04 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:99de9192b4afd13ed65aeae58d55b38e5231eb97a743921357b7d5b4c0c903c4`  
		Last Modified: Fri, 04 Aug 2023 09:25:19 GMT  
		Size: 30.4 MB (30437960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab3fd228352238bb1856524b5a72c3fc8010fcaf4d2e94b2b3f4fa5561a6566`  
		Last Modified: Wed, 16 Aug 2023 15:56:02 GMT  
		Size: 12.2 MB (12155838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae27da37eb6a0901a83ced53d135ec7a0cff4c4da9fff23a27ee313c26336d8`  
		Last Modified: Wed, 23 Aug 2023 21:05:05 GMT  
		Size: 48.6 MB (48640969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece307c1c060d009aacd936e5a5ed9aafe8085bc7488ca220b95ec7b1a6584b8`  
		Last Modified: Wed, 23 Aug 2023 21:04:58 GMT  
		Size: 4.8 MB (4843260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6597fd82f8d74e1e4742c74936484043f4bd584b21ce89e053bbc48334f10e`  
		Last Modified: Wed, 23 Aug 2023 23:50:03 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ea2bc1101a064742eb414cf5342aa27430376f55df0217e58adca76208e4ec`  
		Last Modified: Wed, 23 Aug 2023 23:50:03 GMT  
		Size: 8.9 KB (8935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb027e66b07407433ec911299bb98961f0555bbc072cb9a3b674ea1ee7273374`  
		Last Modified: Wed, 23 Aug 2023 23:50:03 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33cd048e3e9742f69ef59ee75393bfa0ba767fcd8a2d808809acd5edb19f76b6`  
		Last Modified: Wed, 23 Aug 2023 23:50:01 GMT  
		Size: 31.7 KB (31749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec62cc08f6a54485a422ecaeab623538793e9efacf840b583e19bb7b3d2ab22`  
		Last Modified: Wed, 23 Aug 2023 23:50:03 GMT  
		Size: 14.2 MB (14218466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89d749606396187338ee3d87ec37211fa03247310ffe0ee928a781cfd2b6fa7`  
		Last Modified: Wed, 23 Aug 2023 23:50:01 GMT  
		Size: 867.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea711bfee41ed31569ff941e624e8230cf1ac97f9755b7e8d95449296ecf328a`  
		Last Modified: Wed, 23 Aug 2023 23:50:01 GMT  
		Size: 10.0 KB (10019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c8b76cfe6d889dd671eafebe585b29315c66e5c7c54c79bac4f6a2f7d9832bc`  
		Last Modified: Wed, 23 Aug 2023 23:50:02 GMT  
		Size: 2.6 MB (2632216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:kernel-slim-java17-openj9` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:8176ab3de07c2ff7270a39fa4503abdb6f824b3eda7aac240caf22f2fcc6afcc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.8 MB (108778903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bf1657eafbc937fd255bf577088ed1baa1d0bf2e7c75ad2c372ce937eaa584`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 04 Aug 2023 04:51:14 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:51:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:51:18 GMT
ADD file:5cf7797cf86362218d2bd85debeff136ee897af7eef95a0b8baab9f9457c3e89 in / 
# Fri, 04 Aug 2023 04:51:18 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 14:30:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 16 Aug 2023 14:30:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 23 Aug 2023 20:05:05 GMT
ENV JAVA_VERSION=jdk-17.0.8+7_openj9-0.40.0
# Wed, 23 Aug 2023 20:07:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b8904df2fee0797e493e3482fddb873b25d1e05f27053a2d96a25310c2dce3d4';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.8%2B7_openj9-0.40.0/ibm-semeru-open-jre_aarch64_linux_17.0.8_7_openj9-0.40.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='0986b451944deac0832c2905f1497fddb3ab7c0f63cd9fad707072381c9948a1';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.8%2B7_openj9-0.40.0/ibm-semeru-open-jre_ppc64le_linux_17.0.8_7_openj9-0.40.0.tar.gz';          ;;        amd64|x86_64)          ESUM='461aab09409b3ac26ded0ca921171e141c6b1400a17d8026e924109518b365d4';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.8%2B7_openj9-0.40.0/ibm-semeru-open-jre_x64_linux_17.0.8_7_openj9-0.40.0.tar.gz';          ;;        s390x)          ESUM='c759ed79d237d2e308869b9c1db12f8af4210d2ba08d293ad5d0f90b5eb1ead1';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.8%2B7_openj9-0.40.0/ibm-semeru-open-jre_s390x_linux_17.0.8_7_openj9-0.40.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 23 Aug 2023 20:07:44 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Aug 2023 20:07:44 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 23 Aug 2023 20:08:27 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 23 Aug 2023 21:26:01 GMT
USER root
# Wed, 23 Aug 2023 23:57:38 GMT
ARG LIBERTY_VERSION=23.0.0.8
# Wed, 23 Aug 2023 23:57:38 GMT
ARG LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a
# Wed, 23 Aug 2023 23:57:39 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip
# Wed, 23 Aug 2023 23:57:39 GMT
ARG LIBERTY_BUILD_LABEL=cl230820230807-0401
# Wed, 23 Aug 2023 23:57:39 GMT
ARG OPENJ9_SCC=true
# Wed, 23 Aug 2023 23:57:39 GMT
ARG VERBOSE=false
# Wed, 23 Aug 2023 23:57:39 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl230820230807-0401 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=23.0.0.8
# Wed, 23 Aug 2023 23:57:39 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Wed, 23 Aug 2023 23:57:39 GMT
COPY dir:a51a46b81cfa5e03910d4f938a784aacd5cb102fab83ec37bb694f14e7486355 in /opt/ol/helpers 
# Wed, 23 Aug 2023 23:57:39 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Wed, 23 Aug 2023 23:57:40 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Wed, 23 Aug 2023 23:57:45 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Wed, 23 Aug 2023 23:57:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 23 Aug 2023 23:57:46 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Wed, 23 Aug 2023 23:57:47 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Wed, 23 Aug 2023 23:57:51 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Wed, 23 Aug 2023 23:57:52 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 23 Aug 2023 23:57:52 GMT
USER 1001
# Wed, 23 Aug 2023 23:57:52 GMT
EXPOSE 9080 9443
# Wed, 23 Aug 2023 23:57:52 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 23 Aug 2023 23:57:52 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:9ea365e1e52efb9567c56f02f2200f0e95ddffd579225cc5b20a6333119d2811`  
		Last Modified: Fri, 04 Aug 2023 13:35:19 GMT  
		Size: 28.4 MB (28391903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac60ed8a72576022d43698a13e953c7c74dac694b1a5a12ed5cebf1ae17c140`  
		Last Modified: Wed, 16 Aug 2023 14:38:10 GMT  
		Size: 12.1 MB (12113460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b8c95bd4e5f9c2e661db775f74897c811ea8fa99d505c1390021a99768db34`  
		Last Modified: Wed, 23 Aug 2023 20:20:51 GMT  
		Size: 46.8 MB (46789012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a2885a7c3a6b918d51ddbe4ccfc6d076748a4377916cca03b7266de225f359a`  
		Last Modified: Wed, 23 Aug 2023 20:20:46 GMT  
		Size: 4.6 MB (4613464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9337da7212f9156ad54f4ac948a142b33a4c1cf3a9910de710f13c5caa813e9d`  
		Last Modified: Thu, 24 Aug 2023 00:02:16 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e72f5fcb3f3477dc9af9966d118dc27e0fa595a71cc7c10190ac3185c78e490`  
		Last Modified: Thu, 24 Aug 2023 00:02:16 GMT  
		Size: 8.9 KB (8936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ac69f41355fe0744519a463a60a5d7a3cf198512acba19e42bc493ce0c3e66`  
		Last Modified: Thu, 24 Aug 2023 00:02:16 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6cf4cba8d78069e67ac7fdcc4739e9e77c2367f51c2a826d8ce8b184a958ae`  
		Last Modified: Thu, 24 Aug 2023 00:02:14 GMT  
		Size: 42.3 KB (42322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9986043d054b3579c9c7bef37fd03e231f19664c807ff695d2306fce9278a807`  
		Last Modified: Thu, 24 Aug 2023 00:02:16 GMT  
		Size: 14.2 MB (14219321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0da4a7a9f3314d20ca9c12f8297bc59d1571ff22959e1b96fc245338b09502a`  
		Last Modified: Thu, 24 Aug 2023 00:02:14 GMT  
		Size: 863.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83461187e2f926c77e7f5c10fb6ff7957a7cdf50619c310bdcc06b4f58522d`  
		Last Modified: Thu, 24 Aug 2023 00:02:14 GMT  
		Size: 10.0 KB (10030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe55146b1d7ea9ee82eb9ca1edc4989b04244a8c18beb76a952ccf022494d60`  
		Last Modified: Thu, 24 Aug 2023 00:02:15 GMT  
		Size: 2.6 MB (2588249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:kernel-slim-java17-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:561487614c15610bd8095a49698e5a43ed1507feecbdac0455ec06b86f0b00ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118929242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b44546ff5d1094e6775fd8621e89dbe01c80a38cd8b7c8140540b7ab575664f`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 04 Aug 2023 04:56:16 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:56:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:56:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:56:17 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:56:20 GMT
ADD file:0e9b840e6824ee009acbddc2d337fd5083ebe606393cf7532cdca4f108813ca3 in / 
# Fri, 04 Aug 2023 04:56:20 GMT
CMD ["/bin/bash"]
# Thu, 17 Aug 2023 07:53:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Aug 2023 07:53:44 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 23 Aug 2023 20:30:39 GMT
ENV JAVA_VERSION=jdk-17.0.8+7_openj9-0.40.0
# Wed, 23 Aug 2023 20:34:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b8904df2fee0797e493e3482fddb873b25d1e05f27053a2d96a25310c2dce3d4';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.8%2B7_openj9-0.40.0/ibm-semeru-open-jre_aarch64_linux_17.0.8_7_openj9-0.40.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='0986b451944deac0832c2905f1497fddb3ab7c0f63cd9fad707072381c9948a1';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.8%2B7_openj9-0.40.0/ibm-semeru-open-jre_ppc64le_linux_17.0.8_7_openj9-0.40.0.tar.gz';          ;;        amd64|x86_64)          ESUM='461aab09409b3ac26ded0ca921171e141c6b1400a17d8026e924109518b365d4';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.8%2B7_openj9-0.40.0/ibm-semeru-open-jre_x64_linux_17.0.8_7_openj9-0.40.0.tar.gz';          ;;        s390x)          ESUM='c759ed79d237d2e308869b9c1db12f8af4210d2ba08d293ad5d0f90b5eb1ead1';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.8%2B7_openj9-0.40.0/ibm-semeru-open-jre_s390x_linux_17.0.8_7_openj9-0.40.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 23 Aug 2023 20:34:37 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Aug 2023 20:34:37 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 23 Aug 2023 20:35:15 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 23 Aug 2023 21:16:43 GMT
USER root
# Wed, 23 Aug 2023 23:47:40 GMT
ARG LIBERTY_VERSION=23.0.0.8
# Wed, 23 Aug 2023 23:47:41 GMT
ARG LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a
# Wed, 23 Aug 2023 23:47:41 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip
# Wed, 23 Aug 2023 23:47:42 GMT
ARG LIBERTY_BUILD_LABEL=cl230820230807-0401
# Wed, 23 Aug 2023 23:47:42 GMT
ARG OPENJ9_SCC=true
# Wed, 23 Aug 2023 23:47:43 GMT
ARG VERBOSE=false
# Wed, 23 Aug 2023 23:47:43 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl230820230807-0401 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=23.0.0.8
# Wed, 23 Aug 2023 23:47:44 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Wed, 23 Aug 2023 23:47:44 GMT
COPY dir:a51a46b81cfa5e03910d4f938a784aacd5cb102fab83ec37bb694f14e7486355 in /opt/ol/helpers 
# Wed, 23 Aug 2023 23:47:44 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Wed, 23 Aug 2023 23:47:47 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Wed, 23 Aug 2023 23:48:02 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Wed, 23 Aug 2023 23:48:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 23 Aug 2023 23:48:05 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Wed, 23 Aug 2023 23:48:16 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Wed, 23 Aug 2023 23:48:33 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Wed, 23 Aug 2023 23:48:34 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 23 Aug 2023 23:48:35 GMT
USER 1001
# Wed, 23 Aug 2023 23:48:35 GMT
EXPOSE 9080 9443
# Wed, 23 Aug 2023 23:48:35 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 23 Aug 2023 23:48:36 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:09f4821f68917c7929419fff8bc583c406640180ea7d58eea03a95e463b8fb21`  
		Last Modified: Wed, 16 Aug 2023 02:15:01 GMT  
		Size: 35.7 MB (35712693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e0b5ceb7dfda582574a06a918e899d7d9019dd9005b084e06b6d57c5a53131`  
		Last Modified: Thu, 17 Aug 2023 08:04:07 GMT  
		Size: 12.9 MB (12895032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b9cedcc7b9c346d81c7420fa84d284478a65e6fd824a46a5d77f1dd293ef983`  
		Last Modified: Wed, 23 Aug 2023 20:52:05 GMT  
		Size: 49.7 MB (49730052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8165d874730d8c57ace83dea63b8d7a56e1d7c7eb1139d66a4d380d29e8e47e`  
		Last Modified: Wed, 23 Aug 2023 20:51:54 GMT  
		Size: 3.7 MB (3749585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764da712a675d1ea456c56e26928ba5e5af4809fbfbf23e17e072e982d6abe11`  
		Last Modified: Wed, 23 Aug 2023 23:57:52 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fb7e2cd2dc9a35c25a343a7c5ca131844c7d508dae799e4c753cb8cde195cf`  
		Last Modified: Wed, 23 Aug 2023 23:57:51 GMT  
		Size: 8.9 KB (8935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7533f774f363db338f37e5e0d6de07ca26e4f2fc2c3143a1f56894732904b68f`  
		Last Modified: Wed, 23 Aug 2023 23:57:51 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1828513493df76dbbc4924f96c06a950709c56f250804ed0c199e8f69c5fde98`  
		Last Modified: Wed, 23 Aug 2023 23:57:49 GMT  
		Size: 36.5 KB (36499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d956df83c8e9b276700b121ffa080761e773d1f83f6cfe3ee8121926685685d1`  
		Last Modified: Wed, 23 Aug 2023 23:57:50 GMT  
		Size: 14.2 MB (14218905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68422783488541fd0202652cfe5edad240ef669b1d89b644524c75eacb6cda48`  
		Last Modified: Wed, 23 Aug 2023 23:57:49 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0708963eec69f46f8e64c1a81833e586d21ffb5c15790719dd7f3f69fc2428`  
		Last Modified: Wed, 23 Aug 2023 23:57:49 GMT  
		Size: 10.1 KB (10050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896f49e24f85c4489ff642fa6c3ec23a04d1f1e658bb2431da39f1a70c217f7f`  
		Last Modified: Wed, 23 Aug 2023 23:57:50 GMT  
		Size: 2.6 MB (2565250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:kernel-slim-java17-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:555e45c848e87fb355050ba40f74e65e647992819e3c1788068969f7b81c4ae4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110330910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6c6e90bf84204356d63570aa6d5f2c936d64fbb36143c5d2d44b24e2b4b49e`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 04 Aug 2023 05:03:14 GMT
ARG RELEASE
# Fri, 04 Aug 2023 05:03:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 05:03:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 05:03:14 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 05:03:16 GMT
ADD file:d5b5687c046ca0689ccc4f42ddcc27543404ae2273aa12241e6636a2b3d675df in / 
# Fri, 04 Aug 2023 05:03:16 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 09:23:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 16 Aug 2023 09:23:39 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 23 Aug 2023 20:05:59 GMT
ENV JAVA_VERSION=jdk-17.0.8+7_openj9-0.40.0
# Wed, 23 Aug 2023 20:07:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b8904df2fee0797e493e3482fddb873b25d1e05f27053a2d96a25310c2dce3d4';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.8%2B7_openj9-0.40.0/ibm-semeru-open-jre_aarch64_linux_17.0.8_7_openj9-0.40.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='0986b451944deac0832c2905f1497fddb3ab7c0f63cd9fad707072381c9948a1';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.8%2B7_openj9-0.40.0/ibm-semeru-open-jre_ppc64le_linux_17.0.8_7_openj9-0.40.0.tar.gz';          ;;        amd64|x86_64)          ESUM='461aab09409b3ac26ded0ca921171e141c6b1400a17d8026e924109518b365d4';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.8%2B7_openj9-0.40.0/ibm-semeru-open-jre_x64_linux_17.0.8_7_openj9-0.40.0.tar.gz';          ;;        s390x)          ESUM='c759ed79d237d2e308869b9c1db12f8af4210d2ba08d293ad5d0f90b5eb1ead1';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.8%2B7_openj9-0.40.0/ibm-semeru-open-jre_s390x_linux_17.0.8_7_openj9-0.40.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 23 Aug 2023 20:07:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Aug 2023 20:07:53 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 23 Aug 2023 20:08:25 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 23 Aug 2023 20:34:13 GMT
USER root
# Wed, 23 Aug 2023 23:46:45 GMT
ARG LIBERTY_VERSION=23.0.0.8
# Wed, 23 Aug 2023 23:46:45 GMT
ARG LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a
# Wed, 23 Aug 2023 23:46:45 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip
# Wed, 23 Aug 2023 23:46:45 GMT
ARG LIBERTY_BUILD_LABEL=cl230820230807-0401
# Wed, 23 Aug 2023 23:46:46 GMT
ARG OPENJ9_SCC=true
# Wed, 23 Aug 2023 23:46:46 GMT
ARG VERBOSE=false
# Wed, 23 Aug 2023 23:46:46 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl230820230807-0401 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=23.0.0.8
# Wed, 23 Aug 2023 23:46:46 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Wed, 23 Aug 2023 23:46:46 GMT
COPY dir:a51a46b81cfa5e03910d4f938a784aacd5cb102fab83ec37bb694f14e7486355 in /opt/ol/helpers 
# Wed, 23 Aug 2023 23:46:46 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Wed, 23 Aug 2023 23:46:47 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Wed, 23 Aug 2023 23:46:53 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Wed, 23 Aug 2023 23:46:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 23 Aug 2023 23:46:55 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Wed, 23 Aug 2023 23:46:56 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Wed, 23 Aug 2023 23:47:00 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Wed, 23 Aug 2023 23:47:00 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 23 Aug 2023 23:47:01 GMT
USER 1001
# Wed, 23 Aug 2023 23:47:01 GMT
EXPOSE 9080 9443
# Wed, 23 Aug 2023 23:47:01 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 23 Aug 2023 23:47:01 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:de1d106061fc0332ca262e39ed7d2aa6384ae341a084b39449e21c742802df9c`  
		Last Modified: Wed, 16 Aug 2023 04:39:02 GMT  
		Size: 28.6 MB (28644373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33878ed31a5f2ae2ce7e393a139a1e3266bdd76a60af22203b6d4fcd73343dd7`  
		Last Modified: Wed, 16 Aug 2023 09:33:07 GMT  
		Size: 12.2 MB (12199840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb738a2c4c2f4745158f48114515596148b226153333764cff51c6d187b77db`  
		Last Modified: Wed, 23 Aug 2023 20:15:51 GMT  
		Size: 47.6 MB (47649252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f93f3477ccdf6744e48c7b446de1a296565d3ca70798ddf11c4779e3c88fb17`  
		Last Modified: Wed, 23 Aug 2023 20:15:45 GMT  
		Size: 4.9 MB (4908992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764afcb22393214523fa2a289b0750c5cf7f37f206e7dcdedda1f5531874dd7e`  
		Last Modified: Wed, 23 Aug 2023 23:53:41 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef0d1d7737295f252c73cf92ae1e4582f6c8caff9ffb5a28daa2c79e30c8a56`  
		Last Modified: Wed, 23 Aug 2023 23:53:41 GMT  
		Size: 8.9 KB (8933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9392044d283c54116dd292cb7c5e7d71ae34b178831c83bfb23b7ee863f0eb8d`  
		Last Modified: Wed, 23 Aug 2023 23:53:40 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e1c2b6dbaf185cce5623bd86e83c69bdec6a58c46f9f38ddb6477354a43f5a`  
		Last Modified: Wed, 23 Aug 2023 23:53:39 GMT  
		Size: 33.1 KB (33113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbd1f339f56f0f034b3c21340fc3db0b6c8a0066e130eba9ccd9023756c6ef2`  
		Last Modified: Wed, 23 Aug 2023 23:53:40 GMT  
		Size: 14.2 MB (14218557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b2804937d263abfc9ae598daa3e5a7acd02b0dd8881addcb09366a4aaf7e93`  
		Last Modified: Wed, 23 Aug 2023 23:53:40 GMT  
		Size: 863.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff280652ae7786a9c8b0b416953415d1112e910a3425db6719e0d3025e1635e`  
		Last Modified: Wed, 23 Aug 2023 23:53:39 GMT  
		Size: 10.0 KB (10023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061a6f60782428eff96ad219326eb89cd8ce072d2407b0a85a78059cf5864287`  
		Last Modified: Wed, 23 Aug 2023 23:53:40 GMT  
		Size: 2.7 MB (2655623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
