## `websphere-liberty:kernel-java17-openj9`

```console
$ docker pull websphere-liberty@sha256:0fba0e6e3e8f741fc27d155c34fbdf98706fe62b1cc8ae17463aef90a8973cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:kernel-java17-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:b4f286c137304565036360dbf3231f4b45f76b6997346ddc639b94acb7b9918e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116189974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb95b795feb790641f26ae91face4cce3648bd4ce6d8684684b98cf6b6e3f885`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 02:23:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 02 Dec 2023 02:24:18 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 02:30:59 GMT
ENV JAVA_VERSION=jdk-17.0.9+9_openj9-0.41.0
# Sat, 02 Dec 2023 02:32:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9760aa27a5790a8c20a702ff5f036535f3df51d3fb291bb5254b5ae76e096bad';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.9%2B9_openj9-0.41.0/ibm-semeru-open-jre_aarch64_linux_17.0.9_9_openj9-0.41.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='73b9baab2766191de5da00498f2dcfe9de90fff6c4c457bea4944f103c6dde6e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.9%2B9_openj9-0.41.0/ibm-semeru-open-jre_ppc64le_linux_17.0.9_9_openj9-0.41.0.tar.gz';          ;;        amd64|x86_64)          ESUM='1caf409f33f7738efe37742197525b5ae6244d6383b2017e7b8e925dc0b6a329';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.9%2B9_openj9-0.41.0/ibm-semeru-open-jre_x64_linux_17.0.9_9_openj9-0.41.0.tar.gz';          ;;        s390x)          ESUM='53e813367f3462e9dd66f8d4d3063c96bfd0cfc462b568187f62a5847ae01ad1';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.9%2B9_openj9-0.41.0/ibm-semeru-open-jre_s390x_linux_17.0.9_9_openj9-0.41.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 02 Dec 2023 02:32:43 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 02:32:43 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Sat, 02 Dec 2023 02:33:19 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Sat, 02 Dec 2023 11:29:33 GMT
USER root
# Sat, 02 Dec 2023 11:49:11 GMT
ARG VERBOSE=false
# Sat, 02 Dec 2023 11:49:11 GMT
ARG OPENJ9_SCC=true
# Wed, 13 Dec 2023 18:35:05 GMT
ARG LIBERTY_VERSION=23.0.0.12
# Wed, 13 Dec 2023 18:35:05 GMT
ARG LIBERTY_BUILD_LABEL=cl231220231127-1901
# Wed, 13 Dec 2023 18:35:05 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=23.0.0.12 org.opencontainers.image.revision=cl231220231127-1901 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 13 Dec 2023 18:35:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 13 Dec 2023 18:35:05 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=23.0.0.12 BuildLabel=cl231220231127-1901
# Wed, 13 Dec 2023 18:35:06 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_VERSION=23.0.0.12 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Wed, 13 Dec 2023 18:35:06 GMT
ARG LIBERTY_URL
# Wed, 13 Dec 2023 18:35:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 13 Dec 2023 18:35:17 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_VERSION=23.0.0.12 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2023 18:35:17 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 13 Dec 2023 18:35:18 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_VERSION=23.0.0.12 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env
# Wed, 13 Dec 2023 18:35:18 GMT
COPY file:7278f8f20139aab77b5c9fa76ad85e8a92836053c3ecfb9f5925f1a19788ef47 in /opt/ibm/NOTICES 
# Wed, 13 Dec 2023 18:35:18 GMT
COPY dir:254af54889f4a4b4a77147fe142eaaed75a79fca1e096326071edb660b9fa8b2 in /opt/ibm/helpers/ 
# Wed, 13 Dec 2023 18:35:19 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 13 Dec 2023 18:35:19 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_VERSION=23.0.0.12 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 13 Dec 2023 18:35:25 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_VERSION=23.0.0.12 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 13 Dec 2023 18:35:25 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 13 Dec 2023 18:35:25 GMT
USER 1001
# Wed, 13 Dec 2023 18:35:25 GMT
EXPOSE 9080 9443
# Wed, 13 Dec 2023 18:35:25 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 13 Dec 2023 18:35:25 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a261eab81e521775977f42fd67a3196085829d7723b5ca804ff8e0e504f9526`  
		Last Modified: Sat, 02 Dec 2023 02:37:49 GMT  
		Size: 12.2 MB (12155087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e066abe1e5fa280138eb238ddcaee5d9c8e50d2f615720315e992785beeec45`  
		Last Modified: Sat, 02 Dec 2023 02:40:58 GMT  
		Size: 48.9 MB (48862564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf143e36c72cb4a6c2e20b5d357030d194bcb1b19c3c9ebccb61d01086a5a07`  
		Last Modified: Sat, 02 Dec 2023 02:40:52 GMT  
		Size: 4.8 MB (4811721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e13d27048f00bafb9b65fe3103477da23d2a0adf98977f5899f2b84f2285ae`  
		Last Modified: Wed, 13 Dec 2023 19:06:41 GMT  
		Size: 31.7 KB (31747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c74fb32eb937ad4761661997b323dfd49831bc3c3c0b0942560bf9cc3c3d9b`  
		Last Modified: Wed, 13 Dec 2023 19:06:51 GMT  
		Size: 17.1 MB (17142858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1dd2cda85abcb795e26fde103db3543d49e3e8f0a9583ed317af8347aca7574`  
		Last Modified: Wed, 13 Dec 2023 19:06:40 GMT  
		Size: 611.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2e3fcf93cc523c50fb196b89b05ee4f79ca38a6520d5fc6394f7ec793bef39`  
		Last Modified: Wed, 13 Dec 2023 19:06:39 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ddf51786831ebbf9dc2f843076b3bcbfa0772af314908dc94ff6a728aa65857`  
		Last Modified: Wed, 13 Dec 2023 19:06:38 GMT  
		Size: 11.4 KB (11439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dbaf7ffb3605834c8d48f0b24df910f5e6d8067bac8d9140481d10c11618845`  
		Last Modified: Wed, 13 Dec 2023 19:06:38 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db0f959f1c9652b2013efdc9a8ac4529a2d8ee8c8c1c2fe27b08c6dbcef681d`  
		Last Modified: Wed, 13 Dec 2023 19:06:38 GMT  
		Size: 12.4 KB (12365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d171ac2aca398dad379216fefbf90d0e255ba45848175598c17cce2dc794c5`  
		Last Modified: Wed, 13 Dec 2023 19:06:39 GMT  
		Size: 2.7 MB (2713472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel-java17-openj9` - linux; arm64 variant v8

```console
$ docker pull websphere-liberty@sha256:e06053b670c8cc9ad322e8e0b3847d4d721aaf567edfcd98cb80897e698aa80d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112570617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5edab02ebfcd23a585172ccbc69abe905c3ff289791f7dff2a090fd40c7ab3ba`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 01 Dec 2023 07:43:19 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:43:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:43:21 GMT
ADD file:891dcab0c4ce2880c4dca013d326a3efd7601003b6f5076938d678101e301b79 in / 
# Fri, 01 Dec 2023 07:43:22 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 07:20:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 02 Dec 2023 07:21:21 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 07:27:36 GMT
ENV JAVA_VERSION=jdk-17.0.9+9_openj9-0.41.0
# Sat, 02 Dec 2023 07:29:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9760aa27a5790a8c20a702ff5f036535f3df51d3fb291bb5254b5ae76e096bad';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.9%2B9_openj9-0.41.0/ibm-semeru-open-jre_aarch64_linux_17.0.9_9_openj9-0.41.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='73b9baab2766191de5da00498f2dcfe9de90fff6c4c457bea4944f103c6dde6e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.9%2B9_openj9-0.41.0/ibm-semeru-open-jre_ppc64le_linux_17.0.9_9_openj9-0.41.0.tar.gz';          ;;        amd64|x86_64)          ESUM='1caf409f33f7738efe37742197525b5ae6244d6383b2017e7b8e925dc0b6a329';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.9%2B9_openj9-0.41.0/ibm-semeru-open-jre_x64_linux_17.0.9_9_openj9-0.41.0.tar.gz';          ;;        s390x)          ESUM='53e813367f3462e9dd66f8d4d3063c96bfd0cfc462b568187f62a5847ae01ad1';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.9%2B9_openj9-0.41.0/ibm-semeru-open-jre_s390x_linux_17.0.9_9_openj9-0.41.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 02 Dec 2023 07:29:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 07:29:10 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Sat, 02 Dec 2023 07:29:44 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Sat, 02 Dec 2023 12:22:57 GMT
USER root
# Sat, 02 Dec 2023 12:22:57 GMT
ARG VERBOSE=false
# Sat, 02 Dec 2023 12:22:57 GMT
ARG OPENJ9_SCC=true
# Wed, 13 Dec 2023 19:04:31 GMT
ARG LIBERTY_VERSION=23.0.0.12
# Wed, 13 Dec 2023 19:04:31 GMT
ARG LIBERTY_BUILD_LABEL=cl231220231127-1901
# Wed, 13 Dec 2023 19:04:32 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=23.0.0.12 org.opencontainers.image.revision=cl231220231127-1901 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 13 Dec 2023 19:04:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 13 Dec 2023 19:04:32 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=23.0.0.12 BuildLabel=cl231220231127-1901
# Wed, 13 Dec 2023 19:04:32 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_VERSION=23.0.0.12 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Wed, 13 Dec 2023 19:04:33 GMT
ARG LIBERTY_URL
# Wed, 13 Dec 2023 19:04:33 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 13 Dec 2023 19:04:43 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_VERSION=23.0.0.12 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2023 19:04:43 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 13 Dec 2023 19:04:44 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_VERSION=23.0.0.12 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env
# Wed, 13 Dec 2023 19:04:44 GMT
COPY file:7278f8f20139aab77b5c9fa76ad85e8a92836053c3ecfb9f5925f1a19788ef47 in /opt/ibm/NOTICES 
# Wed, 13 Dec 2023 19:04:44 GMT
COPY dir:254af54889f4a4b4a77147fe142eaaed75a79fca1e096326071edb660b9fa8b2 in /opt/ibm/helpers/ 
# Wed, 13 Dec 2023 19:04:44 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 13 Dec 2023 19:04:45 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_VERSION=23.0.0.12 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 13 Dec 2023 19:04:49 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_VERSION=23.0.0.12 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 13 Dec 2023 19:04:49 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 13 Dec 2023 19:04:49 GMT
USER 1001
# Wed, 13 Dec 2023 19:04:49 GMT
EXPOSE 9080 9443
# Wed, 13 Dec 2023 19:04:49 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 13 Dec 2023 19:04:50 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:aeb9f260d781cd1e09daf0d0a9e5bcb581efce5b33b221f2f4a27de8db66e463`  
		Last Modified: Thu, 30 Nov 2023 02:35:43 GMT  
		Size: 28.4 MB (28399939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95c7df977cc051774d451b6622a7dec0910ee80283f12ed6e3d66e2fa624c39`  
		Last Modified: Sat, 02 Dec 2023 07:34:00 GMT  
		Size: 12.1 MB (12113907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf78b7949b7938412395346e7762f4eb5ad37ff1949133997cd595759b22960b`  
		Last Modified: Sat, 02 Dec 2023 07:36:47 GMT  
		Size: 47.7 MB (47655530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8240d723a20952b47d4653771bb4dde9a91af51e2b41b7aae663f1c5738a6442`  
		Last Modified: Sat, 02 Dec 2023 07:36:43 GMT  
		Size: 4.5 MB (4533810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c6aa66718b26c6d5a248d50b26e2c5e5c16e8b0994b102a6a0f5d41ce05e09a`  
		Last Modified: Wed, 13 Dec 2023 19:26:19 GMT  
		Size: 42.3 KB (42316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9cf620bd3a7e31b45f19fae30129365d11c92666881929a36a5c3bae1204de`  
		Last Modified: Wed, 13 Dec 2023 19:26:20 GMT  
		Size: 17.1 MB (17144249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3a66458aa244f1dbf553550fd734d47ae5f8c0f5cf5d15dba628b57c6fc2a7`  
		Last Modified: Wed, 13 Dec 2023 19:26:19 GMT  
		Size: 608.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d90840aacb0a11ce1b82bef218c0ebf20265d148e71b2d2e88bb5274771309`  
		Last Modified: Wed, 13 Dec 2023 19:26:17 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9483e87c0c0d3c71f87b8c94febc7e2dde69df78fb3e28dfbf779363cb05b1a0`  
		Last Modified: Wed, 13 Dec 2023 19:26:17 GMT  
		Size: 11.4 KB (11444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80dcfee6ea52922581aee75d825ffa339900c57b1a863e96435c9dc0c27074c`  
		Last Modified: Wed, 13 Dec 2023 19:26:17 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d44d23a18302d14da500ea606d9091f7600c7d4d416db3d58fe69646b24b19`  
		Last Modified: Wed, 13 Dec 2023 19:26:17 GMT  
		Size: 12.4 KB (12360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6012eca469403138d2ba7dcebd274e0dd83b46ec8bf8d89b4cc828ee7df28ca`  
		Last Modified: Wed, 13 Dec 2023 19:26:18 GMT  
		Size: 2.7 MB (2654666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel-java17-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:ac37b7b77c9049b69daf9813e64daa7657b4477c5a06d7476b3009e6e61aa717
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.1 MB (122073170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3887e92b41b17798317eb5cb80490f12d6786112cc29de802a693cb1cc1328db`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 12 Dec 2023 11:43:51 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:43:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:43:55 GMT
ADD file:bda128b553d54e39b55daceea1f0ad351c73f83835bbf65d10e5af879ce6fee7 in / 
# Tue, 12 Dec 2023 11:43:56 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:56:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:56:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 11:04:25 GMT
ENV JAVA_VERSION=jdk-17.0.9+9_openj9-0.41.0
# Sat, 16 Dec 2023 11:06:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9760aa27a5790a8c20a702ff5f036535f3df51d3fb291bb5254b5ae76e096bad';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.9%2B9_openj9-0.41.0/ibm-semeru-open-jre_aarch64_linux_17.0.9_9_openj9-0.41.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='73b9baab2766191de5da00498f2dcfe9de90fff6c4c457bea4944f103c6dde6e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.9%2B9_openj9-0.41.0/ibm-semeru-open-jre_ppc64le_linux_17.0.9_9_openj9-0.41.0.tar.gz';          ;;        amd64|x86_64)          ESUM='1caf409f33f7738efe37742197525b5ae6244d6383b2017e7b8e925dc0b6a329';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.9%2B9_openj9-0.41.0/ibm-semeru-open-jre_x64_linux_17.0.9_9_openj9-0.41.0.tar.gz';          ;;        s390x)          ESUM='53e813367f3462e9dd66f8d4d3063c96bfd0cfc462b568187f62a5847ae01ad1';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.9%2B9_openj9-0.41.0/ibm-semeru-open-jre_s390x_linux_17.0.9_9_openj9-0.41.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 16 Dec 2023 11:06:35 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 11:06:37 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Sat, 16 Dec 2023 11:07:14 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Sat, 16 Dec 2023 13:59:46 GMT
USER root
# Sat, 16 Dec 2023 13:59:47 GMT
ARG VERBOSE=false
# Sat, 16 Dec 2023 13:59:47 GMT
ARG OPENJ9_SCC=true
# Sat, 16 Dec 2023 13:59:47 GMT
ARG LIBERTY_VERSION=23.0.0.12
# Sat, 16 Dec 2023 13:59:47 GMT
ARG LIBERTY_BUILD_LABEL=cl231220231127-1901
# Sat, 16 Dec 2023 13:59:48 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=23.0.0.12 org.opencontainers.image.revision=cl231220231127-1901 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Sat, 16 Dec 2023 13:59:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Sat, 16 Dec 2023 13:59:48 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=23.0.0.12 BuildLabel=cl231220231127-1901
# Sat, 16 Dec 2023 13:59:51 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_VERSION=23.0.0.12 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Sat, 16 Dec 2023 13:59:51 GMT
ARG LIBERTY_URL
# Sat, 16 Dec 2023 13:59:51 GMT
ARG DOWNLOAD_OPTIONS=
# Sat, 16 Dec 2023 14:00:06 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_VERSION=23.0.0.12 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 14:00:07 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Sat, 16 Dec 2023 14:00:08 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_VERSION=23.0.0.12 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env
# Sat, 16 Dec 2023 14:00:09 GMT
COPY file:7278f8f20139aab77b5c9fa76ad85e8a92836053c3ecfb9f5925f1a19788ef47 in /opt/ibm/NOTICES 
# Sat, 16 Dec 2023 14:00:09 GMT
COPY dir:254af54889f4a4b4a77147fe142eaaed75a79fca1e096326071edb660b9fa8b2 in /opt/ibm/helpers/ 
# Sat, 16 Dec 2023 14:00:09 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Sat, 16 Dec 2023 14:00:11 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_VERSION=23.0.0.12 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Sat, 16 Dec 2023 14:00:19 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_VERSION=23.0.0.12 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Sat, 16 Dec 2023 14:00:22 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Sat, 16 Dec 2023 14:00:22 GMT
USER 1001
# Sat, 16 Dec 2023 14:00:22 GMT
EXPOSE 9080 9443
# Sat, 16 Dec 2023 14:00:23 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Sat, 16 Dec 2023 14:00:24 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:7775720178c79208fc0d1b977c06891ef7230f39bc02e948d233c49f8a202fcf`  
		Last Modified: Sat, 16 Dec 2023 10:35:18 GMT  
		Size: 35.7 MB (35655287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbc811dfc8395d193589d30acb2a8cb783934cad69ab06a1989b2d9c01af4c8`  
		Last Modified: Sat, 16 Dec 2023 11:12:30 GMT  
		Size: 12.9 MB (12892026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0fb1ed5b0735764af6c23c8464ef841c1ba82ee3473f81187ed8c3c072fb38`  
		Last Modified: Sat, 16 Dec 2023 11:16:10 GMT  
		Size: 50.0 MB (49981919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c18095e5dbcc8d1946bb1996ab8ebd670f68056de194dc69c7de67b7c8cfbc5`  
		Last Modified: Sat, 16 Dec 2023 11:16:04 GMT  
		Size: 3.7 MB (3737136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb74f675a904b03414a2d1349d8fa3c4d838c4fa2e03096eac5c0cda284a680`  
		Last Modified: Sat, 16 Dec 2023 15:08:10 GMT  
		Size: 36.5 KB (36498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d6261cc65c635e679450c294a4161b3b7809897849f28ff61f61a2b7c35c24`  
		Last Modified: Sat, 16 Dec 2023 15:08:11 GMT  
		Size: 17.1 MB (17143584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c160fd128abcbe60294ca2e772f974a4065900f4c5ab5af53a9c5bf283cc00`  
		Last Modified: Sat, 16 Dec 2023 15:08:10 GMT  
		Size: 607.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab4a6ccd7b72af75d7f24e474478d87f39e6503d16d85d48519ba8bfa75e8be`  
		Last Modified: Sat, 16 Dec 2023 15:08:07 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67332fdb1d0d819a9e57f1389269969a6263c0e5f90fe002ec27a2d9b155c1b9`  
		Last Modified: Sat, 16 Dec 2023 15:08:08 GMT  
		Size: 11.4 KB (11440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a7f1dab0c9c5af25af7a88b71282bbcbbd6a1728ef0fdc200d90d1116d7093`  
		Last Modified: Sat, 16 Dec 2023 15:08:08 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da76e1b6efe9d530723de2a2f3a3e2dc172bbb6ec226ad7b1f1d8495cce598c`  
		Last Modified: Sat, 16 Dec 2023 15:08:07 GMT  
		Size: 12.4 KB (12368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e603153970875049f129d11d71188342bb28555b780be8a4e8278283311cff`  
		Last Modified: Sat, 16 Dec 2023 15:08:08 GMT  
		Size: 2.6 MB (2600518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel-java17-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:ebf8446420364499400ab9a3afaef5f1eef3290b8a674f105e7fdd62aa9e74fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113381454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aba9d0e2cfb0430c5c5df295b4513b0b4fb19ff03c9ece854217cd657ebd51ef`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 12 Dec 2023 11:44:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:44:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:44:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:44:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:44:59 GMT
ADD file:1729e720d10023da7d783040cefa8f30d3c61772a5e1ae577182a1fcba69aff1 in / 
# Tue, 12 Dec 2023 11:44:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 07:56:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 07:56:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 08:05:45 GMT
ENV JAVA_VERSION=jdk-17.0.9+9_openj9-0.41.0
# Sat, 16 Dec 2023 08:08:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9760aa27a5790a8c20a702ff5f036535f3df51d3fb291bb5254b5ae76e096bad';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.9%2B9_openj9-0.41.0/ibm-semeru-open-jre_aarch64_linux_17.0.9_9_openj9-0.41.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='73b9baab2766191de5da00498f2dcfe9de90fff6c4c457bea4944f103c6dde6e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.9%2B9_openj9-0.41.0/ibm-semeru-open-jre_ppc64le_linux_17.0.9_9_openj9-0.41.0.tar.gz';          ;;        amd64|x86_64)          ESUM='1caf409f33f7738efe37742197525b5ae6244d6383b2017e7b8e925dc0b6a329';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.9%2B9_openj9-0.41.0/ibm-semeru-open-jre_x64_linux_17.0.9_9_openj9-0.41.0.tar.gz';          ;;        s390x)          ESUM='53e813367f3462e9dd66f8d4d3063c96bfd0cfc462b568187f62a5847ae01ad1';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.9%2B9_openj9-0.41.0/ibm-semeru-open-jre_s390x_linux_17.0.9_9_openj9-0.41.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 16 Dec 2023 08:08:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 08:08:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Sat, 16 Dec 2023 08:08:39 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Sat, 16 Dec 2023 09:37:53 GMT
USER root
# Sat, 16 Dec 2023 09:37:53 GMT
ARG VERBOSE=false
# Sat, 16 Dec 2023 09:37:53 GMT
ARG OPENJ9_SCC=true
# Sat, 16 Dec 2023 09:37:53 GMT
ARG LIBERTY_VERSION=23.0.0.12
# Sat, 16 Dec 2023 09:37:53 GMT
ARG LIBERTY_BUILD_LABEL=cl231220231127-1901
# Sat, 16 Dec 2023 09:37:54 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=23.0.0.12 org.opencontainers.image.revision=cl231220231127-1901 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Sat, 16 Dec 2023 09:37:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Sat, 16 Dec 2023 09:37:54 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=23.0.0.12 BuildLabel=cl231220231127-1901
# Sat, 16 Dec 2023 09:37:55 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_VERSION=23.0.0.12 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Sat, 16 Dec 2023 09:37:55 GMT
ARG LIBERTY_URL
# Sat, 16 Dec 2023 09:37:55 GMT
ARG DOWNLOAD_OPTIONS=
# Sat, 16 Dec 2023 09:38:05 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_VERSION=23.0.0.12 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 09:38:06 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Sat, 16 Dec 2023 09:38:07 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_VERSION=23.0.0.12 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env
# Sat, 16 Dec 2023 09:38:07 GMT
COPY file:7278f8f20139aab77b5c9fa76ad85e8a92836053c3ecfb9f5925f1a19788ef47 in /opt/ibm/NOTICES 
# Sat, 16 Dec 2023 09:38:07 GMT
COPY dir:254af54889f4a4b4a77147fe142eaaed75a79fca1e096326071edb660b9fa8b2 in /opt/ibm/helpers/ 
# Sat, 16 Dec 2023 09:38:07 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Sat, 16 Dec 2023 09:38:08 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_VERSION=23.0.0.12 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Sat, 16 Dec 2023 09:38:12 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_VERSION=23.0.0.12 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Sat, 16 Dec 2023 09:38:12 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Sat, 16 Dec 2023 09:38:13 GMT
USER 1001
# Sat, 16 Dec 2023 09:38:13 GMT
EXPOSE 9080 9443
# Sat, 16 Dec 2023 09:38:13 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Sat, 16 Dec 2023 09:38:13 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:6949655473f9a6801351bc2ee9bef80a58f5ac2dd31547e0d4f473c53d282400`  
		Last Modified: Sat, 16 Dec 2023 07:42:42 GMT  
		Size: 28.7 MB (28654553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faadb4f032ac796bbd76d4fbd3ea1c6a3984cb437adc9d463772f3453f9e0a54`  
		Last Modified: Sat, 16 Dec 2023 08:13:40 GMT  
		Size: 12.2 MB (12199927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1319a29d200d79cc566d53caef1bb846e4dbb698b7db4ef52cf3867b36f3a42`  
		Last Modified: Sat, 16 Dec 2023 08:16:22 GMT  
		Size: 47.8 MB (47768230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632b8070a7edd04582bf2026f4eb9dfdf2b7a302d6cbd9d634dc9484bf81a78a`  
		Last Modified: Sat, 16 Dec 2023 08:16:16 GMT  
		Size: 4.9 MB (4878550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d28eb111e67b0d26cabfb3510be3812e7d8ddf8fe23d0ab6113b2768d3313f9`  
		Last Modified: Sat, 16 Dec 2023 10:34:55 GMT  
		Size: 33.1 KB (33111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb49d6eaa1aaae5548a02f078cbc91aaada3215ecfc63d51b2f4d06ae8771cb5`  
		Last Modified: Sat, 16 Dec 2023 10:34:56 GMT  
		Size: 17.1 MB (17143188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3202f095181b68e7fca834a6c88bd6bca7aba4d5b6661d6f1fc7b2503ba6a6`  
		Last Modified: Sat, 16 Dec 2023 10:34:55 GMT  
		Size: 613.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8f2e84538e424ce35a9f8c6320e92205ba6cb37a7c107a1eff7cd495dd0c61`  
		Last Modified: Sat, 16 Dec 2023 10:34:54 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11ef10626008cb109071895ac22c9ae61954c97d621ad68ff0bb82eb2a52d37`  
		Last Modified: Sat, 16 Dec 2023 10:34:54 GMT  
		Size: 11.4 KB (11439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ade17fd4c99b8bd4f713baaaf1af86cf59938444ded075c64e936a1478e0ef`  
		Last Modified: Sat, 16 Dec 2023 10:34:54 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe7b4aeb1bedc92e67b839b41e0f01520faecc4c185c4030dc31ab4d216e845`  
		Last Modified: Sat, 16 Dec 2023 10:34:54 GMT  
		Size: 12.4 KB (12365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46a88a76336245b6ec22aac5ff666bdac8f50165da293f4bc878b813464deb0`  
		Last Modified: Sat, 16 Dec 2023 10:34:54 GMT  
		Size: 2.7 MB (2677690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
