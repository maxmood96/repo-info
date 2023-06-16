## `open-liberty:latest`

```console
$ docker pull open-liberty@sha256:421989693e39d3087aba122a810e59cd2bf68a1c0c7f8b3bbadbf3894042a135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `open-liberty:latest` - linux; amd64

```console
$ docker pull open-liberty@sha256:278b392be5efd866e58a9428677b07e25eeb1214ecb79db1aea1496de03d2f4a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.1 MB (453077885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee43e077268814a9c2ae465f20de13eda28175c2ae89848f8f45f2ca4b44285`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 05 Jun 2023 17:08:57 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:08:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:08:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:08:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Jun 2023 17:08:58 GMT
ADD file:655d373cb551d0dd5d7867f88a4f98908dc3f16190986f693e88c423e6f21b8d in / 
# Mon, 05 Jun 2023 17:08:58 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:36:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:37:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:37:10 GMT
ENV JAVA_VERSION=jdk8u372-b07_openj9-0.38.0
# Fri, 16 Jun 2023 02:39:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='b0d830c47350de0b9d056d60f98b48d0452183bb640a03b316028e3c7d603162';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u372-b07_openj9-0.38.0/ibm-semeru-open-jre_aarch64_linux_8u372b07_openj9-0.38.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='30e9a4c4bd693128a6d3e9244495b1ffc0255af9eb6183247b7c03580337284c';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u372-b07_openj9-0.38.0/ibm-semeru-open-jre_ppc64le_linux_8u372b07_openj9-0.38.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ad0829fbd2473704e8103524882bc25625958b6f3038e80f8a99ab926e6b58a3';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u372-b07_openj9-0.38.0/ibm-semeru-open-jre_x64_linux_8u372b07_openj9-0.38.0.tar.gz';          ;;        s390x)          ESUM='5a0e098267ea57c5088c2c9d2a6f6bf0f8f3e1ed6fd6f1ebf4a7a94e02352dc4';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u372-b07_openj9-0.38.0/ibm-semeru-open-jre_s390x_linux_8u372b07_openj9-0.38.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 16 Jun 2023 02:39:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:39:09 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 16 Jun 2023 02:39:44 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 16 Jun 2023 07:55:46 GMT
ARG LIBERTY_VERSION=23.0.0.5
# Fri, 16 Jun 2023 07:56:38 GMT
ARG LIBERTY_SHA=4ee902cc2b5a775349510c9025af50d90f1c072a
# Fri, 16 Jun 2023 07:56:38 GMT
ARG LIBERTY_BUILD_LABEL=cl230520230514-1901
# Fri, 16 Jun 2023 07:56:38 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.5/openliberty-runtime-23.0.0.5.zip
# Fri, 16 Jun 2023 07:56:38 GMT
ARG OPENJ9_SCC=true
# Fri, 16 Jun 2023 07:56:38 GMT
ARG VERBOSE=false
# Fri, 16 Jun 2023 07:56:38 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl230520230514-1901 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=23.0.0.5
# Fri, 16 Jun 2023 07:56:38 GMT
COPY dir:773abd8b4cf4a2ffc55415a59f9d771027eaed2ee34c2c442c7e03d21abd00e5 in /opt/ol/helpers 
# Fri, 16 Jun 2023 07:56:38 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Fri, 16 Jun 2023 07:56:56 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230520230514-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.5/openliberty-runtime-23.0.0.5.zip LIBERTY_SHA=4ee902cc2b5a775349510c9025af50d90f1c072a LIBERTY_VERSION=23.0.0.5 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Fri, 16 Jun 2023 07:56:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 16 Jun 2023 07:56:58 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230520230514-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.5/openliberty-runtime-23.0.0.5.zip LIBERTY_SHA=4ee902cc2b5a775349510c9025af50d90f1c072a LIBERTY_VERSION=23.0.0.5 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 16 Jun 2023 07:56:58 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230520230514-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.5/openliberty-runtime-23.0.0.5.zip LIBERTY_SHA=4ee902cc2b5a775349510c9025af50d90f1c072a LIBERTY_VERSION=23.0.0.5 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Fri, 16 Jun 2023 07:57:22 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230520230514-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.5/openliberty-runtime-23.0.0.5.zip LIBERTY_SHA=4ee902cc2b5a775349510c9025af50d90f1c072a LIBERTY_VERSION=23.0.0.5 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Fri, 16 Jun 2023 07:57:23 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 16 Jun 2023 07:57:23 GMT
USER 1001
# Fri, 16 Jun 2023 07:57:23 GMT
EXPOSE 9080 9443
# Fri, 16 Jun 2023 07:57:23 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 16 Jun 2023 07:57:23 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:f0412dfb1aaea4892c13dab6f771bcd79641a4bdcb521ce881f5dcfc0df9a7a5`  
		Last Modified: Tue, 06 Jun 2023 09:20:27 GMT  
		Size: 28.6 MB (28580519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5b8a6c177da705d4046b823b19504b0d011f22ae445a4767227c0d7e59cb55`  
		Last Modified: Fri, 16 Jun 2023 02:51:36 GMT  
		Size: 16.1 MB (16057515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cba04b0a6e2aea848de1669fe77af3668c4b5d579ca76ff599570f7cc048ba`  
		Last Modified: Fri, 16 Jun 2023 02:52:14 GMT  
		Size: 50.3 MB (50259599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b050d34526d4d5f599b0024ef5585bbcc832a08b70825e2b5808d05deb5c732`  
		Last Modified: Fri, 16 Jun 2023 02:52:10 GMT  
		Size: 4.2 MB (4207735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932a0201b3cf2aa3a828bd2fa7a7089357ac3887e05bcc45b639f24fadfc1c62`  
		Last Modified: Fri, 16 Jun 2023 08:08:09 GMT  
		Size: 8.7 KB (8660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c6d830f6a158e6d4907c27455196cbb9ae1ada08076d14c5dda4bf25d0f22c`  
		Last Modified: Fri, 16 Jun 2023 08:08:07 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66dd494e951232d6446ede980c24fd70ef45de61877b430ab7fb9ed7ce12cb36`  
		Last Modified: Fri, 16 Jun 2023 08:08:22 GMT  
		Size: 340.1 MB (340069693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa51878d1b2db7a59ec9293f41aeff70270bb82522664013af871d77353945aa`  
		Last Modified: Fri, 16 Jun 2023 08:08:07 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a7e712f1f404bc8995544846eba603a60132a9d532b1c1c92ef0da05ff2966`  
		Last Modified: Fri, 16 Jun 2023 08:08:07 GMT  
		Size: 10.2 KB (10187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb1d509599aefdb0a6f9c394618efc99d1894528e065d2e1e395b53da7b36db`  
		Last Modified: Fri, 16 Jun 2023 08:08:09 GMT  
		Size: 13.9 MB (13882466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:latest` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:2867c9ca950381b22fd3c2fc6fe2bbf4b470f9cbce49458947eb315542348056
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.9 MB (448915616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9039392ef5dc82d54566262f12d76f8cb8bd725089b1a8bbf5df0e772e1738e6`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 05 Jun 2023 17:07:59 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:07:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:07:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:07:59 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Jun 2023 17:08:02 GMT
ADD file:6c0661b94e27ede70ca2a8842bdab5bc26b9ae4760b17870eda9d595672795ff in / 
# Mon, 05 Jun 2023 17:08:02 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:54:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:54:26 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:54:27 GMT
ENV JAVA_VERSION=jdk8u372-b07_openj9-0.38.0
# Fri, 16 Jun 2023 02:56:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='b0d830c47350de0b9d056d60f98b48d0452183bb640a03b316028e3c7d603162';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u372-b07_openj9-0.38.0/ibm-semeru-open-jre_aarch64_linux_8u372b07_openj9-0.38.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='30e9a4c4bd693128a6d3e9244495b1ffc0255af9eb6183247b7c03580337284c';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u372-b07_openj9-0.38.0/ibm-semeru-open-jre_ppc64le_linux_8u372b07_openj9-0.38.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ad0829fbd2473704e8103524882bc25625958b6f3038e80f8a99ab926e6b58a3';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u372-b07_openj9-0.38.0/ibm-semeru-open-jre_x64_linux_8u372b07_openj9-0.38.0.tar.gz';          ;;        s390x)          ESUM='5a0e098267ea57c5088c2c9d2a6f6bf0f8f3e1ed6fd6f1ebf4a7a94e02352dc4';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u372-b07_openj9-0.38.0/ibm-semeru-open-jre_s390x_linux_8u372b07_openj9-0.38.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 16 Jun 2023 02:56:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:56:19 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 16 Jun 2023 02:56:53 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 16 Jun 2023 08:05:54 GMT
ARG LIBERTY_VERSION=23.0.0.5
# Fri, 16 Jun 2023 08:06:35 GMT
ARG LIBERTY_SHA=4ee902cc2b5a775349510c9025af50d90f1c072a
# Fri, 16 Jun 2023 08:06:35 GMT
ARG LIBERTY_BUILD_LABEL=cl230520230514-1901
# Fri, 16 Jun 2023 08:06:35 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.5/openliberty-runtime-23.0.0.5.zip
# Fri, 16 Jun 2023 08:06:35 GMT
ARG OPENJ9_SCC=true
# Fri, 16 Jun 2023 08:06:35 GMT
ARG VERBOSE=false
# Fri, 16 Jun 2023 08:06:35 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl230520230514-1901 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=23.0.0.5
# Fri, 16 Jun 2023 08:06:35 GMT
COPY dir:773abd8b4cf4a2ffc55415a59f9d771027eaed2ee34c2c442c7e03d21abd00e5 in /opt/ol/helpers 
# Fri, 16 Jun 2023 08:06:35 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Fri, 16 Jun 2023 08:06:48 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230520230514-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.5/openliberty-runtime-23.0.0.5.zip LIBERTY_SHA=4ee902cc2b5a775349510c9025af50d90f1c072a LIBERTY_VERSION=23.0.0.5 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Fri, 16 Jun 2023 08:06:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 16 Jun 2023 08:06:51 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230520230514-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.5/openliberty-runtime-23.0.0.5.zip LIBERTY_SHA=4ee902cc2b5a775349510c9025af50d90f1c072a LIBERTY_VERSION=23.0.0.5 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 16 Jun 2023 08:06:52 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230520230514-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.5/openliberty-runtime-23.0.0.5.zip LIBERTY_SHA=4ee902cc2b5a775349510c9025af50d90f1c072a LIBERTY_VERSION=23.0.0.5 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Fri, 16 Jun 2023 08:07:12 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230520230514-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.5/openliberty-runtime-23.0.0.5.zip LIBERTY_SHA=4ee902cc2b5a775349510c9025af50d90f1c072a LIBERTY_VERSION=23.0.0.5 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Fri, 16 Jun 2023 08:07:12 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 16 Jun 2023 08:07:12 GMT
USER 1001
# Fri, 16 Jun 2023 08:07:12 GMT
EXPOSE 9080 9443
# Fri, 16 Jun 2023 08:07:12 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 16 Jun 2023 08:07:12 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:29c851dfb906fc3c51d9a9d53a0cfa8ea88e10040baaf47155e04bf87ce3f3a5`  
		Last Modified: Fri, 09 Jun 2023 02:40:24 GMT  
		Size: 27.2 MB (27200436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908d2a4439128f77a97999ae3e8e9e21642cbb5fe6d8e9516d0c2c579a631ee2`  
		Last Modified: Fri, 16 Jun 2023 03:07:56 GMT  
		Size: 15.9 MB (15926389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f460d7b2590153895f91ced805895a29e25feefc7d462a8610ec0814b9f3140b`  
		Last Modified: Fri, 16 Jun 2023 03:08:31 GMT  
		Size: 48.4 MB (48420073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52aa993790593ac858793bd9f66639e10df1f188f51bd0376c22d0b6430cfbe7`  
		Last Modified: Fri, 16 Jun 2023 03:08:28 GMT  
		Size: 4.1 MB (4064409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2caec7bd1867928d54b9a18e25af899a59465918e6e203c9fffe0dabbd008495`  
		Last Modified: Fri, 16 Jun 2023 08:16:18 GMT  
		Size: 8.7 KB (8658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b678157922b12acc6698134bfabcb157b9fd0e3c8d910c6b9b8a5347c8facf2d`  
		Last Modified: Fri, 16 Jun 2023 08:16:17 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0132c867c67b6ca9b1f4017aefa7ffca8d3a0817fb87b1b1175bc6de898109b`  
		Last Modified: Fri, 16 Jun 2023 08:16:29 GMT  
		Size: 340.1 MB (340071094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd7eb95819c2a983b6893163c0f306930f4cc5f62c1ccf7d7c8e5e577fe7858`  
		Last Modified: Fri, 16 Jun 2023 08:16:17 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce281e1c57065ff3fa0a8708bf181cfea57c562d86aecf3633ef61d7db3d031`  
		Last Modified: Fri, 16 Jun 2023 08:16:16 GMT  
		Size: 10.2 KB (10179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ca06095419e3e6c1b306af4c9089352661c176992a598474a578ad707d0f4c`  
		Last Modified: Fri, 16 Jun 2023 08:16:18 GMT  
		Size: 13.2 MB (13212868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:latest` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:b5dd20a78d86bf914064d0f02ba177554b1f6355a20fb96e4f7eede5ee5ec45f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **457.5 MB (457509961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caadffdba8829db6ea90f0aa327b649027fb09a9d3e8ca3b2e367cbaf7a0fafc`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:24:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:25:21 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 00:16:41 GMT
ENV JAVA_VERSION=jdk8u372-b07_openj9-0.38.0
# Thu, 01 Jun 2023 00:19:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='b0d830c47350de0b9d056d60f98b48d0452183bb640a03b316028e3c7d603162';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u372-b07_openj9-0.38.0/ibm-semeru-open-jre_aarch64_linux_8u372b07_openj9-0.38.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='30e9a4c4bd693128a6d3e9244495b1ffc0255af9eb6183247b7c03580337284c';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u372-b07_openj9-0.38.0/ibm-semeru-open-jre_ppc64le_linux_8u372b07_openj9-0.38.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ad0829fbd2473704e8103524882bc25625958b6f3038e80f8a99ab926e6b58a3';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u372-b07_openj9-0.38.0/ibm-semeru-open-jre_x64_linux_8u372b07_openj9-0.38.0.tar.gz';          ;;        s390x)          ESUM='5a0e098267ea57c5088c2c9d2a6f6bf0f8f3e1ed6fd6f1ebf4a7a94e02352dc4';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u372-b07_openj9-0.38.0/ibm-semeru-open-jre_s390x_linux_8u372b07_openj9-0.38.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 01 Jun 2023 00:19:22 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jun 2023 00:19:24 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 01 Jun 2023 00:20:04 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 09 Jun 2023 08:23:14 GMT
ARG LIBERTY_VERSION=23.0.0.5
# Fri, 09 Jun 2023 08:24:47 GMT
ARG LIBERTY_SHA=4ee902cc2b5a775349510c9025af50d90f1c072a
# Fri, 09 Jun 2023 08:24:47 GMT
ARG LIBERTY_BUILD_LABEL=cl230520230514-1901
# Fri, 09 Jun 2023 08:24:48 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.5/openliberty-runtime-23.0.0.5.zip
# Fri, 09 Jun 2023 08:24:48 GMT
ARG OPENJ9_SCC=true
# Fri, 09 Jun 2023 08:24:48 GMT
ARG VERBOSE=false
# Fri, 09 Jun 2023 08:24:49 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl230520230514-1901 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=23.0.0.5
# Fri, 09 Jun 2023 08:24:49 GMT
COPY dir:773abd8b4cf4a2ffc55415a59f9d771027eaed2ee34c2c442c7e03d21abd00e5 in /opt/ol/helpers 
# Fri, 09 Jun 2023 08:24:49 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Fri, 09 Jun 2023 08:25:30 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230520230514-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.5/openliberty-runtime-23.0.0.5.zip LIBERTY_SHA=4ee902cc2b5a775349510c9025af50d90f1c072a LIBERTY_VERSION=23.0.0.5 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Fri, 09 Jun 2023 08:25:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 09 Jun 2023 08:25:38 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230520230514-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.5/openliberty-runtime-23.0.0.5.zip LIBERTY_SHA=4ee902cc2b5a775349510c9025af50d90f1c072a LIBERTY_VERSION=23.0.0.5 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 09 Jun 2023 08:25:39 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230520230514-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.5/openliberty-runtime-23.0.0.5.zip LIBERTY_SHA=4ee902cc2b5a775349510c9025af50d90f1c072a LIBERTY_VERSION=23.0.0.5 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Fri, 09 Jun 2023 08:26:25 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230520230514-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.5/openliberty-runtime-23.0.0.5.zip LIBERTY_SHA=4ee902cc2b5a775349510c9025af50d90f1c072a LIBERTY_VERSION=23.0.0.5 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Fri, 09 Jun 2023 08:26:27 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 09 Jun 2023 08:26:27 GMT
USER 1001
# Fri, 09 Jun 2023 08:26:28 GMT
EXPOSE 9080 9443
# Fri, 09 Jun 2023 08:26:28 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 09 Jun 2023 08:26:30 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:d276072145993a42aed3e2b3e8cd26b6e08aab266d9c9d792ee89b26150681da`  
		Last Modified: Fri, 14 Apr 2023 09:36:00 GMT  
		Size: 33.3 MB (33300980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a328f93092ceadb7a1b931cc278addf4dfae1321b9f8ced8d4ea73dc90facfb`  
		Last Modified: Tue, 18 Apr 2023 01:34:37 GMT  
		Size: 17.2 MB (17176898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed6cd86f3acf3fd82aad73cbe9152dc0edcf31cf12d66c35b3addb6d8aba01e`  
		Last Modified: Thu, 01 Jun 2023 00:32:08 GMT  
		Size: 50.8 MB (50758395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9efae1f790de2c12e2e59b9dafdf215ba4df54d8cd8ac34b05dad888974a534`  
		Last Modified: Thu, 01 Jun 2023 00:31:59 GMT  
		Size: 3.6 MB (3550910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac45ceeaf2a4c5a09415d55a97f7369b02c75902a8298a8c38e2054cb8c48680`  
		Last Modified: Fri, 09 Jun 2023 08:41:01 GMT  
		Size: 8.7 KB (8663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a51d6d1b61ee524c2effd56dd78f3aa6a87557cfc0a6e133fe7c278b2074c6f`  
		Last Modified: Fri, 09 Jun 2023 08:41:00 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410c2d8925ef3f3ed4aaa08fdb3e23c799153bef629a087bda672165746ee525`  
		Last Modified: Fri, 09 Jun 2023 08:41:27 GMT  
		Size: 340.4 MB (340402090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b92918506ce0ab25f8e70a7646fd3b9a367d2aae7bde8867180bb6b98e05556`  
		Last Modified: Fri, 09 Jun 2023 08:40:59 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb684b8d9b5cd213522b1341bcfdc3d5903a15b64b1a87da9817331cc06a105c`  
		Last Modified: Fri, 09 Jun 2023 08:40:59 GMT  
		Size: 10.2 KB (10194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abc3fc85eaa1870d262e7ca9ebe4f22dc1c8e7430389daec03d55a8ac526f1f`  
		Last Modified: Fri, 09 Jun 2023 08:41:02 GMT  
		Size: 12.3 MB (12300309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:latest` - linux; s390x

```console
$ docker pull open-liberty@sha256:45a4e37fb55144cdd5f4a4791cc2986c2f392f042d098a0381b37a37ee272050
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.4 MB (451355646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3712fab6509ce5504008803c2d6e154ef0fb368fd15d0385398d0901ee6eb6`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:35 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:37 GMT
ADD file:44c66c03ba0afcc05de1b2078f83e8bfe04706b31491fcd3fdd93cfc88d5f06c in / 
# Thu, 13 Apr 2023 13:09:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:20:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:20:42 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 31 May 2023 23:43:01 GMT
ENV JAVA_VERSION=jdk8u372-b07_openj9-0.38.0
# Wed, 31 May 2023 23:44:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='b0d830c47350de0b9d056d60f98b48d0452183bb640a03b316028e3c7d603162';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u372-b07_openj9-0.38.0/ibm-semeru-open-jre_aarch64_linux_8u372b07_openj9-0.38.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='30e9a4c4bd693128a6d3e9244495b1ffc0255af9eb6183247b7c03580337284c';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u372-b07_openj9-0.38.0/ibm-semeru-open-jre_ppc64le_linux_8u372b07_openj9-0.38.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ad0829fbd2473704e8103524882bc25625958b6f3038e80f8a99ab926e6b58a3';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u372-b07_openj9-0.38.0/ibm-semeru-open-jre_x64_linux_8u372b07_openj9-0.38.0.tar.gz';          ;;        s390x)          ESUM='5a0e098267ea57c5088c2c9d2a6f6bf0f8f3e1ed6fd6f1ebf4a7a94e02352dc4';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u372-b07_openj9-0.38.0/ibm-semeru-open-jre_s390x_linux_8u372b07_openj9-0.38.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 31 May 2023 23:44:57 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 May 2023 23:44:57 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 31 May 2023 23:45:30 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 09 Jun 2023 04:11:21 GMT
ARG LIBERTY_VERSION=23.0.0.5
# Fri, 09 Jun 2023 04:12:17 GMT
ARG LIBERTY_SHA=4ee902cc2b5a775349510c9025af50d90f1c072a
# Fri, 09 Jun 2023 04:12:17 GMT
ARG LIBERTY_BUILD_LABEL=cl230520230514-1901
# Fri, 09 Jun 2023 04:12:17 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.5/openliberty-runtime-23.0.0.5.zip
# Fri, 09 Jun 2023 04:12:18 GMT
ARG OPENJ9_SCC=true
# Fri, 09 Jun 2023 04:12:18 GMT
ARG VERBOSE=false
# Fri, 09 Jun 2023 04:12:18 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl230520230514-1901 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=23.0.0.5
# Fri, 09 Jun 2023 04:12:18 GMT
COPY dir:773abd8b4cf4a2ffc55415a59f9d771027eaed2ee34c2c442c7e03d21abd00e5 in /opt/ol/helpers 
# Fri, 09 Jun 2023 04:12:18 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Fri, 09 Jun 2023 04:12:40 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230520230514-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.5/openliberty-runtime-23.0.0.5.zip LIBERTY_SHA=4ee902cc2b5a775349510c9025af50d90f1c072a LIBERTY_VERSION=23.0.0.5 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Fri, 09 Jun 2023 04:12:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 09 Jun 2023 04:12:49 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230520230514-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.5/openliberty-runtime-23.0.0.5.zip LIBERTY_SHA=4ee902cc2b5a775349510c9025af50d90f1c072a LIBERTY_VERSION=23.0.0.5 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 09 Jun 2023 04:12:50 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230520230514-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.5/openliberty-runtime-23.0.0.5.zip LIBERTY_SHA=4ee902cc2b5a775349510c9025af50d90f1c072a LIBERTY_VERSION=23.0.0.5 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Fri, 09 Jun 2023 04:13:10 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230520230514-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.5/openliberty-runtime-23.0.0.5.zip LIBERTY_SHA=4ee902cc2b5a775349510c9025af50d90f1c072a LIBERTY_VERSION=23.0.0.5 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Fri, 09 Jun 2023 04:13:11 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 09 Jun 2023 04:13:11 GMT
USER 1001
# Fri, 09 Jun 2023 04:13:11 GMT
EXPOSE 9080 9443
# Fri, 09 Jun 2023 04:13:11 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 09 Jun 2023 04:13:11 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:f11b609b1d63f2d37c0e3789823e7a7e62a078bddca7c46da8602655989c62d9`  
		Last Modified: Fri, 14 Apr 2023 09:38:39 GMT  
		Size: 27.0 MB (27016370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904a0c815c072ccdf47e2b629d60ff91ad3ae9a1485d39c406b7c5e846233b1c`  
		Last Modified: Tue, 18 Apr 2023 01:29:20 GMT  
		Size: 15.7 MB (15693377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0035bd1ad5e27c9f579a780ebe65a17fa3b05ea00b73d6a266bb72271fa9ae4d`  
		Last Modified: Wed, 31 May 2023 23:55:19 GMT  
		Size: 50.2 MB (50170377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cade5ea768fba19782b48f6c450de05b34f9e2a638d75fdf13b5173e7634ba35`  
		Last Modified: Wed, 31 May 2023 23:55:14 GMT  
		Size: 4.3 MB (4333467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f049a3639fc85fe48f3973de18baed4106c09e1641025fbb59381cd67b97728f`  
		Last Modified: Fri, 09 Jun 2023 04:22:00 GMT  
		Size: 8.7 KB (8661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d5199743775035be2ab696ab6cd2e1fd456b8341e7b7f7084808e06a8ea58b`  
		Last Modified: Fri, 09 Jun 2023 04:21:58 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016aaf5df2d2c72dbef4f2f6d5cada6376f0cdd4051f16b4c87fde37e28e497b`  
		Last Modified: Fri, 09 Jun 2023 04:22:12 GMT  
		Size: 340.4 MB (340383720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e340e26880ad46c46dceb33500d37f8230c37d52cdccb87bd4549d5e81ee8f43`  
		Last Modified: Fri, 09 Jun 2023 04:21:58 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840224d5e5f3939a1cf2a7611c983992d1b70e432b94e35e11f2a8d962491f3f`  
		Last Modified: Fri, 09 Jun 2023 04:21:58 GMT  
		Size: 10.2 KB (10181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0269b5e631798d914127c8811088f6f8b73bc12119cb28b810dd5a4492f69579`  
		Last Modified: Fri, 09 Jun 2023 04:22:00 GMT  
		Size: 13.7 MB (13737978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
