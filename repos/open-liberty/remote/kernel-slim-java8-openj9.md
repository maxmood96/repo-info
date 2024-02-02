## `open-liberty:kernel-slim-java8-openj9`

```console
$ docker pull open-liberty@sha256:041ff5425d8f56ababd190e1cf594faff4e8dd1c60ed0c1ed8cc2a489f8c590d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `open-liberty:kernel-slim-java8-openj9` - linux; amd64

```console
$ docker pull open-liberty@sha256:48d06e2246759a347d7567d24af6b9582ae6da6b67521c2d787aae00e478ccf1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.4 MB (114389258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21277669044d78931c10d2240987ec4f841686035eff1aa7ba2325cb3e820c86`
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
# Tue, 30 Jan 2024 23:40:36 GMT
ARG LIBERTY_VERSION=24.0.0.1
# Tue, 30 Jan 2024 23:40:36 GMT
ARG LIBERTY_SHA=2ad434d83ac0998ecfcbd3b5583888ba936e6be2
# Tue, 30 Jan 2024 23:40:36 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.1/openliberty-kernel-24.0.0.1.zip
# Tue, 30 Jan 2024 23:40:36 GMT
ARG LIBERTY_BUILD_LABEL=cl240120240115-2042
# Tue, 30 Jan 2024 23:40:37 GMT
ARG OPENJ9_SCC=true
# Tue, 30 Jan 2024 23:40:37 GMT
ARG VERBOSE=false
# Tue, 30 Jan 2024 23:40:37 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240120240115-2042 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=24.0.0.1
# Tue, 30 Jan 2024 23:40:37 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Tue, 30 Jan 2024 23:40:37 GMT
COPY dir:21b3941757f3951d4136d43e6fb19dfa2e72ecb2c9af6886872e3a0ef83269e7 in /opt/ol/helpers 
# Tue, 30 Jan 2024 23:40:37 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Tue, 30 Jan 2024 23:40:38 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.1/openliberty-kernel-24.0.0.1.zip LIBERTY_SHA=2ad434d83ac0998ecfcbd3b5583888ba936e6be2 LIBERTY_VERSION=24.0.0.1 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Tue, 30 Jan 2024 23:40:46 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.1/openliberty-kernel-24.0.0.1.zip LIBERTY_SHA=2ad434d83ac0998ecfcbd3b5583888ba936e6be2 LIBERTY_VERSION=24.0.0.1 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Tue, 30 Jan 2024 23:40:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 30 Jan 2024 23:40:47 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.1/openliberty-kernel-24.0.0.1.zip LIBERTY_SHA=2ad434d83ac0998ecfcbd3b5583888ba936e6be2 LIBERTY_VERSION=24.0.0.1 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Tue, 30 Jan 2024 23:40:48 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.1/openliberty-kernel-24.0.0.1.zip LIBERTY_SHA=2ad434d83ac0998ecfcbd3b5583888ba936e6be2 LIBERTY_VERSION=24.0.0.1 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Tue, 30 Jan 2024 23:40:53 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.1/openliberty-kernel-24.0.0.1.zip LIBERTY_SHA=2ad434d83ac0998ecfcbd3b5583888ba936e6be2 LIBERTY_VERSION=24.0.0.1 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Tue, 30 Jan 2024 23:40:53 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 30 Jan 2024 23:40:53 GMT
USER 1001
# Tue, 30 Jan 2024 23:40:53 GMT
EXPOSE 9080 9443
# Tue, 30 Jan 2024 23:40:53 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 30 Jan 2024 23:40:53 GMT
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
	-	`sha256:dd7a7962ea51ada5411601e693324576af4136440554f0f2b0103d6e8f373ce2`  
		Last Modified: Tue, 30 Jan 2024 23:46:59 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671004c55d6557d57a39e8c8e74045aeb04f9499e55c70b77a89ff645754cb4d`  
		Last Modified: Tue, 30 Jan 2024 23:46:59 GMT  
		Size: 9.2 KB (9190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf74acb17cba84c16e7cfa118f121adefc89358518e0a750858e499d542a2d1`  
		Last Modified: Tue, 30 Jan 2024 23:46:59 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0d0247a67d4980292f913e52802d8492f02b058f99555972838135a29e2bdb`  
		Last Modified: Tue, 30 Jan 2024 23:46:57 GMT  
		Size: 31.7 KB (31749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2d5491c6b7b73c06eeb42d4c300c27367c62ef3e108e9569e096273007d0bd`  
		Last Modified: Tue, 30 Jan 2024 23:46:58 GMT  
		Size: 14.7 MB (14658100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5db54d9d0f4739d789c08f425f7aa4e73273e22f510415f8315101710199882`  
		Last Modified: Tue, 30 Jan 2024 23:46:57 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf6a24339bcb16cde87f9f82bf682aa3d6fcbe677522cf1bbfa01aebc456704`  
		Last Modified: Tue, 30 Jan 2024 23:46:57 GMT  
		Size: 10.3 KB (10275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e63c8f4300b1650d7cdc9d184ea3580e2471472e80cb0219ee3239a8f29932`  
		Last Modified: Tue, 30 Jan 2024 23:46:57 GMT  
		Size: 2.6 MB (2643175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:kernel-slim-java8-openj9` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:9bd8585852f69cafd9ec678de0f908844cd1c37191b506ba09505f805b4cf03f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.9 MB (110936214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc62961a84bd77cef5ccd57ad03519a71c1da4cfdf0d0effcd30a525998c5b11`
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
# Wed, 31 Jan 2024 00:08:35 GMT
ARG LIBERTY_VERSION=24.0.0.1
# Wed, 31 Jan 2024 00:08:35 GMT
ARG LIBERTY_SHA=2ad434d83ac0998ecfcbd3b5583888ba936e6be2
# Wed, 31 Jan 2024 00:08:35 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.1/openliberty-kernel-24.0.0.1.zip
# Wed, 31 Jan 2024 00:08:35 GMT
ARG LIBERTY_BUILD_LABEL=cl240120240115-2042
# Wed, 31 Jan 2024 00:08:35 GMT
ARG OPENJ9_SCC=true
# Wed, 31 Jan 2024 00:08:35 GMT
ARG VERBOSE=false
# Wed, 31 Jan 2024 00:08:35 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240120240115-2042 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=24.0.0.1
# Wed, 31 Jan 2024 00:08:36 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Wed, 31 Jan 2024 00:08:36 GMT
COPY dir:21b3941757f3951d4136d43e6fb19dfa2e72ecb2c9af6886872e3a0ef83269e7 in /opt/ol/helpers 
# Wed, 31 Jan 2024 00:08:36 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Wed, 31 Jan 2024 00:08:37 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.1/openliberty-kernel-24.0.0.1.zip LIBERTY_SHA=2ad434d83ac0998ecfcbd3b5583888ba936e6be2 LIBERTY_VERSION=24.0.0.1 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Wed, 31 Jan 2024 00:08:43 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.1/openliberty-kernel-24.0.0.1.zip LIBERTY_SHA=2ad434d83ac0998ecfcbd3b5583888ba936e6be2 LIBERTY_VERSION=24.0.0.1 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Wed, 31 Jan 2024 00:08:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 31 Jan 2024 00:08:44 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.1/openliberty-kernel-24.0.0.1.zip LIBERTY_SHA=2ad434d83ac0998ecfcbd3b5583888ba936e6be2 LIBERTY_VERSION=24.0.0.1 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Wed, 31 Jan 2024 00:08:44 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.1/openliberty-kernel-24.0.0.1.zip LIBERTY_SHA=2ad434d83ac0998ecfcbd3b5583888ba936e6be2 LIBERTY_VERSION=24.0.0.1 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Wed, 31 Jan 2024 00:08:48 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.1/openliberty-kernel-24.0.0.1.zip LIBERTY_SHA=2ad434d83ac0998ecfcbd3b5583888ba936e6be2 LIBERTY_VERSION=24.0.0.1 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Wed, 31 Jan 2024 00:08:48 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 31 Jan 2024 00:08:48 GMT
USER 1001
# Wed, 31 Jan 2024 00:08:48 GMT
EXPOSE 9080 9443
# Wed, 31 Jan 2024 00:08:48 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 31 Jan 2024 00:08:48 GMT
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
	-	`sha256:41a1512da8549452d88ac2f5b41212a3ce8c8337d8d8508b470e2c0ae320cbd6`  
		Last Modified: Wed, 31 Jan 2024 00:14:02 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9db9520b9ae042dfd91e9d24151f1852f18bfcbd257c19cccd2cb352accb833`  
		Last Modified: Wed, 31 Jan 2024 00:14:02 GMT  
		Size: 9.2 KB (9189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d7a9b589a2b297b3607a098021ddc7bfc18bec6a176690ebc1dd73e139cd6c`  
		Last Modified: Wed, 31 Jan 2024 00:14:01 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f98d298870d4fbc5a37e97b3903288adfdc65d1ae50f9cd7d7b1d665403b9cad`  
		Last Modified: Wed, 31 Jan 2024 00:14:00 GMT  
		Size: 42.3 KB (42321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce71ae70e1cfbe214e52961c2b8a980fcd29d4d3bda0dc93b4d37ec3b622ff4`  
		Last Modified: Wed, 31 Jan 2024 00:14:00 GMT  
		Size: 14.6 MB (14633884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d4f89c92f5725296e831c9ad468622ea8a158fa7798bd26cb03426902eb6f6`  
		Last Modified: Wed, 31 Jan 2024 00:13:59 GMT  
		Size: 864.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5d46c277ef8f9cb4e1e19239d5ae772ba92a81c4e2edcdb333cd68442d6214`  
		Last Modified: Wed, 31 Jan 2024 00:13:59 GMT  
		Size: 10.3 KB (10273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6015e2a9ae280d5e71bfe4837a8b5b9cb44a3a8dde0b641f0742a85f575572f7`  
		Last Modified: Wed, 31 Jan 2024 00:14:00 GMT  
		Size: 2.6 MB (2616222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:kernel-slim-java8-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:5cb66ca1263303b8a99cfeac6be058ec9bc6e51ffc10f3cb3517751774bf271b
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119588121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28feb77300d36a1dfb684c1be826816d707a3607ce27be86ea8ba2e12d42498e`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 25 Jan 2024 17:56:59 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:56:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:57:02 GMT
ADD file:516de9c24f8fb95b9521e039ca0709347304eaf18821af0546eb4f3e9da81a19 in / 
# Thu, 25 Jan 2024 17:57:02 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:28:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 01:29:17 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:29:19 GMT
ENV JAVA_VERSION=jdk8u392-b08_openj9-0.41.0
# Fri, 02 Feb 2024 01:31:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='17df56bf2567bcca36d78ac4e46d025aec2553ba4df0b18c89464fcfebf9bb21';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_aarch64_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='3991f050a560a6ef21c1f3e08ce84302c4d41b923502667c23dac21e82706a0c';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_ppc64le_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        amd64|x86_64)          ESUM='2e771721212f403dd97a132ddcd20b4ed2d0ee95d504c299517a8ce58590690e';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_x64_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        s390x)          ESUM='5108b16f79176b501d9b5e5950bb143ffcf839da6472940bb62279db529e2630';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_s390x_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 02 Feb 2024 01:31:26 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 01:31:27 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 02 Feb 2024 01:32:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3f022ec8552bce1b72eb85d0778c93052ccb00226de3302544ec844ab93a9991e19c2db56ed06c18f03e5d75f34a46cedac46ae83bdd225518a55c62fc69ea04";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.83/bin/apache-tomcat-9.0.83.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 02 Feb 2024 05:41:55 GMT
USER root
# Fri, 02 Feb 2024 05:47:09 GMT
ARG LIBERTY_VERSION=24.0.0.1
# Fri, 02 Feb 2024 05:47:10 GMT
ARG LIBERTY_SHA=2ad434d83ac0998ecfcbd3b5583888ba936e6be2
# Fri, 02 Feb 2024 05:47:11 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.1/openliberty-kernel-24.0.0.1.zip
# Fri, 02 Feb 2024 05:47:12 GMT
ARG LIBERTY_BUILD_LABEL=cl240120240115-2042
# Fri, 02 Feb 2024 05:47:13 GMT
ARG OPENJ9_SCC=true
# Fri, 02 Feb 2024 05:47:14 GMT
ARG VERBOSE=false
# Fri, 02 Feb 2024 05:47:15 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240120240115-2042 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=24.0.0.1
# Fri, 02 Feb 2024 05:47:15 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Fri, 02 Feb 2024 05:47:16 GMT
COPY dir:21b3941757f3951d4136d43e6fb19dfa2e72ecb2c9af6886872e3a0ef83269e7 in /opt/ol/helpers 
# Fri, 02 Feb 2024 05:47:16 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Fri, 02 Feb 2024 05:47:19 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.1/openliberty-kernel-24.0.0.1.zip LIBERTY_SHA=2ad434d83ac0998ecfcbd3b5583888ba936e6be2 LIBERTY_VERSION=24.0.0.1 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Fri, 02 Feb 2024 05:47:34 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.1/openliberty-kernel-24.0.0.1.zip LIBERTY_SHA=2ad434d83ac0998ecfcbd3b5583888ba936e6be2 LIBERTY_VERSION=24.0.0.1 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Fri, 02 Feb 2024 05:47:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 02 Feb 2024 05:47:38 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.1/openliberty-kernel-24.0.0.1.zip LIBERTY_SHA=2ad434d83ac0998ecfcbd3b5583888ba936e6be2 LIBERTY_VERSION=24.0.0.1 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Fri, 02 Feb 2024 05:47:40 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.1/openliberty-kernel-24.0.0.1.zip LIBERTY_SHA=2ad434d83ac0998ecfcbd3b5583888ba936e6be2 LIBERTY_VERSION=24.0.0.1 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Fri, 02 Feb 2024 05:47:48 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.1/openliberty-kernel-24.0.0.1.zip LIBERTY_SHA=2ad434d83ac0998ecfcbd3b5583888ba936e6be2 LIBERTY_VERSION=24.0.0.1 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Fri, 02 Feb 2024 05:47:49 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 02 Feb 2024 05:47:49 GMT
USER 1001
# Fri, 02 Feb 2024 05:47:50 GMT
EXPOSE 9080 9443
# Fri, 02 Feb 2024 05:47:52 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 02 Feb 2024 05:47:53 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:4cddbbaaed5c0bb0075d1b49c5185496b73a0103b0d818f916036e28a6cb5f81`  
		Last Modified: Fri, 02 Feb 2024 00:09:07 GMT  
		Size: 35.7 MB (35659183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffafe232c1276a1c12d986c5714733656083b095badd2eb2ccf3cf0e9fa72c0`  
		Last Modified: Fri, 02 Feb 2024 01:44:53 GMT  
		Size: 12.9 MB (12893849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14509c958760f7c8009dbadd8160ce5a2441977f5dec4baf5771d78c9f2794e1`  
		Last Modified: Fri, 02 Feb 2024 01:45:47 GMT  
		Size: 50.7 MB (50680410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2824e0a6f2bf19d5781dfa886f3ad7a9951441ca58c4dc36ab262ec568e767`  
		Last Modified: Fri, 02 Feb 2024 01:45:41 GMT  
		Size: 3.5 MB (3535121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267c8c903a54d53557aebe57497295fc7afe3b2226ca58619c56f15c44a0e8d7`  
		Last Modified: Fri, 02 Feb 2024 06:17:59 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773b831903b7c38d81197af902d082ee2f5870dbecf93f8a586e5750dcd35266`  
		Last Modified: Fri, 02 Feb 2024 06:17:59 GMT  
		Size: 9.2 KB (9189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a594bd92fb4a751954f06e22fcfa4c7e66cb46825a1bdc3bd4279facf39f575c`  
		Last Modified: Fri, 02 Feb 2024 06:17:59 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468002cd8518be4039a1926af8fac61c4412245bee6296089a1ba8e9ee1928fb`  
		Last Modified: Fri, 02 Feb 2024 06:17:56 GMT  
		Size: 36.5 KB (36494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5386ef0452b7a521cbc2015cd1c4e4b371ea56ada20559d6dc2767e264a67c`  
		Last Modified: Fri, 02 Feb 2024 06:17:58 GMT  
		Size: 14.3 MB (14254978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8515eb68aea3e8ffc25d07faab5ea25659bf566caddbb18a8ce7c39ab975b28b`  
		Last Modified: Fri, 02 Feb 2024 06:17:56 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7e98db238ff727f29e62ea1836e8d399b6584ab25bf93b81d9cc481ee07fa5`  
		Last Modified: Fri, 02 Feb 2024 06:17:56 GMT  
		Size: 10.3 KB (10297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c63c475baa4cd30ec7aa3c4884955cf4da6677350b7e883e69f9e00616c4a6`  
		Last Modified: Fri, 02 Feb 2024 06:17:57 GMT  
		Size: 2.5 MB (2506390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:kernel-slim-java8-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:537f303f856b944f8d9aed0c18c03adbddb89592156951be8c3b83749655f853
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112587373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:198516e1169e3923fe2f88e9214b48fa0aef437c4bb469d7590ffc73b67b0959`
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
# Wed, 31 Jan 2024 02:14:14 GMT
ARG LIBERTY_VERSION=24.0.0.1
# Wed, 31 Jan 2024 02:14:14 GMT
ARG LIBERTY_SHA=2ad434d83ac0998ecfcbd3b5583888ba936e6be2
# Wed, 31 Jan 2024 02:14:14 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.1/openliberty-kernel-24.0.0.1.zip
# Wed, 31 Jan 2024 02:14:14 GMT
ARG LIBERTY_BUILD_LABEL=cl240120240115-2042
# Wed, 31 Jan 2024 02:14:14 GMT
ARG OPENJ9_SCC=true
# Wed, 31 Jan 2024 02:14:14 GMT
ARG VERBOSE=false
# Wed, 31 Jan 2024 02:14:15 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240120240115-2042 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=24.0.0.1
# Wed, 31 Jan 2024 02:14:15 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Wed, 31 Jan 2024 02:14:15 GMT
COPY dir:21b3941757f3951d4136d43e6fb19dfa2e72ecb2c9af6886872e3a0ef83269e7 in /opt/ol/helpers 
# Wed, 31 Jan 2024 02:14:15 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Wed, 31 Jan 2024 02:14:16 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.1/openliberty-kernel-24.0.0.1.zip LIBERTY_SHA=2ad434d83ac0998ecfcbd3b5583888ba936e6be2 LIBERTY_VERSION=24.0.0.1 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Wed, 31 Jan 2024 02:14:22 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.1/openliberty-kernel-24.0.0.1.zip LIBERTY_SHA=2ad434d83ac0998ecfcbd3b5583888ba936e6be2 LIBERTY_VERSION=24.0.0.1 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Wed, 31 Jan 2024 02:14:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 31 Jan 2024 02:14:23 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.1/openliberty-kernel-24.0.0.1.zip LIBERTY_SHA=2ad434d83ac0998ecfcbd3b5583888ba936e6be2 LIBERTY_VERSION=24.0.0.1 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Wed, 31 Jan 2024 02:14:23 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.1/openliberty-kernel-24.0.0.1.zip LIBERTY_SHA=2ad434d83ac0998ecfcbd3b5583888ba936e6be2 LIBERTY_VERSION=24.0.0.1 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Wed, 31 Jan 2024 02:14:27 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/24.0.0.1/openliberty-kernel-24.0.0.1.zip LIBERTY_SHA=2ad434d83ac0998ecfcbd3b5583888ba936e6be2 LIBERTY_VERSION=24.0.0.1 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Wed, 31 Jan 2024 02:14:27 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 31 Jan 2024 02:14:27 GMT
USER 1001
# Wed, 31 Jan 2024 02:14:27 GMT
EXPOSE 9080 9443
# Wed, 31 Jan 2024 02:14:27 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 31 Jan 2024 02:14:27 GMT
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
	-	`sha256:046a9f7337c7a0d56a14ab32cf62a4a388cadaab39dd767e48056cb96ee40f01`  
		Last Modified: Wed, 31 Jan 2024 02:48:31 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc39f45f08c437c406f14a21ff7c3f0e007182576d9c258abb3f3e9decc02962`  
		Last Modified: Wed, 31 Jan 2024 02:48:31 GMT  
		Size: 9.2 KB (9189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f394960339bf6772a5ad5d5118568e4814fa729ac849a3715f9eb5768acd700e`  
		Last Modified: Wed, 31 Jan 2024 02:48:30 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52c9fb9e919217ec02326c81ca9def2f3839e865d8f3771e6205c3b51086262`  
		Last Modified: Wed, 31 Jan 2024 02:48:29 GMT  
		Size: 33.1 KB (33116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a16f219bbcbdcb5051beb0d197861315a49c00e24839a5bf47eae688f845ae`  
		Last Modified: Wed, 31 Jan 2024 02:48:30 GMT  
		Size: 14.7 MB (14659634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2a0f244422ee440696c480cb68fcbda754150f565f0571b295c1774d4ab8fb`  
		Last Modified: Wed, 31 Jan 2024 02:48:29 GMT  
		Size: 864.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855926e4dfb5c02cd81d07360957d188dfffc1ae7c64b01ce8b734b183796566`  
		Last Modified: Wed, 31 Jan 2024 02:48:29 GMT  
		Size: 10.3 KB (10275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89600eed4446b12c1e30718c7553d73fa747b7c291d2bce6af1b6eb26428718f`  
		Last Modified: Wed, 31 Jan 2024 02:48:29 GMT  
		Size: 2.6 MB (2619237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
