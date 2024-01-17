## `open-liberty:kernel-slim`

```console
$ docker pull open-liberty@sha256:2e2d40542033a0822da5b79cba6900bcc50815355ae5703db6ebdbf599212e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `open-liberty:kernel-slim` - linux; amd64

```console
$ docker pull open-liberty@sha256:dee9f83d96289cb7fe71642c8d9c4aa9d9797c73fd814bdef14991eb0e7b52be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (113960785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691eea09200da66fc134f19a530680c7cdbe3aa2d8330bb53fef27aa3ec6f300`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 11 Jan 2024 17:08:09 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:08:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:08:11 GMT
ADD file:c646150c866c8b5ece67bc79c610718acf858034fa22502b0dba3d38c53fc9a9 in / 
# Thu, 11 Jan 2024 17:08:11 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:23:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 07:23:41 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 07:23:42 GMT
ENV JAVA_VERSION=jdk8u392-b08_openj9-0.41.0
# Wed, 17 Jan 2024 07:24:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='17df56bf2567bcca36d78ac4e46d025aec2553ba4df0b18c89464fcfebf9bb21';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_aarch64_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='3991f050a560a6ef21c1f3e08ce84302c4d41b923502667c23dac21e82706a0c';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_ppc64le_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        amd64|x86_64)          ESUM='2e771721212f403dd97a132ddcd20b4ed2d0ee95d504c299517a8ce58590690e';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_x64_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        s390x)          ESUM='5108b16f79176b501d9b5e5950bb143ffcf839da6472940bb62279db529e2630';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_s390x_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 17 Jan 2024 07:24:35 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 07:24:36 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 17 Jan 2024 07:25:08 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3f022ec8552bce1b72eb85d0778c93052ccb00226de3302544ec844ab93a9991e19c2db56ed06c18f03e5d75f34a46cedac46ae83bdd225518a55c62fc69ea04";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.83/bin/apache-tomcat-9.0.83.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 17 Jan 2024 19:27:12 GMT
USER root
# Wed, 17 Jan 2024 19:30:08 GMT
ARG LIBERTY_VERSION=23.0.0.12
# Wed, 17 Jan 2024 19:30:08 GMT
ARG LIBERTY_SHA=f8b7fb58f928ba135e01fedf18d37b0de9848ccc
# Wed, 17 Jan 2024 19:30:08 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.12/openliberty-kernel-23.0.0.12.zip
# Wed, 17 Jan 2024 19:30:08 GMT
ARG LIBERTY_BUILD_LABEL=cl231220231127-1901
# Wed, 17 Jan 2024 19:30:08 GMT
ARG OPENJ9_SCC=true
# Wed, 17 Jan 2024 19:30:08 GMT
ARG VERBOSE=false
# Wed, 17 Jan 2024 19:30:08 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl231220231127-1901 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=23.0.0.12
# Wed, 17 Jan 2024 19:30:08 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Wed, 17 Jan 2024 19:30:08 GMT
COPY dir:97cf6279dcb954616dcf6e80b110334a500f1803178f9fea6d45ccc032b92466 in /opt/ol/helpers 
# Wed, 17 Jan 2024 19:30:09 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Wed, 17 Jan 2024 19:30:10 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.12/openliberty-kernel-23.0.0.12.zip LIBERTY_SHA=f8b7fb58f928ba135e01fedf18d37b0de9848ccc LIBERTY_VERSION=23.0.0.12 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Wed, 17 Jan 2024 19:30:18 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.12/openliberty-kernel-23.0.0.12.zip LIBERTY_SHA=f8b7fb58f928ba135e01fedf18d37b0de9848ccc LIBERTY_VERSION=23.0.0.12 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Wed, 17 Jan 2024 19:30:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 17 Jan 2024 19:30:19 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.12/openliberty-kernel-23.0.0.12.zip LIBERTY_SHA=f8b7fb58f928ba135e01fedf18d37b0de9848ccc LIBERTY_VERSION=23.0.0.12 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Wed, 17 Jan 2024 19:30:19 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.12/openliberty-kernel-23.0.0.12.zip LIBERTY_SHA=f8b7fb58f928ba135e01fedf18d37b0de9848ccc LIBERTY_VERSION=23.0.0.12 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Wed, 17 Jan 2024 19:30:24 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.12/openliberty-kernel-23.0.0.12.zip LIBERTY_SHA=f8b7fb58f928ba135e01fedf18d37b0de9848ccc LIBERTY_VERSION=23.0.0.12 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Wed, 17 Jan 2024 19:30:24 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 17 Jan 2024 19:30:24 GMT
USER 1001
# Wed, 17 Jan 2024 19:30:24 GMT
EXPOSE 9080 9443
# Wed, 17 Jan 2024 19:30:24 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 17 Jan 2024 19:30:24 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:df2fac849a4581b035132d99e203fd83dc65590ea565435a266cb0e14a508838`  
		Last Modified: Thu, 11 Jan 2024 22:28:44 GMT  
		Size: 30.4 MB (30447114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ccd42b271e8a4254551e0e36bfc9b0533c035df83e2ebaad930433e9bc1529f`  
		Last Modified: Wed, 17 Jan 2024 07:30:59 GMT  
		Size: 12.2 MB (12158919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb47686bb4f36af8338b1deee7b5746e73655d66c5a5058ba3da30940104cce1`  
		Last Modified: Wed, 17 Jan 2024 07:31:23 GMT  
		Size: 50.2 MB (50214668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67683df497e53845264f560132632e28bd3dcd7f4ad4efa19c4fccea611f7263`  
		Last Modified: Wed, 17 Jan 2024 07:31:18 GMT  
		Size: 4.2 MB (4213862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a2f25b6a1f1776cf5d3dcb032ed89de6fc5d7f7db6b76b12582f06ca383e884`  
		Last Modified: Wed, 17 Jan 2024 19:42:31 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f712602125acd799416c1bff8311b0ce043da3c1e5f700b01fa447a99b7184`  
		Last Modified: Wed, 17 Jan 2024 19:42:31 GMT  
		Size: 9.1 KB (9128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193ff4240915c3e4bd4755a4a054e1e623a41a9aef028a11a1457107d44b62ab`  
		Last Modified: Wed, 17 Jan 2024 19:42:31 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9d66f5e9f14bdc2c7526431ad2b837e8c0b59c49f42e713c54758fb9e83566`  
		Last Modified: Wed, 17 Jan 2024 19:42:29 GMT  
		Size: 31.8 KB (31751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d230774f1aa20c8e564eef7e5a40badd2f645577e10e8c233dc5422f2165ffce`  
		Last Modified: Wed, 17 Jan 2024 19:42:30 GMT  
		Size: 14.3 MB (14252858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8eff9ae2b1699693fdd39ca30a986dc5a159c06364c54fadc5d03295cd0fcd7`  
		Last Modified: Wed, 17 Jan 2024 19:42:29 GMT  
		Size: 863.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732c11e4a54160465b7752f28eadd1b78d92bdd5797ef509029c07e2f8cef10c`  
		Last Modified: Wed, 17 Jan 2024 19:42:29 GMT  
		Size: 10.2 KB (10217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee57e9f607e774df4f5151767c0682da521b48ac90356c571851a1bfe78a3a4`  
		Last Modified: Wed, 17 Jan 2024 19:42:30 GMT  
		Size: 2.6 MB (2620061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:kernel-slim` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:f0901b643a4b4ec0b519b98a2eb525c4d2a678df396f7b9c04582d59971d47a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110528180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aacf1783df316fe552d3bce896870e5e6b0bcd83e229364793551b68b6e2bdfd`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 11 Jan 2024 17:03:13 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:03:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:03:15 GMT
ADD file:5703a6689620ec495e864cfc12e80f8b2ee9e69b1a7b7365bf80955ba05a53ab in / 
# Thu, 11 Jan 2024 17:03:15 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:04:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 07:04:17 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 07:04:17 GMT
ENV JAVA_VERSION=jdk8u392-b08_openj9-0.41.0
# Wed, 17 Jan 2024 07:05:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='17df56bf2567bcca36d78ac4e46d025aec2553ba4df0b18c89464fcfebf9bb21';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_aarch64_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='3991f050a560a6ef21c1f3e08ce84302c4d41b923502667c23dac21e82706a0c';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_ppc64le_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        amd64|x86_64)          ESUM='2e771721212f403dd97a132ddcd20b4ed2d0ee95d504c299517a8ce58590690e';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_x64_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        s390x)          ESUM='5108b16f79176b501d9b5e5950bb143ffcf839da6472940bb62279db529e2630';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_s390x_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 17 Jan 2024 07:05:11 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 07:05:11 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 17 Jan 2024 07:05:42 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3f022ec8552bce1b72eb85d0778c93052ccb00226de3302544ec844ab93a9991e19c2db56ed06c18f03e5d75f34a46cedac46ae83bdd225518a55c62fc69ea04";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.83/bin/apache-tomcat-9.0.83.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 17 Jan 2024 15:01:40 GMT
USER root
# Wed, 17 Jan 2024 15:04:25 GMT
ARG LIBERTY_VERSION=23.0.0.12
# Wed, 17 Jan 2024 15:04:25 GMT
ARG LIBERTY_SHA=f8b7fb58f928ba135e01fedf18d37b0de9848ccc
# Wed, 17 Jan 2024 15:04:25 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.12/openliberty-kernel-23.0.0.12.zip
# Wed, 17 Jan 2024 15:04:25 GMT
ARG LIBERTY_BUILD_LABEL=cl231220231127-1901
# Wed, 17 Jan 2024 15:04:25 GMT
ARG OPENJ9_SCC=true
# Wed, 17 Jan 2024 15:04:25 GMT
ARG VERBOSE=false
# Wed, 17 Jan 2024 15:04:25 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl231220231127-1901 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=23.0.0.12
# Wed, 17 Jan 2024 15:04:25 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Wed, 17 Jan 2024 15:04:25 GMT
COPY dir:97cf6279dcb954616dcf6e80b110334a500f1803178f9fea6d45ccc032b92466 in /opt/ol/helpers 
# Wed, 17 Jan 2024 15:04:25 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Wed, 17 Jan 2024 15:04:27 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.12/openliberty-kernel-23.0.0.12.zip LIBERTY_SHA=f8b7fb58f928ba135e01fedf18d37b0de9848ccc LIBERTY_VERSION=23.0.0.12 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Wed, 17 Jan 2024 15:04:32 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.12/openliberty-kernel-23.0.0.12.zip LIBERTY_SHA=f8b7fb58f928ba135e01fedf18d37b0de9848ccc LIBERTY_VERSION=23.0.0.12 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Wed, 17 Jan 2024 15:04:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 17 Jan 2024 15:04:33 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.12/openliberty-kernel-23.0.0.12.zip LIBERTY_SHA=f8b7fb58f928ba135e01fedf18d37b0de9848ccc LIBERTY_VERSION=23.0.0.12 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Wed, 17 Jan 2024 15:04:34 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.12/openliberty-kernel-23.0.0.12.zip LIBERTY_SHA=f8b7fb58f928ba135e01fedf18d37b0de9848ccc LIBERTY_VERSION=23.0.0.12 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Wed, 17 Jan 2024 15:04:37 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.12/openliberty-kernel-23.0.0.12.zip LIBERTY_SHA=f8b7fb58f928ba135e01fedf18d37b0de9848ccc LIBERTY_VERSION=23.0.0.12 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Wed, 17 Jan 2024 15:04:38 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 17 Jan 2024 15:04:38 GMT
USER 1001
# Wed, 17 Jan 2024 15:04:38 GMT
EXPOSE 9080 9443
# Wed, 17 Jan 2024 15:04:38 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 17 Jan 2024 15:04:38 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:bc8daefb9978b7f23cfc73ae68e998e85ee72a68588997321b1697cb0b9926df`  
		Last Modified: Thu, 11 Jan 2024 22:46:38 GMT  
		Size: 28.4 MB (28399616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d5742c9c31cbb7424e60c563307d1f6430ce374e15e840b77696a22c5a6727`  
		Last Modified: Wed, 17 Jan 2024 07:11:10 GMT  
		Size: 12.1 MB (12116817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf7839fb1f246e27342935163b2430c4971096cd222c33f1b81955e979c443a`  
		Last Modified: Wed, 17 Jan 2024 07:11:29 GMT  
		Size: 49.0 MB (49049474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5693e8d0fa49295ee1d86ca7b620d4c2c1c33dba701d9ac9e1ceb93a848c57e7`  
		Last Modified: Wed, 17 Jan 2024 07:11:25 GMT  
		Size: 4.1 MB (4056213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90db739bf899700335427e56b7bbd511dbeb7fe3a55f547abf5cb53c466bbf33`  
		Last Modified: Wed, 17 Jan 2024 15:15:08 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51bf966d5cb796f4de6b98219d14c3b0f835753c47876f41611312f231701ee9`  
		Last Modified: Wed, 17 Jan 2024 15:15:08 GMT  
		Size: 9.1 KB (9121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bc4d7355d7ca98a575523cb045a9a35a9934192c84eae5c95fcae99bc4bbf0`  
		Last Modified: Wed, 17 Jan 2024 15:15:08 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0deef2ea555044dd0101e330c8122b3e1a16c141dda424ef52c925f6dc17da`  
		Last Modified: Wed, 17 Jan 2024 15:15:06 GMT  
		Size: 42.3 KB (42321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d15eeda78bf5d2911a5e18b8974f117c07d64dfd8321aff1b7961fb6db42522`  
		Last Modified: Wed, 17 Jan 2024 15:15:07 GMT  
		Size: 14.3 MB (14253167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be3af001af5786b16d70a287640551b6535ce64a4ef95c3d58f172c5cca70ed`  
		Last Modified: Wed, 17 Jan 2024 15:15:06 GMT  
		Size: 864.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b352cc09f1ee539c148efbd3bfb3105c366fafe1fb1f7fa63004a4b0ef8c02`  
		Last Modified: Wed, 17 Jan 2024 15:15:06 GMT  
		Size: 10.2 KB (10212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580adfe249d0cbd60c0f6888ddb4214360818b6917dbff133754172b4839a269`  
		Last Modified: Wed, 17 Jan 2024 15:15:06 GMT  
		Size: 2.6 MB (2589041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:kernel-slim` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:240e97221fd111f71c6fc678cc96499f9df6856f27272d5d5b925eb3c2e75808
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119583678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f34c8051d228a7c92a5269fa8fbccb91ce316ee7dea9836553a926b81e228d`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 11 Jan 2024 17:10:02 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:10:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:10:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:10:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:10:06 GMT
ADD file:4da6fb9ba29da03fa46ed73abfae01fa7c87f2c26044ee297c88359085392aef in / 
# Thu, 11 Jan 2024 17:10:06 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 08:11:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 08:12:37 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:12:39 GMT
ENV JAVA_VERSION=jdk8u392-b08_openj9-0.41.0
# Wed, 17 Jan 2024 08:13:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='17df56bf2567bcca36d78ac4e46d025aec2553ba4df0b18c89464fcfebf9bb21';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_aarch64_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='3991f050a560a6ef21c1f3e08ce84302c4d41b923502667c23dac21e82706a0c';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_ppc64le_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        amd64|x86_64)          ESUM='2e771721212f403dd97a132ddcd20b4ed2d0ee95d504c299517a8ce58590690e';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_x64_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        s390x)          ESUM='5108b16f79176b501d9b5e5950bb143ffcf839da6472940bb62279db529e2630';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_s390x_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 17 Jan 2024 08:13:57 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 08:13:58 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 17 Jan 2024 08:14:32 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3f022ec8552bce1b72eb85d0778c93052ccb00226de3302544ec844ab93a9991e19c2db56ed06c18f03e5d75f34a46cedac46ae83bdd225518a55c62fc69ea04";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.83/bin/apache-tomcat-9.0.83.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 17 Jan 2024 10:56:23 GMT
USER root
# Wed, 17 Jan 2024 11:00:51 GMT
ARG LIBERTY_VERSION=23.0.0.12
# Wed, 17 Jan 2024 11:00:51 GMT
ARG LIBERTY_SHA=f8b7fb58f928ba135e01fedf18d37b0de9848ccc
# Wed, 17 Jan 2024 11:00:52 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.12/openliberty-kernel-23.0.0.12.zip
# Wed, 17 Jan 2024 11:00:52 GMT
ARG LIBERTY_BUILD_LABEL=cl231220231127-1901
# Wed, 17 Jan 2024 11:00:52 GMT
ARG OPENJ9_SCC=true
# Wed, 17 Jan 2024 11:00:53 GMT
ARG VERBOSE=false
# Wed, 17 Jan 2024 11:00:53 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl231220231127-1901 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=23.0.0.12
# Wed, 17 Jan 2024 11:00:54 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Wed, 17 Jan 2024 11:00:54 GMT
COPY dir:97cf6279dcb954616dcf6e80b110334a500f1803178f9fea6d45ccc032b92466 in /opt/ol/helpers 
# Wed, 17 Jan 2024 11:00:54 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Wed, 17 Jan 2024 11:00:56 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.12/openliberty-kernel-23.0.0.12.zip LIBERTY_SHA=f8b7fb58f928ba135e01fedf18d37b0de9848ccc LIBERTY_VERSION=23.0.0.12 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Wed, 17 Jan 2024 11:01:09 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.12/openliberty-kernel-23.0.0.12.zip LIBERTY_SHA=f8b7fb58f928ba135e01fedf18d37b0de9848ccc LIBERTY_VERSION=23.0.0.12 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Wed, 17 Jan 2024 11:01:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 17 Jan 2024 11:01:11 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.12/openliberty-kernel-23.0.0.12.zip LIBERTY_SHA=f8b7fb58f928ba135e01fedf18d37b0de9848ccc LIBERTY_VERSION=23.0.0.12 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Wed, 17 Jan 2024 11:01:13 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.12/openliberty-kernel-23.0.0.12.zip LIBERTY_SHA=f8b7fb58f928ba135e01fedf18d37b0de9848ccc LIBERTY_VERSION=23.0.0.12 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Wed, 17 Jan 2024 11:01:19 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.12/openliberty-kernel-23.0.0.12.zip LIBERTY_SHA=f8b7fb58f928ba135e01fedf18d37b0de9848ccc LIBERTY_VERSION=23.0.0.12 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Wed, 17 Jan 2024 11:01:19 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 17 Jan 2024 11:01:20 GMT
USER 1001
# Wed, 17 Jan 2024 11:01:20 GMT
EXPOSE 9080 9443
# Wed, 17 Jan 2024 11:01:20 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 17 Jan 2024 11:01:21 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:898e4a5fe680690395e7fd9d920dfa248b7508ec0573741c491bf250179ddbda`  
		Last Modified: Wed, 17 Jan 2024 05:26:53 GMT  
		Size: 35.7 MB (35657152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65667c00b5fcfd11e7e44a89f1b0e57aad8c84c14d66d24807227d6ff9bf00da`  
		Last Modified: Wed, 17 Jan 2024 08:21:10 GMT  
		Size: 12.9 MB (12893691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ea5ca7e18bbe097c134154ed478547e50e6a577f40e3345e812fcf5e9435af`  
		Last Modified: Wed, 17 Jan 2024 08:21:37 GMT  
		Size: 50.7 MB (50680402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38a41c8d3c0b1a5cf4d056045a9a405bad8c38fec29f533a796c0cf0c354f9f`  
		Last Modified: Wed, 17 Jan 2024 08:21:31 GMT  
		Size: 3.5 MB (3527188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117b04e39c828bc890de2779ee256cfe5c578b7894c65ee4e2a63ed170e26883`  
		Last Modified: Wed, 17 Jan 2024 11:16:39 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a651bd3a6cb42196543419181f555e1007efc3b15eac040c336b37d301e39d`  
		Last Modified: Wed, 17 Jan 2024 11:16:39 GMT  
		Size: 9.1 KB (9128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9fa224b31e958aca8a2e7195d806b978f863df7bed0d5ba81606af73acac74b`  
		Last Modified: Wed, 17 Jan 2024 11:16:39 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3696db4511da15058653b71cebd6d2b66a5d4d859c0eb82edc42e2fbf811fc`  
		Last Modified: Wed, 17 Jan 2024 11:16:37 GMT  
		Size: 36.5 KB (36501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be8f509258f7960510b09cb4d82efcccc8f7c71dccbbafccb6bead4ca2524ee`  
		Last Modified: Wed, 17 Jan 2024 11:16:39 GMT  
		Size: 14.3 MB (14253566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3fd10bd1e2aed1452223a6401b2139fe1ddf8c84997314c2a20fe9e18d83e59`  
		Last Modified: Wed, 17 Jan 2024 11:16:37 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f9547740932cf0971abaeee002cff1df3b319d2088af430870d2d7d4c26766`  
		Last Modified: Wed, 17 Jan 2024 11:16:37 GMT  
		Size: 10.2 KB (10217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40783e994aec038e701b08f5156f89a58454c77f64250cc8abd541a9fd65065b`  
		Last Modified: Wed, 17 Jan 2024 11:16:38 GMT  
		Size: 2.5 MB (2513627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:kernel-slim` - linux; s390x

```console
$ docker pull open-liberty@sha256:4712e3c3a8db1837c4c46287d8a7df7709ae6af465088b8a3ab549dd0201041d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112191030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0760f206be4ca5104a51899c1f9a2c08a60e2448bf9f59f6c790c3c6ac227ba`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 11 Jan 2024 17:12:07 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:12:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:12:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:12:07 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:12:10 GMT
ADD file:5ae109128826d2e7660949ed9ff9af4b92bbade5ce06a7011ab7b15bb21d8b75 in / 
# Thu, 11 Jan 2024 17:12:10 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 11:27:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 11:27:58 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 11:27:59 GMT
ENV JAVA_VERSION=jdk8u392-b08_openj9-0.41.0
# Wed, 17 Jan 2024 11:31:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='17df56bf2567bcca36d78ac4e46d025aec2553ba4df0b18c89464fcfebf9bb21';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_aarch64_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='3991f050a560a6ef21c1f3e08ce84302c4d41b923502667c23dac21e82706a0c';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_ppc64le_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        amd64|x86_64)          ESUM='2e771721212f403dd97a132ddcd20b4ed2d0ee95d504c299517a8ce58590690e';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_x64_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        s390x)          ESUM='5108b16f79176b501d9b5e5950bb143ffcf839da6472940bb62279db529e2630';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_s390x_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 17 Jan 2024 11:31:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 11:31:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 17 Jan 2024 11:32:05 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3f022ec8552bce1b72eb85d0778c93052ccb00226de3302544ec844ab93a9991e19c2db56ed06c18f03e5d75f34a46cedac46ae83bdd225518a55c62fc69ea04";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.83/bin/apache-tomcat-9.0.83.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 17 Jan 2024 19:40:50 GMT
USER root
# Wed, 17 Jan 2024 19:47:18 GMT
ARG LIBERTY_VERSION=23.0.0.12
# Wed, 17 Jan 2024 19:47:18 GMT
ARG LIBERTY_SHA=f8b7fb58f928ba135e01fedf18d37b0de9848ccc
# Wed, 17 Jan 2024 19:47:18 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.12/openliberty-kernel-23.0.0.12.zip
# Wed, 17 Jan 2024 19:47:19 GMT
ARG LIBERTY_BUILD_LABEL=cl231220231127-1901
# Wed, 17 Jan 2024 19:47:19 GMT
ARG OPENJ9_SCC=true
# Wed, 17 Jan 2024 19:47:19 GMT
ARG VERBOSE=false
# Wed, 17 Jan 2024 19:47:19 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl231220231127-1901 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=23.0.0.12
# Wed, 17 Jan 2024 19:47:19 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Wed, 17 Jan 2024 19:47:19 GMT
COPY dir:97cf6279dcb954616dcf6e80b110334a500f1803178f9fea6d45ccc032b92466 in /opt/ol/helpers 
# Wed, 17 Jan 2024 19:47:19 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Wed, 17 Jan 2024 19:47:20 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.12/openliberty-kernel-23.0.0.12.zip LIBERTY_SHA=f8b7fb58f928ba135e01fedf18d37b0de9848ccc LIBERTY_VERSION=23.0.0.12 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Wed, 17 Jan 2024 19:47:26 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.12/openliberty-kernel-23.0.0.12.zip LIBERTY_SHA=f8b7fb58f928ba135e01fedf18d37b0de9848ccc LIBERTY_VERSION=23.0.0.12 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Wed, 17 Jan 2024 19:47:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 17 Jan 2024 19:47:27 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.12/openliberty-kernel-23.0.0.12.zip LIBERTY_SHA=f8b7fb58f928ba135e01fedf18d37b0de9848ccc LIBERTY_VERSION=23.0.0.12 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Wed, 17 Jan 2024 19:47:27 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.12/openliberty-kernel-23.0.0.12.zip LIBERTY_SHA=f8b7fb58f928ba135e01fedf18d37b0de9848ccc LIBERTY_VERSION=23.0.0.12 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Wed, 17 Jan 2024 19:47:30 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231220231127-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.12/openliberty-kernel-23.0.0.12.zip LIBERTY_SHA=f8b7fb58f928ba135e01fedf18d37b0de9848ccc LIBERTY_VERSION=23.0.0.12 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Wed, 17 Jan 2024 19:47:31 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 17 Jan 2024 19:47:31 GMT
USER 1001
# Wed, 17 Jan 2024 19:47:31 GMT
EXPOSE 9080 9443
# Wed, 17 Jan 2024 19:47:31 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 17 Jan 2024 19:47:31 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:9767f83c892c3413514216ee1180f4118e77f689d61466a79134bd214cf66520`  
		Last Modified: Wed, 17 Jan 2024 10:37:33 GMT  
		Size: 28.7 MB (28654354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05963aa390a549a6395f30929c3e4c93c525db396700855c78d7eb451737f196`  
		Last Modified: Wed, 17 Jan 2024 11:58:09 GMT  
		Size: 12.2 MB (12206009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408cbbdd2520b72026d5bd389d4da2c873e9d4a9c4a96bc9c6f17c53df705e7a`  
		Last Modified: Wed, 17 Jan 2024 11:58:51 GMT  
		Size: 50.1 MB (50084217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf5f9477fe3a2081acb099cef7caa4925edb59b68d2224fc96776e610d5b482e`  
		Last Modified: Wed, 17 Jan 2024 11:58:43 GMT  
		Size: 4.3 MB (4309137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1052f956035966ad866292d9cd31f2e3656fead2fc019179b02d3c8aa9836b`  
		Last Modified: Wed, 17 Jan 2024 20:21:37 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c79032874042691146cce9adc6a333fae335b05d0b3fffdd26a8cae32f14138`  
		Last Modified: Wed, 17 Jan 2024 20:21:37 GMT  
		Size: 9.1 KB (9128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:105e04802f79ec8e4411823cfcf5645f9ad02fc33367862d7173746abb8ec723`  
		Last Modified: Wed, 17 Jan 2024 20:21:37 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7af77eefe0a190bc2002b0d465a0cf7798c36125d0189bc17fd014ee80307d8`  
		Last Modified: Wed, 17 Jan 2024 20:21:36 GMT  
		Size: 33.1 KB (33114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dfa3cace2ace2b0df2e7f5bb86e91d9892c416f5b9b7b52083866a7d64bb530`  
		Last Modified: Wed, 17 Jan 2024 20:21:37 GMT  
		Size: 14.3 MB (14253069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b14856dcd11c316358b71bfe06e569a6ba191c36ef2df8f18d3b957dc651237`  
		Last Modified: Wed, 17 Jan 2024 20:21:36 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85728c02042462316d0f6687aa3e2d096438d2b1e310b96a336d315f187e476c`  
		Last Modified: Wed, 17 Jan 2024 20:21:36 GMT  
		Size: 10.2 KB (10215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d53c3983da75b28d34530dea42e0d0e00e9fbb3969ae21e3ef73ab42f83046`  
		Last Modified: Wed, 17 Jan 2024 20:21:36 GMT  
		Size: 2.6 MB (2629580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
