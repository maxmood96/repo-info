## `open-liberty:beta`

```console
$ docker pull open-liberty@sha256:76f39663f30771e15b91c1fee5d49aa8a7524f391c9855ee863ab21e233c039c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `open-liberty:beta` - linux; amd64

```console
$ docker pull open-liberty@sha256:3817cfa5f4b233b942f7dddfa20d348c3fa302d5ab4d5b8049ccf3cb04bf721b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.6 MB (445567158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ce8e6bc2056daded10ed49a3d7f7bbd52695e064530a7d6d02657af909099c`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 05:01:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 16 Apr 2024 05:01:39 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:01:39 GMT
ENV JAVA_VERSION=jdk8u402-b06_openj9-0.43.0
# Tue, 16 Apr 2024 05:03:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='4921671d26754483f096007cfb537922f1b190ca471aaebda6eccdefe91f7fb0';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u402-b06_openj9-0.43.0/ibm-semeru-open-jre_aarch64_linux_8u402b06_openj9-0.43.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d0efc1cee9a57bdb623e4f976aaa2ca96b7b724631521d9e387e543b2c57288b';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u402-b06_openj9-0.43.0/ibm-semeru-open-jre_ppc64le_linux_8u402b06_openj9-0.43.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6f2e0e977f833ad9b2d85e97e568aa57c658eea3f096a1544d72e70f94e55f73';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u402-b06_openj9-0.43.0/ibm-semeru-open-jre_x64_linux_8u402b06_openj9-0.43.0.tar.gz';          ;;        s390x)          ESUM='2c4cf63ea82f8d1fc84394b83c6c1e93fb30c6a83c8635ee648885f81b5d8d31';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u402-b06_openj9-0.43.0/ibm-semeru-open-jre_s390x_linux_8u402b06_openj9-0.43.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 16 Apr 2024 05:03:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 05:03:19 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 16 Apr 2024 05:03:51 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.85/bin/apache-tomcat-9.0.85.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Tue, 16 Apr 2024 12:40:28 GMT
USER root
# Fri, 24 May 2024 00:38:10 GMT
ARG LIBERTY_VERSION=24.0.0.6-beta
# Fri, 24 May 2024 00:38:11 GMT
ARG LIBERTY_SHA=e583894c9ce9cc1739e8593f3deb379520ed2ef2
# Fri, 24 May 2024 00:38:11 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.6-beta/openliberty-runtime-24.0.0.6-beta.zip
# Fri, 24 May 2024 00:38:11 GMT
ARG LIBERTY_BUILD_LABEL=cl240520240506-1951
# Fri, 24 May 2024 00:38:11 GMT
ARG OPENJ9_SCC=true
# Fri, 24 May 2024 00:38:11 GMT
ARG VERBOSE=false
# Fri, 24 May 2024 00:38:11 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240520240506-1951 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=24.0.0.6-beta
# Fri, 24 May 2024 00:38:11 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Fri, 24 May 2024 00:38:11 GMT
COPY dir:93a31d96afbc2ac47437e2c484fa07c529424a64c74e8646723e7655492506d3 in /opt/ol/helpers 
# Fri, 24 May 2024 00:38:11 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Fri, 24 May 2024 00:38:13 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.6-beta/openliberty-runtime-24.0.0.6-beta.zip LIBERTY_SHA=e583894c9ce9cc1739e8593f3deb379520ed2ef2 LIBERTY_VERSION=24.0.0.6-beta OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Fri, 24 May 2024 00:38:33 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.6-beta/openliberty-runtime-24.0.0.6-beta.zip LIBERTY_SHA=e583894c9ce9cc1739e8593f3deb379520ed2ef2 LIBERTY_VERSION=24.0.0.6-beta OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Fri, 24 May 2024 00:38:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 24 May 2024 00:38:35 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.6-beta/openliberty-runtime-24.0.0.6-beta.zip LIBERTY_SHA=e583894c9ce9cc1739e8593f3deb379520ed2ef2 LIBERTY_VERSION=24.0.0.6-beta VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Fri, 24 May 2024 00:38:36 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.6-beta/openliberty-runtime-24.0.0.6-beta.zip LIBERTY_SHA=e583894c9ce9cc1739e8593f3deb379520ed2ef2 LIBERTY_VERSION=24.0.0.6-beta VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Fri, 24 May 2024 00:39:08 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.6-beta/openliberty-runtime-24.0.0.6-beta.zip LIBERTY_SHA=e583894c9ce9cc1739e8593f3deb379520ed2ef2 LIBERTY_VERSION=24.0.0.6-beta VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Fri, 24 May 2024 00:39:08 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 24 May 2024 00:39:08 GMT
USER 1001
# Fri, 24 May 2024 00:39:08 GMT
EXPOSE 9080 9443
# Fri, 24 May 2024 00:39:08 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 24 May 2024 00:39:08 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7174e6ca1f346329bcdcb2b0c9e4a5deec1e5e895ae1fc065cef54ef5b38ef80`  
		Last Modified: Tue, 16 Apr 2024 05:14:19 GMT  
		Size: 12.2 MB (12156612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c980529a03382656b5ae771a61395edd700c08718ce66f993ec961548d718274`  
		Last Modified: Tue, 16 Apr 2024 05:14:57 GMT  
		Size: 50.4 MB (50386579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18928df37171ce65b39546cdbd83b583864059fe42bcb25b956edc9b1185662b`  
		Last Modified: Tue, 16 Apr 2024 05:14:52 GMT  
		Size: 4.2 MB (4165049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93712b1c0f33ef5936b51c44d7b6686a9104265fa3a91296ac57d5ab4eda53b1`  
		Last Modified: Fri, 24 May 2024 00:47:00 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57cdc7a7278666f8aacda507b705c4150cc5abbab890e92c0208e8c68a19814d`  
		Last Modified: Fri, 24 May 2024 00:46:59 GMT  
		Size: 10.0 KB (10016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b13d1ef5f52d556f36870d747d79f3a913db98401eff72ebe19fd7fcd77e8420`  
		Last Modified: Fri, 24 May 2024 00:46:59 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebdeb2c255a065c8510dd35e0bcc41a9c80a0688ff368b53f28017e1a445c2a0`  
		Last Modified: Fri, 24 May 2024 00:46:57 GMT  
		Size: 31.8 KB (31750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90455fd780d259e89b123ad743b2b33ee5c2916b7a190ccca00f445378bdbf1f`  
		Last Modified: Fri, 24 May 2024 00:47:12 GMT  
		Size: 334.9 MB (334934028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f03d7455702b68f378d3c7208330e763ea4a0d1b7cc93b7e831999f060ff7a`  
		Last Modified: Fri, 24 May 2024 00:46:57 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1f32877295db57e908403bbe46736a538b9db2b5385dc573b2de508df66dc1`  
		Last Modified: Fri, 24 May 2024 00:46:57 GMT  
		Size: 11.5 KB (11494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e489e5fe8286732e8055b5be1790b885d42fd7733bebbc57bd3d8a22d1ddf8b`  
		Last Modified: Fri, 24 May 2024 00:46:59 GMT  
		Size: 13.4 MB (13429328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:beta` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:05c0fb5a5156edb09b605875f90e9bcce1e3b9628e3db9a7805e8b7d44b5653e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.9 MB (441894653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ac5d45425fc0f0a4e9749d945752002eaf1f16a15162e1b31096fead8248e4`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:01:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 16 Apr 2024 03:02:11 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:02:11 GMT
ENV JAVA_VERSION=jdk8u402-b06_openj9-0.43.0
# Tue, 16 Apr 2024 03:03:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='4921671d26754483f096007cfb537922f1b190ca471aaebda6eccdefe91f7fb0';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u402-b06_openj9-0.43.0/ibm-semeru-open-jre_aarch64_linux_8u402b06_openj9-0.43.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d0efc1cee9a57bdb623e4f976aaa2ca96b7b724631521d9e387e543b2c57288b';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u402-b06_openj9-0.43.0/ibm-semeru-open-jre_ppc64le_linux_8u402b06_openj9-0.43.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6f2e0e977f833ad9b2d85e97e568aa57c658eea3f096a1544d72e70f94e55f73';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u402-b06_openj9-0.43.0/ibm-semeru-open-jre_x64_linux_8u402b06_openj9-0.43.0.tar.gz';          ;;        s390x)          ESUM='2c4cf63ea82f8d1fc84394b83c6c1e93fb30c6a83c8635ee648885f81b5d8d31';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u402-b06_openj9-0.43.0/ibm-semeru-open-jre_s390x_linux_8u402b06_openj9-0.43.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 16 Apr 2024 03:03:46 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 03:03:46 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 16 Apr 2024 03:04:18 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.85/bin/apache-tomcat-9.0.85.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Tue, 16 Apr 2024 08:49:01 GMT
USER root
# Fri, 24 May 2024 00:43:09 GMT
ARG LIBERTY_VERSION=24.0.0.6-beta
# Fri, 24 May 2024 00:43:09 GMT
ARG LIBERTY_SHA=e583894c9ce9cc1739e8593f3deb379520ed2ef2
# Fri, 24 May 2024 00:43:09 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.6-beta/openliberty-runtime-24.0.0.6-beta.zip
# Fri, 24 May 2024 00:43:09 GMT
ARG LIBERTY_BUILD_LABEL=cl240520240506-1951
# Fri, 24 May 2024 00:43:09 GMT
ARG OPENJ9_SCC=true
# Fri, 24 May 2024 00:43:09 GMT
ARG VERBOSE=false
# Fri, 24 May 2024 00:43:09 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240520240506-1951 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=24.0.0.6-beta
# Fri, 24 May 2024 00:43:09 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Fri, 24 May 2024 00:43:09 GMT
COPY dir:93a31d96afbc2ac47437e2c484fa07c529424a64c74e8646723e7655492506d3 in /opt/ol/helpers 
# Fri, 24 May 2024 00:43:09 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Fri, 24 May 2024 00:43:10 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.6-beta/openliberty-runtime-24.0.0.6-beta.zip LIBERTY_SHA=e583894c9ce9cc1739e8593f3deb379520ed2ef2 LIBERTY_VERSION=24.0.0.6-beta OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Fri, 24 May 2024 00:43:27 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.6-beta/openliberty-runtime-24.0.0.6-beta.zip LIBERTY_SHA=e583894c9ce9cc1739e8593f3deb379520ed2ef2 LIBERTY_VERSION=24.0.0.6-beta OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Fri, 24 May 2024 00:43:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 24 May 2024 00:43:30 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.6-beta/openliberty-runtime-24.0.0.6-beta.zip LIBERTY_SHA=e583894c9ce9cc1739e8593f3deb379520ed2ef2 LIBERTY_VERSION=24.0.0.6-beta VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Fri, 24 May 2024 00:43:31 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.6-beta/openliberty-runtime-24.0.0.6-beta.zip LIBERTY_SHA=e583894c9ce9cc1739e8593f3deb379520ed2ef2 LIBERTY_VERSION=24.0.0.6-beta VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Fri, 24 May 2024 00:43:58 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.6-beta/openliberty-runtime-24.0.0.6-beta.zip LIBERTY_SHA=e583894c9ce9cc1739e8593f3deb379520ed2ef2 LIBERTY_VERSION=24.0.0.6-beta VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Fri, 24 May 2024 00:43:58 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 24 May 2024 00:43:58 GMT
USER 1001
# Fri, 24 May 2024 00:43:59 GMT
EXPOSE 9080 9443
# Fri, 24 May 2024 00:43:59 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 24 May 2024 00:43:59 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf623939c01b82bafd9b4d9e769ce2119ef976cbd0968b69dfb1bd1590dbe55`  
		Last Modified: Tue, 16 Apr 2024 03:14:17 GMT  
		Size: 12.1 MB (12115565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864a62dd1e5ec4307f19a25e137252f514a1ed39eeef85ac88e2503c79610156`  
		Last Modified: Tue, 16 Apr 2024 03:14:50 GMT  
		Size: 49.7 MB (49661877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae723ff6ca639254e6ad8b93b2104e1b47e67a22438511c49eaf8f9df1bd0e80`  
		Last Modified: Tue, 16 Apr 2024 03:14:46 GMT  
		Size: 4.0 MB (4020203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0ae62d09f7e822c57658e4f110486170ab4d9fbf3c1131b21bba5dc403b53c`  
		Last Modified: Fri, 24 May 2024 00:50:49 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bf76bd762413e72371dd6925d804a5eacbf00ea8c76ba76164a2842ad204b9`  
		Last Modified: Fri, 24 May 2024 00:50:49 GMT  
		Size: 10.0 KB (10016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aded51c6035def1148865ea9fd3e519372902ec90dcf893c13239fc2e9fe7e81`  
		Last Modified: Fri, 24 May 2024 00:50:49 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe05362df6d9d8ec1e51f4a213a8853d04f5d01b09f9d6410f61ed46e4cd73ca`  
		Last Modified: Fri, 24 May 2024 00:50:48 GMT  
		Size: 42.3 KB (42325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54914b2fc1825a870c9ce572c6b96610c76642ab8fef2308a2850592061f38be`  
		Last Modified: Fri, 24 May 2024 00:51:00 GMT  
		Size: 334.9 MB (334934709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72da34f109509312ee643e83c07f88cceb9ea8505111558671a1d7bb46c50aaf`  
		Last Modified: Fri, 24 May 2024 00:50:47 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b743e65f0f68a1922c72a2056a708dba0eb822f4353f88f62b78275d552e107e`  
		Last Modified: Fri, 24 May 2024 00:50:48 GMT  
		Size: 11.5 KB (11497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd6e0c8d1ab528724560b2a362c07daaeb2c282054af2555e98687b9c95e20d`  
		Last Modified: Fri, 24 May 2024 00:50:49 GMT  
		Size: 12.7 MB (12695632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:beta` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:6710c2bff3602c723d3943adf3759203703e60429f9d9f04e8fa730dc0843519
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.3 MB (450250449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51598189a5422dda64570a813c831ca4ff5d5f2e20aa721cbc3a9f29c2cc7d69`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 10 Apr 2024 18:53:14 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:53:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:53:18 GMT
ADD file:417bf7a0c7958ce23aaf2e92c63328e2bc36835d1c9b8c8302702ba8bdf3cc7b in / 
# Wed, 10 Apr 2024 18:53:18 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:45:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 16 Apr 2024 03:46:30 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:46:34 GMT
ENV JAVA_VERSION=jdk8u402-b06_openj9-0.43.0
# Tue, 16 Apr 2024 03:49:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='4921671d26754483f096007cfb537922f1b190ca471aaebda6eccdefe91f7fb0';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u402-b06_openj9-0.43.0/ibm-semeru-open-jre_aarch64_linux_8u402b06_openj9-0.43.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d0efc1cee9a57bdb623e4f976aaa2ca96b7b724631521d9e387e543b2c57288b';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u402-b06_openj9-0.43.0/ibm-semeru-open-jre_ppc64le_linux_8u402b06_openj9-0.43.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6f2e0e977f833ad9b2d85e97e568aa57c658eea3f096a1544d72e70f94e55f73';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u402-b06_openj9-0.43.0/ibm-semeru-open-jre_x64_linux_8u402b06_openj9-0.43.0.tar.gz';          ;;        s390x)          ESUM='2c4cf63ea82f8d1fc84394b83c6c1e93fb30c6a83c8635ee648885f81b5d8d31';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u402-b06_openj9-0.43.0/ibm-semeru-open-jre_s390x_linux_8u402b06_openj9-0.43.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 16 Apr 2024 03:49:08 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 03:49:09 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 16 Apr 2024 03:49:42 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.85/bin/apache-tomcat-9.0.85.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Tue, 16 Apr 2024 08:25:01 GMT
USER root
# Fri, 24 May 2024 00:24:45 GMT
ARG LIBERTY_VERSION=24.0.0.6-beta
# Fri, 24 May 2024 00:24:45 GMT
ARG LIBERTY_SHA=e583894c9ce9cc1739e8593f3deb379520ed2ef2
# Fri, 24 May 2024 00:24:46 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.6-beta/openliberty-runtime-24.0.0.6-beta.zip
# Fri, 24 May 2024 00:24:46 GMT
ARG LIBERTY_BUILD_LABEL=cl240520240506-1951
# Fri, 24 May 2024 00:24:46 GMT
ARG OPENJ9_SCC=true
# Fri, 24 May 2024 00:24:46 GMT
ARG VERBOSE=false
# Fri, 24 May 2024 00:24:47 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240520240506-1951 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=24.0.0.6-beta
# Fri, 24 May 2024 00:24:47 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Fri, 24 May 2024 00:24:47 GMT
COPY dir:93a31d96afbc2ac47437e2c484fa07c529424a64c74e8646723e7655492506d3 in /opt/ol/helpers 
# Fri, 24 May 2024 00:24:47 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Fri, 24 May 2024 00:24:50 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.6-beta/openliberty-runtime-24.0.0.6-beta.zip LIBERTY_SHA=e583894c9ce9cc1739e8593f3deb379520ed2ef2 LIBERTY_VERSION=24.0.0.6-beta OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Fri, 24 May 2024 00:25:57 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.6-beta/openliberty-runtime-24.0.0.6-beta.zip LIBERTY_SHA=e583894c9ce9cc1739e8593f3deb379520ed2ef2 LIBERTY_VERSION=24.0.0.6-beta OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Fri, 24 May 2024 00:26:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 24 May 2024 00:26:04 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.6-beta/openliberty-runtime-24.0.0.6-beta.zip LIBERTY_SHA=e583894c9ce9cc1739e8593f3deb379520ed2ef2 LIBERTY_VERSION=24.0.0.6-beta VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Fri, 24 May 2024 00:26:05 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.6-beta/openliberty-runtime-24.0.0.6-beta.zip LIBERTY_SHA=e583894c9ce9cc1739e8593f3deb379520ed2ef2 LIBERTY_VERSION=24.0.0.6-beta VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Fri, 24 May 2024 00:26:42 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.6-beta/openliberty-runtime-24.0.0.6-beta.zip LIBERTY_SHA=e583894c9ce9cc1739e8593f3deb379520ed2ef2 LIBERTY_VERSION=24.0.0.6-beta VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Fri, 24 May 2024 00:26:43 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 24 May 2024 00:26:43 GMT
USER 1001
# Fri, 24 May 2024 00:26:43 GMT
EXPOSE 9080 9443
# Fri, 24 May 2024 00:26:44 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 24 May 2024 00:26:44 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:fdd7d0bd8ffc52196a33ea69f83c6ade1ff36b223484bae6626aa6f7db714a40`  
		Last Modified: Tue, 16 Apr 2024 02:34:05 GMT  
		Size: 35.6 MB (35587250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8539c6f8a1607ac59b46c0a3f097a0d7a8e240093007cf5df2caee4abe59a476`  
		Last Modified: Tue, 16 Apr 2024 04:02:51 GMT  
		Size: 12.9 MB (12890585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c48507a7063949052739e42d72a901ad131f6c4ab28d8b8fd438a2581cb902`  
		Last Modified: Tue, 16 Apr 2024 04:03:33 GMT  
		Size: 51.6 MB (51641956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695987e47ca9b908020b9c0ba039eadacb7b30a0b922b0380f64683d8eb82c41`  
		Last Modified: Tue, 16 Apr 2024 04:03:27 GMT  
		Size: 3.5 MB (3500391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd438940b93065449269c1129bea8fa4ba58f5dc371787c613f741b6cfbf25b`  
		Last Modified: Fri, 24 May 2024 00:37:41 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ef781b11d60634eef44383941462dbe55eaddc8a2a59a0ae4ea22c20341db3`  
		Last Modified: Fri, 24 May 2024 00:37:40 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab31786c8ce31af2005520fda271ed1e61af6da4b430559ea8814962a7f2767`  
		Last Modified: Fri, 24 May 2024 00:37:40 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec926605011e8643901812312f612b67d885242c7aded92fa6499854d0682e63`  
		Last Modified: Fri, 24 May 2024 00:37:38 GMT  
		Size: 36.5 KB (36499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b4ecb09a2209384eeba88398ef161841213521feb3b8ad7092f3faa01eeb3b`  
		Last Modified: Fri, 24 May 2024 00:37:56 GMT  
		Size: 334.9 MB (334934808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c169267d3b87cf479a923dd05401565584dbf49eefb49abd267344fe2eef7f03`  
		Last Modified: Fri, 24 May 2024 00:37:38 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c8322c271f758e54727904d56b15d1771e5bad42459bd8578e67f541b1ee768`  
		Last Modified: Fri, 24 May 2024 00:37:38 GMT  
		Size: 11.5 KB (11494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0a0cf0c47240b3b80ac776146e5bf907c929198b9e734433ad9796309399f9`  
		Last Modified: Fri, 24 May 2024 00:37:40 GMT  
		Size: 11.6 MB (11634913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:beta` - linux; s390x

```console
$ docker pull open-liberty@sha256:92ed3a0086651df6ddc53cd50763ce1239915dca81292c9c786b52b52237aff4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **443.7 MB (443660756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c3fe380a3ed36d910866cc94cb68b7280d5d9d51939d43ceb72dba3c01baec`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 10 Apr 2024 19:09:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:09:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:09:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:09:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 19:09:05 GMT
ADD file:7691b95908cace61ceeec91c44a1a37e7dc2fc3ab5a5fd89f493cefdff9e840e in / 
# Wed, 10 Apr 2024 19:09:05 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 01:55:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 16 Apr 2024 01:55:46 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 01:55:47 GMT
ENV JAVA_VERSION=jdk8u402-b06_openj9-0.43.0
# Tue, 16 Apr 2024 01:59:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='4921671d26754483f096007cfb537922f1b190ca471aaebda6eccdefe91f7fb0';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u402-b06_openj9-0.43.0/ibm-semeru-open-jre_aarch64_linux_8u402b06_openj9-0.43.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d0efc1cee9a57bdb623e4f976aaa2ca96b7b724631521d9e387e543b2c57288b';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u402-b06_openj9-0.43.0/ibm-semeru-open-jre_ppc64le_linux_8u402b06_openj9-0.43.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6f2e0e977f833ad9b2d85e97e568aa57c658eea3f096a1544d72e70f94e55f73';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u402-b06_openj9-0.43.0/ibm-semeru-open-jre_x64_linux_8u402b06_openj9-0.43.0.tar.gz';          ;;        s390x)          ESUM='2c4cf63ea82f8d1fc84394b83c6c1e93fb30c6a83c8635ee648885f81b5d8d31';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u402-b06_openj9-0.43.0/ibm-semeru-open-jre_s390x_linux_8u402b06_openj9-0.43.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 16 Apr 2024 01:59:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 01:59:31 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 16 Apr 2024 02:00:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.85/bin/apache-tomcat-9.0.85.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Tue, 16 Apr 2024 05:33:08 GMT
USER root
# Fri, 24 May 2024 00:44:22 GMT
ARG LIBERTY_VERSION=24.0.0.6-beta
# Fri, 24 May 2024 00:44:22 GMT
ARG LIBERTY_SHA=e583894c9ce9cc1739e8593f3deb379520ed2ef2
# Fri, 24 May 2024 00:44:22 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.6-beta/openliberty-runtime-24.0.0.6-beta.zip
# Fri, 24 May 2024 00:44:23 GMT
ARG LIBERTY_BUILD_LABEL=cl240520240506-1951
# Fri, 24 May 2024 00:44:23 GMT
ARG OPENJ9_SCC=true
# Fri, 24 May 2024 00:44:23 GMT
ARG VERBOSE=false
# Fri, 24 May 2024 00:44:23 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240520240506-1951 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=24.0.0.6-beta
# Fri, 24 May 2024 00:44:23 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Fri, 24 May 2024 00:44:23 GMT
COPY dir:93a31d96afbc2ac47437e2c484fa07c529424a64c74e8646723e7655492506d3 in /opt/ol/helpers 
# Fri, 24 May 2024 00:44:23 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Fri, 24 May 2024 00:44:24 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.6-beta/openliberty-runtime-24.0.0.6-beta.zip LIBERTY_SHA=e583894c9ce9cc1739e8593f3deb379520ed2ef2 LIBERTY_VERSION=24.0.0.6-beta OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Fri, 24 May 2024 00:44:52 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.6-beta/openliberty-runtime-24.0.0.6-beta.zip LIBERTY_SHA=e583894c9ce9cc1739e8593f3deb379520ed2ef2 LIBERTY_VERSION=24.0.0.6-beta OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Fri, 24 May 2024 00:44:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 24 May 2024 00:44:57 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.6-beta/openliberty-runtime-24.0.0.6-beta.zip LIBERTY_SHA=e583894c9ce9cc1739e8593f3deb379520ed2ef2 LIBERTY_VERSION=24.0.0.6-beta VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Fri, 24 May 2024 00:44:58 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.6-beta/openliberty-runtime-24.0.0.6-beta.zip LIBERTY_SHA=e583894c9ce9cc1739e8593f3deb379520ed2ef2 LIBERTY_VERSION=24.0.0.6-beta VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Fri, 24 May 2024 00:45:23 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240520240506-1951 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.6-beta/openliberty-runtime-24.0.0.6-beta.zip LIBERTY_SHA=e583894c9ce9cc1739e8593f3deb379520ed2ef2 LIBERTY_VERSION=24.0.0.6-beta VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Fri, 24 May 2024 00:45:24 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 24 May 2024 00:45:24 GMT
USER 1001
# Fri, 24 May 2024 00:45:24 GMT
EXPOSE 9080 9443
# Fri, 24 May 2024 00:45:24 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 24 May 2024 00:45:24 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:800aa7ed945a05dec0024b71aaef6a3ed35eb8fc8eef0982ff134513d2295713`  
		Last Modified: Tue, 16 Apr 2024 01:37:03 GMT  
		Size: 28.6 MB (28637157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c848c934aa4ef4451fd4c7c2a114e25882400ab8f06c52583083702c9b804a`  
		Last Modified: Tue, 16 Apr 2024 02:14:32 GMT  
		Size: 12.2 MB (12204328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76930e84b9a3a09b1c45ca2ff9e77898536d78333c8c0a918471010ff0ec6b7e`  
		Last Modified: Tue, 16 Apr 2024 02:15:04 GMT  
		Size: 50.2 MB (50163394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f46ac186418dfc09c08c95cb20698cd7f1825bb7c9532b3cfc37312acdc269`  
		Last Modified: Tue, 16 Apr 2024 02:14:59 GMT  
		Size: 4.4 MB (4373344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4a339ef8049d200852daeaaef85d444a2ccb596a637e9a1ae57fd56428e09c`  
		Last Modified: Fri, 24 May 2024 00:54:53 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792e2b778522b6cc2a5232d132389062651629f319dd4f453e81e5e95862785c`  
		Last Modified: Fri, 24 May 2024 00:54:53 GMT  
		Size: 10.0 KB (10019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f421eda848e13bf6f40c1a9eea1438145840e0c989d146f787c453a32b7d0ab6`  
		Last Modified: Fri, 24 May 2024 00:54:52 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d724108d073e98bc47b8c93ed58f02863ffa08d3e9f5a24a871fc28ef0ef7b4d`  
		Last Modified: Fri, 24 May 2024 00:54:51 GMT  
		Size: 33.1 KB (33114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d588354ac78f199cd8765c75336d364a19bd0ae714abe6dda44d2c79082a4614`  
		Last Modified: Fri, 24 May 2024 00:55:05 GMT  
		Size: 334.9 MB (334934305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d99937fa9edf35de218145831dd82851d20b77e870ceef718cd9a4649abafd8`  
		Last Modified: Fri, 24 May 2024 00:54:51 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90572fdd125f6bbe6d1c49c432d67f140d76862d4cd2bc187565f5fe18d67a6`  
		Last Modified: Fri, 24 May 2024 00:54:51 GMT  
		Size: 11.5 KB (11500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc5808b82a3bad6a4f6ccb98ae54bb96a90c797259ddc2aa22cb0a7de01c673`  
		Last Modified: Fri, 24 May 2024 00:54:52 GMT  
		Size: 13.3 MB (13291064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
