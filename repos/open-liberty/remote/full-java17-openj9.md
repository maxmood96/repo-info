## `open-liberty:full-java17-openj9`

```console
$ docker pull open-liberty@sha256:3d1678714e8d05e103a1d84f508b161facfef9348f7c1dfc8fb641ac2e8d798d
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

### `open-liberty:full-java17-openj9` - linux; amd64

```console
$ docker pull open-liberty@sha256:5c66cecd031a6791d065b019e2d7f686f8c30158a792cd8f3640f73787485d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.1 MB (442134008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3ff70f632a2f2bbb1bba4c40a03e729a61d52c53216544298fbe5ca35babdd`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:35:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 05 Jun 2024 07:35:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 07:41:40 GMT
ENV JAVA_VERSION=jdk-17.0.11+9_openj9-0.44.0
# Wed, 05 Jun 2024 07:43:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6764398cdbcf824f2b99c095d58efb69b140d0c9824239560d58478f67bc15b';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='12a951e5353f4bccae5430de05a7204b6e1ad983780d3ecccacd2179936cc9ee';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='a47d3fabdf14c0f56561e5be24d689007f42cb079af0c89db235a58899fd4ab3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='049c6d6db4ba22fdfc7aaef3ee0af1bed1b71bda314b5c9ab27451d2c7392c1c';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 05 Jun 2024 07:43:17 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jun 2024 07:43:17 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 05 Jun 2024 07:43:50 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Tue, 18 Jun 2024 19:00:56 GMT
USER root
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_VERSION=24.0.0.6
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_BUILD_LABEL=cl240620240603-2001
# Tue, 18 Jun 2024 19:00:56 GMT
ARG OPENJ9_SCC=true
# Tue, 18 Jun 2024 19:00:56 GMT
ARG VERBOSE=false
# Tue, 18 Jun 2024 19:00:56 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240620240603-2001 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=24.0.0.6
# Tue, 18 Jun 2024 19:00:56 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 18 Jun 2024 19:00:56 GMT
USER 1001
# Tue, 18 Jun 2024 19:00:56 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 18 Jun 2024 19:00:56 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 18 Jun 2024 19:00:56 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1c42da6b1c9c8512a8f49f8b6a6f8d1819a2b9ef475ea78cd7ef2cfd5978bf`  
		Last Modified: Wed, 05 Jun 2024 07:51:11 GMT  
		Size: 12.2 MB (12156895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff35db90503df527195f46b01451d5cbd4a100468e5f0b166451194dc206e2c`  
		Last Modified: Wed, 05 Jun 2024 07:54:16 GMT  
		Size: 51.8 MB (51801719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9965b8c1e6ecaf90b8346e3ffc06b4e91b6ae9b26d4da0862ec680fc73ef133e`  
		Last Modified: Wed, 05 Jun 2024 07:54:10 GMT  
		Size: 4.9 MB (4911218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5e9ea56b18c4016285f2bed45f6fd5648ab52bfea5d8b8e4ad556ecf4bf943`  
		Last Modified: Fri, 21 Jun 2024 01:05:06 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454241339aad965744154605fb883c0394aeea303122d674cbd1227e75b0f741`  
		Last Modified: Fri, 21 Jun 2024 01:05:06 GMT  
		Size: 10.0 KB (9990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05dddfab4bfc3d8069fdb7ae9e8ffcfa2093797bcb2d47cc7bbf353dc7cf8980`  
		Last Modified: Fri, 21 Jun 2024 01:05:06 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e898519bff216fd41d9782be99c592610095a6a13bd86d0fa89ad0d5a7ca069f`  
		Last Modified: Fri, 21 Jun 2024 01:04:10 GMT  
		Size: 31.7 KB (31744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad03a09e627d0b4a52090e5fd52ca83387091b1291b82ec5a96639dde2466fa`  
		Last Modified: Fri, 21 Jun 2024 01:05:12 GMT  
		Size: 329.0 MB (328967621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c55ad75fe3859cc35ddc66b96e28e9954cf1daa3a418b67c3bfc64ddc451e6`  
		Last Modified: Fri, 21 Jun 2024 01:05:07 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6465939dcafe763674dc1afe2bcd4587f93a99c5c298aa17e833f5e429be805e`  
		Last Modified: Fri, 21 Jun 2024 01:05:07 GMT  
		Size: 11.3 KB (11348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812421c3b6e943090d11fbb9a949c03381bc78e1b43235409af108dcc9ed0e2b`  
		Last Modified: Fri, 21 Jun 2024 01:05:07 GMT  
		Size: 13.8 MB (13801843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:80cdad24fb583849fbd29f221f068154686a7cc9eec265868a05650101543b3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3956504a5e5079b024c13f63135436ce88f6a251863821cfeefa5413b758a31`

```dockerfile
```

-	Layers:
	-	`sha256:35d32d491dbbb29d27c15e379f796183878a8a3acffc1b8313ead9bf0529c1cc`  
		Last Modified: Fri, 21 Jun 2024 01:05:06 GMT  
		Size: 5.1 MB (5085125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e27c3f1f8c55fe8dd2f830f6454852a42d1d65e712c0f48c365bd42b50029e4`  
		Last Modified: Fri, 21 Jun 2024 01:05:06 GMT  
		Size: 38.6 KB (38610 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java17-openj9` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:c0adf2087fba935a0bb6dce40efbb93df798819d0831bb55bcd2a2a6a3d9d6fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.1 MB (435129001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49e252adf81fce86d300c4f34aff4d472ec627c5bf34cbc2ca19b7dcea3651e2`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 06:00:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 05 Jun 2024 06:01:22 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:07:20 GMT
ENV JAVA_VERSION=jdk-17.0.11+9_openj9-0.44.0
# Wed, 05 Jun 2024 06:08:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6764398cdbcf824f2b99c095d58efb69b140d0c9824239560d58478f67bc15b';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='12a951e5353f4bccae5430de05a7204b6e1ad983780d3ecccacd2179936cc9ee';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='a47d3fabdf14c0f56561e5be24d689007f42cb079af0c89db235a58899fd4ab3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='049c6d6db4ba22fdfc7aaef3ee0af1bed1b71bda314b5c9ab27451d2c7392c1c';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 05 Jun 2024 06:08:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jun 2024 06:08:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 05 Jun 2024 06:09:27 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Tue, 18 Jun 2024 19:00:56 GMT
USER root
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_VERSION=24.0.0.6
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_BUILD_LABEL=cl240620240603-2001
# Tue, 18 Jun 2024 19:00:56 GMT
ARG OPENJ9_SCC=true
# Tue, 18 Jun 2024 19:00:56 GMT
ARG VERBOSE=false
# Tue, 18 Jun 2024 19:00:56 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240620240603-2001 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=24.0.0.6
# Tue, 18 Jun 2024 19:00:56 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 18 Jun 2024 19:00:56 GMT
USER 1001
# Tue, 18 Jun 2024 19:00:56 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 18 Jun 2024 19:00:56 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 18 Jun 2024 19:00:56 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb8d6134690c858cfd9f9b81a6adb73767cdf8efe4e439360fbd094b85dde8c`  
		Last Modified: Wed, 05 Jun 2024 06:16:39 GMT  
		Size: 12.1 MB (12117024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb225ef883a0467ac72d839fe17fe830259fe2da1c5d1a9fcf30499db683f5b3`  
		Last Modified: Wed, 05 Jun 2024 06:19:21 GMT  
		Size: 47.8 MB (47819107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0524922904f72012ae23421700c598ef7d8964d30f2fb660d8e93814410ca3fd`  
		Last Modified: Wed, 05 Jun 2024 06:19:17 GMT  
		Size: 4.6 MB (4601747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a002cfde18f4d32e9bda7d5c7131103a158901700882310374c96e0ee7cf08b1`  
		Last Modified: Fri, 21 Jun 2024 11:02:00 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3132308d5a81e97764ae34bcd3db0ee3a87e1b70b27b4461bf458d0814b7309c`  
		Last Modified: Fri, 21 Jun 2024 11:02:00 GMT  
		Size: 10.0 KB (9993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7001c4cc7cb91d0fc6fdca4e1eb7a8e9992a0257b302b2be727a6c449c27c4d`  
		Last Modified: Fri, 21 Jun 2024 11:02:00 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeebe3e55553b397e76f0929a81ffe80955c75384d20531c7d3f2489ec23c131`  
		Last Modified: Fri, 21 Jun 2024 11:20:03 GMT  
		Size: 42.3 KB (42323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82105963ed7284714c3addbb8f69ad800d6e184df7b9e4ba0f12d311dc3ad3b`  
		Last Modified: Fri, 21 Jun 2024 11:20:11 GMT  
		Size: 329.0 MB (328968493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f917f2cccc0f636c125e0543681f9b677da5ce9b05d25d93b3c57a9b58d2fa0`  
		Last Modified: Fri, 21 Jun 2024 11:20:03 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a6349c56a61c2c19b8248fc5fed687c94d533edbc4926749bd37b6c53d6c64`  
		Last Modified: Fri, 21 Jun 2024 11:20:03 GMT  
		Size: 11.4 KB (11351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03ebe76c83d32d51d2ddad68eb9c7cd43e8c71d9263edf0fe505ed7d8831747`  
		Last Modified: Fri, 21 Jun 2024 11:20:04 GMT  
		Size: 13.2 MB (13154309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:67f557663e9200773f823c6941cc8441de1d90ad0621536340a6542e698f5792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5124278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce874fa14b4cb3c286a17da68e3031a2b8527fd0d9134a1da953e3ac09fd84d`

```dockerfile
```

-	Layers:
	-	`sha256:4a252f3490c14f39f9f13e6a14446dc561c0a4f262f892157801b6abc2ba8ebd`  
		Last Modified: Fri, 21 Jun 2024 11:20:03 GMT  
		Size: 5.1 MB (5085378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fa2a3ff88e12a2951473b89efe0b61e1c4bdab835ab880f876e76b116184c87`  
		Last Modified: Fri, 21 Jun 2024 11:20:02 GMT  
		Size: 38.9 KB (38900 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java17-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:acb240f09eabb13229e9ac0643fdf633164cbe4e79aebbb6189348fc72ee5e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.2 MB (446188751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d69a6ec7e737e6cd42e9c65e305a5b37756dbc6953b751472c440a267a2bcdb4`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 03 Jun 2024 10:34:18 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:34:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:34:22 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 10:34:22 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:09:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 05 Jun 2024 04:10:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:17:25 GMT
ENV JAVA_VERSION=jdk-17.0.11+9_openj9-0.44.0
# Wed, 05 Jun 2024 04:19:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6764398cdbcf824f2b99c095d58efb69b140d0c9824239560d58478f67bc15b';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='12a951e5353f4bccae5430de05a7204b6e1ad983780d3ecccacd2179936cc9ee';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='a47d3fabdf14c0f56561e5be24d689007f42cb079af0c89db235a58899fd4ab3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='049c6d6db4ba22fdfc7aaef3ee0af1bed1b71bda314b5c9ab27451d2c7392c1c';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 05 Jun 2024 04:19:24 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jun 2024 04:19:24 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 05 Jun 2024 04:19:58 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Tue, 18 Jun 2024 19:00:56 GMT
USER root
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_VERSION=24.0.0.6
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_BUILD_LABEL=cl240620240603-2001
# Tue, 18 Jun 2024 19:00:56 GMT
ARG OPENJ9_SCC=true
# Tue, 18 Jun 2024 19:00:56 GMT
ARG VERBOSE=false
# Tue, 18 Jun 2024 19:00:56 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240620240603-2001 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=24.0.0.6
# Tue, 18 Jun 2024 19:00:56 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 18 Jun 2024 19:00:56 GMT
USER 1001
# Tue, 18 Jun 2024 19:00:56 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 18 Jun 2024 19:00:56 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 18 Jun 2024 19:00:56 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:391f04f7f495cb5fc20be69876c8638cb8f316a2cddac5d48d77ca39244e6dea`  
		Last Modified: Wed, 05 Jun 2024 03:48:14 GMT  
		Size: 35.6 MB (35588332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98c5621e9cde7a31d0331e179ec18fc66523065d973f996e2d2dc3d2b24ee95`  
		Last Modified: Wed, 05 Jun 2024 04:28:48 GMT  
		Size: 12.9 MB (12889842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4e6566d3f51ab566fb3d3dfa61711bdcc1e44b54fec875f4ef521bfea3633f`  
		Last Modified: Wed, 05 Jun 2024 04:32:09 GMT  
		Size: 53.1 MB (53050207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c671c9ce6895e6f6cdd0fa0c79a2d6a894d68881243af956fa8ff43a814a9b6`  
		Last Modified: Wed, 05 Jun 2024 04:32:02 GMT  
		Size: 3.8 MB (3793667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4cde85ca008d58fd34fb1d1ae4cd05162493875c63fff5f9b3a24fa3a760ff`  
		Last Modified: Fri, 21 Jun 2024 04:42:49 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f166c6d1aa2007dd6d18970c9874c4c230086f8a42b0e62da17930976f0965`  
		Last Modified: Fri, 21 Jun 2024 04:42:49 GMT  
		Size: 10.0 KB (9993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6892206fedf0a1385075153416d8fe74ae1f1c86edf2015c14eebee0402f8739`  
		Last Modified: Fri, 21 Jun 2024 04:42:50 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1ac6280bfc7be241aece95b990bd678d63f3e34aae7219e869ceba6d549dbe`  
		Last Modified: Fri, 21 Jun 2024 04:55:48 GMT  
		Size: 36.5 KB (36498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512cef9a703c0c0e3195985d47388a5cb5d9bb609d4e886be7a9c49641f35192`  
		Last Modified: Fri, 21 Jun 2024 04:55:57 GMT  
		Size: 329.0 MB (328967994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf21ea84f4300301085a4829122a85edc748b3b3bfb53c59ae44a981505844e`  
		Last Modified: Fri, 21 Jun 2024 04:55:48 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6880b820d8c9fbb58d1994a8190906ff41435643d43b647fd16c3c9f2937a24b`  
		Last Modified: Fri, 21 Jun 2024 04:55:48 GMT  
		Size: 11.4 KB (11355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeaa4083282920287419e28911200604c78f7f190b4ed0b312723a3c16d2ff82`  
		Last Modified: Fri, 21 Jun 2024 04:55:50 GMT  
		Size: 11.8 MB (11838515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:5777a73978330c064bd3f24bb91fdaddbcda2571f4c63aaeb4aac77bfd1b7960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5128245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91fd295047f25a32bc3535bdcce47f173ba0a2245810ba3ea4266bb6c9d5c870`

```dockerfile
```

-	Layers:
	-	`sha256:99a44b8b47a3acd9b8974d1ae8839f5b98ac3047410a60df4d3f30528637be02`  
		Last Modified: Fri, 21 Jun 2024 04:55:48 GMT  
		Size: 5.1 MB (5089607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a02c84302dd8756cc5f264944333b286bf69f1a56821476e9a7ff88ca074a85d`  
		Last Modified: Fri, 21 Jun 2024 04:55:48 GMT  
		Size: 38.6 KB (38638 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java17-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:1bc28346993f025b6c34258a2ce24e593a5dbc5312d5a4bbb68444f0800542bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.2 MB (439177740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83f375ce1531e8e1d37e8003af61246ce6bbcf6af024f97385114b503ab4a4e1`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 03 Jun 2024 10:29:44 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:29:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:29:47 GMT
ADD file:4fb908f3bd908a7abc338d7e2006cb2c97aa7f83aca415f3b86c0ae86d61fed1 in / 
# Mon, 03 Jun 2024 10:29:47 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:39:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 05 Jun 2024 03:39:27 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:46:00 GMT
ENV JAVA_VERSION=jdk-17.0.11+9_openj9-0.44.0
# Wed, 05 Jun 2024 03:47:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6764398cdbcf824f2b99c095d58efb69b140d0c9824239560d58478f67bc15b';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='12a951e5353f4bccae5430de05a7204b6e1ad983780d3ecccacd2179936cc9ee';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='a47d3fabdf14c0f56561e5be24d689007f42cb079af0c89db235a58899fd4ab3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='049c6d6db4ba22fdfc7aaef3ee0af1bed1b71bda314b5c9ab27451d2c7392c1c';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 05 Jun 2024 03:47:42 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jun 2024 03:47:42 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 05 Jun 2024 03:48:14 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Tue, 18 Jun 2024 19:00:56 GMT
USER root
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_VERSION=24.0.0.6
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_BUILD_LABEL=cl240620240603-2001
# Tue, 18 Jun 2024 19:00:56 GMT
ARG OPENJ9_SCC=true
# Tue, 18 Jun 2024 19:00:56 GMT
ARG VERBOSE=false
# Tue, 18 Jun 2024 19:00:56 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240620240603-2001 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=24.0.0.6
# Tue, 18 Jun 2024 19:00:56 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.6 LIBERTY_SHA=08a2f3aee2f96fad4d2b6f728fd55658be3f02a0 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/24.0.0.6/openliberty-runtime-24.0.0.6.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 18 Jun 2024 19:00:56 GMT
USER 1001
# Tue, 18 Jun 2024 19:00:56 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 18 Jun 2024 19:00:56 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 18 Jun 2024 19:00:56 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:0424de0056677a3a1d049300220cb3d875fb304aae1fa90f7b0292500716e5ed`  
		Last Modified: Wed, 05 Jun 2024 03:12:35 GMT  
		Size: 28.6 MB (28637399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bec82a3649a60c81782d42d575ab21e0b591737fe7cf76c87eb0ee6dad4b737`  
		Last Modified: Wed, 05 Jun 2024 03:56:08 GMT  
		Size: 12.2 MB (12204558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c048e9004b047f1aa48da41e07bf0ace4fccb8e9602f3219be4c191e3dec17a`  
		Last Modified: Wed, 05 Jun 2024 03:58:57 GMT  
		Size: 50.4 MB (50407811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925c7758507a0684ddfbe10ceff956839b2c7ecc346bd80b0877d4b013997969`  
		Last Modified: Wed, 05 Jun 2024 03:58:50 GMT  
		Size: 5.1 MB (5059489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e089eee68983ec1dac2e089e8a1b14ffe28cd491cd6461beec63ed867eca9af`  
		Last Modified: Fri, 21 Jun 2024 12:53:01 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6d2da711564dfe20aab8df393cf110830294e73ec999eb2771d150e1337465`  
		Last Modified: Fri, 21 Jun 2024 12:53:01 GMT  
		Size: 10.0 KB (9996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed32647a8185ad2a9d04b067eb05543e98a415abda5bd2434056877c8b9c402`  
		Last Modified: Fri, 21 Jun 2024 12:53:02 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929f321369b3a98329bcc02113b176f1c56aae6a97fb2a565bb10a847dbaec9d`  
		Last Modified: Fri, 21 Jun 2024 13:02:16 GMT  
		Size: 33.1 KB (33111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cc1f0f8fed33468a58b66eac75d1cb8bcf43de0f3b84b23847b1414a425ecf`  
		Last Modified: Fri, 21 Jun 2024 13:02:23 GMT  
		Size: 329.0 MB (328967655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224675ea812fa8eb9cbf1652e14dd25fc407625358c06c1319b64327fa85a0bf`  
		Last Modified: Fri, 21 Jun 2024 13:02:17 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795afd5e78b1ad2e54373c5f5446aa12f9ef397dd557cd0e7fdea4b69d8c9285`  
		Last Modified: Fri, 21 Jun 2024 13:02:17 GMT  
		Size: 11.4 KB (11358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7f4b42d4b173b23079053edeb16e9cddda2725c97c6db1fed17bfd7df87fa9`  
		Last Modified: Fri, 21 Jun 2024 13:02:18 GMT  
		Size: 13.8 MB (13844011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:0357518d42b27d07b730efae12afeef23c5ad01bf84b17d9f1f600bddc04201b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5124060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d568fa7057874b28fe67b3015c40b664c01c2716149e3a68ac9bcaa721767f56`

```dockerfile
```

-	Layers:
	-	`sha256:179547f07b871c180570ee4918243cfe2369adf52658e6ee82f81973a20479b7`  
		Last Modified: Fri, 21 Jun 2024 13:02:16 GMT  
		Size: 5.1 MB (5085450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf0cd51acf433e0bf1d8b3299064e4c6db8153acbde54a060d7f21f09b3c2ac7`  
		Last Modified: Fri, 21 Jun 2024 13:02:16 GMT  
		Size: 38.6 KB (38610 bytes)  
		MIME: application/vnd.in-toto+json
