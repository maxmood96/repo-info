## `open-liberty:full`

```console
$ docker pull open-liberty@sha256:ff9b703e6b6d99f15e4056508a4bcf4228547fbcf6f89c98fd6f03bc3584b449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `open-liberty:full` - linux; amd64

```console
$ docker pull open-liberty@sha256:d8ddf628bcd60d9d7b04037f65ae5f8cfbe4febe36d808be4d48c965dad7b3e7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285245204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01dbd22d389e3f49f0bc10ff3d55c22ad57b5149814b2a05c174e3f25e4d359`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Oct 2020 17:32:33 GMT
ADD file:435d9776fdd3a1834f344fb82e459dbbb67cd50c71ab5e29b719273888d5bb7c in / 
# Fri, 23 Oct 2020 17:32:34 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Oct 2020 17:32:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Oct 2020 17:32:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Oct 2020 17:32:36 GMT
CMD ["/bin/bash"]
# Wed, 28 Oct 2020 17:19:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Oct 2020 17:20:10 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 19:20:44 GMT
ENV JAVA_VERSION=jdk8u275-b01_openj9-0.23.0
# Thu, 19 Nov 2020 19:22:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='44d9feb46d613b55a8b7f249bbf5c5db27102e21a2fb64c5af72d1742a27b808';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u275-b01_openj9-0.23.0/OpenJDK8U-jre_aarch64_linux_openj9_8u275b01_openj9-0.23.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8003472eb7f44d401cea9d3258ee5d5e55e38707c5b9c0b292d672e801325440';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u275-b01_openj9-0.23.0/OpenJDK8U-jre_ppc64le_linux_openj9_8u275b01_openj9-0.23.0.tar.gz';          ;;        s390x)          ESUM='3f02a8bcb9ebad4061a4bf4600b6af0670e08ad87f75adb9adf7556035943195';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u275-b01_openj9-0.23.0/OpenJDK8U-jre_s390x_linux_openj9_8u275b01_openj9-0.23.0.tar.gz';          ;;        amd64|x86_64)          ESUM='75850de26fe76a1686f838403a34b67925c573fddc492ecee0b752d30ee2545a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u275-b01_openj9-0.23.0/OpenJDK8U-jre_x64_linux_openj9_8u275b01_openj9-0.23.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Nov 2020 19:22:35 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 19:22:35 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle
# Thu, 19 Nov 2020 19:24:01 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     SCC_GEN_RUNS_COUNT=3;     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     for i in $(seq 0 $SCC_GEN_RUNS_COUNT);     do         "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;         sleep 5;         "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh;         sleep 5;     done;         FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     for i in $(seq 0 $SCC_GEN_RUNS_COUNT);     do         "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;         sleep 5;         "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh;         sleep 5;     done;         FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 19 Nov 2020 19:24:01 GMT
ENV OPENJ9_JAVA_OPTIONS=-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 24 Nov 2020 01:51:53 GMT
ARG LIBERTY_VERSION=20.0.0.12
# Tue, 24 Nov 2020 01:52:43 GMT
ARG LIBERTY_SHA=18deec3a143a6a2ac46c717722a90678c524fa4e
# Tue, 24 Nov 2020 01:52:43 GMT
ARG LIBERTY_BUILD_LABEL=cl201220201111-0736
# Tue, 24 Nov 2020 01:52:43 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/20.0.0.12/openliberty-runtime-20.0.0.12.zip
# Tue, 24 Nov 2020 01:52:44 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Tue, 24 Nov 2020 01:52:44 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Tue, 24 Nov 2020 01:52:44 GMT
ARG OPENJ9_SCC=true
# Tue, 24 Nov 2020 01:52:44 GMT
ARG VERBOSE=false
# Tue, 24 Nov 2020 01:52:44 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl201220201111-0736 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=20.0.0.12
# Tue, 24 Nov 2020 01:52:45 GMT
COPY dir:7aff51efcc7f992aebc75df1ed45eed67c8a6f2121249c7fc7b35f23cc108b3d in /opt/ol/helpers 
# Tue, 24 Nov 2020 01:52:45 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Tue, 24 Nov 2020 01:52:56 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/20.0.0.12/openliberty-runtime-20.0.0.12.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=18deec3a143a6a2ac46c717722a90678c524fa4e LIBERTY_VERSION=20.0.0.12 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Tue, 24 Nov 2020 01:52:56 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 24 Nov 2020 01:52:57 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/20.0.0.12/openliberty-runtime-20.0.0.12.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=18deec3a143a6a2ac46c717722a90678c524fa4e LIBERTY_VERSION=20.0.0.12 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Tue, 24 Nov 2020 01:52:58 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/20.0.0.12/openliberty-runtime-20.0.0.12.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=18deec3a143a6a2ac46c717722a90678c524fa4e LIBERTY_VERSION=20.0.0.12 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Tue, 24 Nov 2020 01:53:34 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/20.0.0.12/openliberty-runtime-20.0.0.12.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=18deec3a143a6a2ac46c717722a90678c524fa4e LIBERTY_VERSION=20.0.0.12 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Tue, 24 Nov 2020 01:53:34 GMT
ENV RANDFILE=/tmp/.rnd
# Tue, 24 Nov 2020 01:53:34 GMT
USER 1001
# Tue, 24 Nov 2020 01:53:35 GMT
EXPOSE 9080 9443
# Tue, 24 Nov 2020 01:53:35 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 24 Nov 2020 01:53:35 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:6a5697faee43339ef8e33e3839060252392ad99325a48f7c9d7e93c22db4d4cf`  
		Last Modified: Thu, 08 Oct 2020 15:19:51 GMT  
		Size: 28.6 MB (28558714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba13d3bc422b493440f97a8f148d245e1999cb616cb05876edc3ef29e79852f2`  
		Last Modified: Fri, 23 Oct 2020 17:33:25 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a254829d9e55168306fd80a49e02eb015551facee9c444d9dce3b26d19238b82`  
		Last Modified: Fri, 23 Oct 2020 17:33:25 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03adaffd7e576f90e30e1dede0962fbbb0b58baede693e6375c2c137e506ef92`  
		Last Modified: Wed, 28 Oct 2020 17:37:00 GMT  
		Size: 16.0 MB (16031340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168877d9653146108785fc0fae8413373c3bf38570b5e2889cb26c20c7471a79`  
		Last Modified: Thu, 19 Nov 2020 19:26:57 GMT  
		Size: 49.2 MB (49176356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef63a68a33cbb86db9b0119dd1fba76f1b52451bde1540f521c6cf9e598c3887`  
		Last Modified: Thu, 19 Nov 2020 19:26:51 GMT  
		Size: 4.3 MB (4344237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b301e8e4912399d4efe9baca3d0fbbd6455c25dd47980b4ac4b8fa5cab6441a`  
		Last Modified: Tue, 24 Nov 2020 01:57:40 GMT  
		Size: 8.5 KB (8524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e04408fc6d03bf8ca6dfdebe18d700cae9fc0810e6a7cf6dff9e61d54da906`  
		Last Modified: Tue, 24 Nov 2020 01:57:39 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3222a371e7cd907495e787f86a28e3afddf26ca48f45553194584f516c4f3df8`  
		Last Modified: Tue, 24 Nov 2020 01:57:50 GMT  
		Size: 173.6 MB (173562178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641b79609c22cad5e21937da2fe522e3f795ed5f59c5d6fdf3cbc316ec757ff2`  
		Last Modified: Tue, 24 Nov 2020 01:57:39 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936a601e73fae6400ed40b14573f9e54b61d38ede651d8bf264d5de94d995c7a`  
		Last Modified: Tue, 24 Nov 2020 01:57:39 GMT  
		Size: 9.9 KB (9898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e362944bb1a2ca37fb1b1dd7ffad50932be48182ee0a67b97ffd3737935ae9cd`  
		Last Modified: Tue, 24 Nov 2020 01:57:41 GMT  
		Size: 13.6 MB (13551482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:full` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:e76c103cef8a2a7038801bb40bb9b1b1d64a65b63e4016daa3351b164aa3961b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.7 MB (287704444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2e7bf3831e52ec23bc69904f45ef578bf14c94829832737c97510c22f78b84`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Oct 2020 19:25:52 GMT
ADD file:b9c09681764b8697badc8139e82a30efeb353faf61258695d1cd3a843c4de6a8 in / 
# Fri, 23 Oct 2020 19:26:22 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Oct 2020 19:26:38 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Oct 2020 19:26:53 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Oct 2020 19:27:03 GMT
CMD ["/bin/bash"]
# Wed, 28 Oct 2020 17:17:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Oct 2020 17:19:40 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 19:38:23 GMT
ENV JAVA_VERSION=jdk8u275-b01_openj9-0.23.0
# Thu, 19 Nov 2020 19:43:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='44d9feb46d613b55a8b7f249bbf5c5db27102e21a2fb64c5af72d1742a27b808';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u275-b01_openj9-0.23.0/OpenJDK8U-jre_aarch64_linux_openj9_8u275b01_openj9-0.23.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8003472eb7f44d401cea9d3258ee5d5e55e38707c5b9c0b292d672e801325440';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u275-b01_openj9-0.23.0/OpenJDK8U-jre_ppc64le_linux_openj9_8u275b01_openj9-0.23.0.tar.gz';          ;;        s390x)          ESUM='3f02a8bcb9ebad4061a4bf4600b6af0670e08ad87f75adb9adf7556035943195';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u275-b01_openj9-0.23.0/OpenJDK8U-jre_s390x_linux_openj9_8u275b01_openj9-0.23.0.tar.gz';          ;;        amd64|x86_64)          ESUM='75850de26fe76a1686f838403a34b67925c573fddc492ecee0b752d30ee2545a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u275-b01_openj9-0.23.0/OpenJDK8U-jre_x64_linux_openj9_8u275b01_openj9-0.23.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Nov 2020 19:44:24 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 19:45:01 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle
# Thu, 19 Nov 2020 19:46:57 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     SCC_GEN_RUNS_COUNT=3;     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     for i in $(seq 0 $SCC_GEN_RUNS_COUNT);     do         "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;         sleep 5;         "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh;         sleep 5;     done;         FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     for i in $(seq 0 $SCC_GEN_RUNS_COUNT);     do         "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;         sleep 5;         "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh;         sleep 5;     done;         FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 19 Nov 2020 19:48:22 GMT
ENV OPENJ9_JAVA_OPTIONS=-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 24 Nov 2020 03:37:51 GMT
ARG LIBERTY_VERSION=20.0.0.12
# Tue, 24 Nov 2020 03:44:30 GMT
ARG LIBERTY_SHA=18deec3a143a6a2ac46c717722a90678c524fa4e
# Tue, 24 Nov 2020 03:44:33 GMT
ARG LIBERTY_BUILD_LABEL=cl201220201111-0736
# Tue, 24 Nov 2020 03:44:35 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/20.0.0.12/openliberty-runtime-20.0.0.12.zip
# Tue, 24 Nov 2020 03:44:38 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Tue, 24 Nov 2020 03:44:42 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Tue, 24 Nov 2020 03:44:46 GMT
ARG OPENJ9_SCC=true
# Tue, 24 Nov 2020 03:44:47 GMT
ARG VERBOSE=false
# Tue, 24 Nov 2020 03:44:49 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl201220201111-0736 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=20.0.0.12
# Tue, 24 Nov 2020 03:44:50 GMT
COPY dir:7aff51efcc7f992aebc75df1ed45eed67c8a6f2121249c7fc7b35f23cc108b3d in /opt/ol/helpers 
# Tue, 24 Nov 2020 03:44:52 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Tue, 24 Nov 2020 03:45:30 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/20.0.0.12/openliberty-runtime-20.0.0.12.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=18deec3a143a6a2ac46c717722a90678c524fa4e LIBERTY_VERSION=20.0.0.12 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Tue, 24 Nov 2020 03:45:46 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 24 Nov 2020 03:46:00 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/20.0.0.12/openliberty-runtime-20.0.0.12.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=18deec3a143a6a2ac46c717722a90678c524fa4e LIBERTY_VERSION=20.0.0.12 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Tue, 24 Nov 2020 03:46:15 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/20.0.0.12/openliberty-runtime-20.0.0.12.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=18deec3a143a6a2ac46c717722a90678c524fa4e LIBERTY_VERSION=20.0.0.12 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Tue, 24 Nov 2020 03:47:17 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/20.0.0.12/openliberty-runtime-20.0.0.12.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=18deec3a143a6a2ac46c717722a90678c524fa4e LIBERTY_VERSION=20.0.0.12 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Tue, 24 Nov 2020 03:47:23 GMT
ENV RANDFILE=/tmp/.rnd
# Tue, 24 Nov 2020 03:47:28 GMT
USER 1001
# Tue, 24 Nov 2020 03:47:31 GMT
EXPOSE 9080 9443
# Tue, 24 Nov 2020 03:47:33 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 24 Nov 2020 03:47:38 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:76ff736f6fb2d41940a6cbdeab4242e9a64ef7df99ee4f3d9fcb9ec67bfccfc6`  
		Last Modified: Mon, 12 Oct 2020 16:20:28 GMT  
		Size: 33.3 MB (33275528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3d354673d1251716a1ed9cc3460095ee31664859e23d7e616546a17d287728`  
		Last Modified: Fri, 23 Oct 2020 19:31:29 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434fabf01a92cfd54e3ae6f5e3dc7a3837ac2199999f713fbdf5cb2c800324a2`  
		Last Modified: Fri, 23 Oct 2020 19:31:29 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb82384b001eeabdc2ca426e902a10696a33f7e7723f24eca9f4848ebbe13a5e`  
		Last Modified: Wed, 28 Oct 2020 17:47:13 GMT  
		Size: 17.2 MB (17208276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2f79c447f20a611d40b2f64ea6c3188f6d7dd5aeb4381c79836741f2f4d1ce`  
		Last Modified: Thu, 19 Nov 2020 20:10:00 GMT  
		Size: 49.6 MB (49603251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b5efb5095e6b26f2ac3da3dfd36d03904251df7024ad41aac8a362fd494416`  
		Last Modified: Thu, 19 Nov 2020 20:09:52 GMT  
		Size: 3.5 MB (3539881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f43c793230c1bc06ea952af86e196c6c84c71921201aeaa9843fbef5ba9df34`  
		Last Modified: Tue, 24 Nov 2020 03:59:11 GMT  
		Size: 8.5 KB (8547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d7302a20cb17fd50c657ad3f9830d84023e24495ebe5acea8b01ff028a806b8`  
		Last Modified: Tue, 24 Nov 2020 03:59:09 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702716097cf974ef7c1ad855c59c86afeda102fb9d42e48ffe786a7a899afb0d`  
		Last Modified: Tue, 24 Nov 2020 03:59:25 GMT  
		Size: 173.6 MB (173562826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13b31bcb951bf4e603f2837ada0440f38d229813d9b67118437fca0f5bdd6b58`  
		Last Modified: Tue, 24 Nov 2020 03:59:08 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f975e52e612075d5916bf563ca11d8ce95982baaa86c8c3e2da13b3fd7e71a`  
		Last Modified: Tue, 24 Nov 2020 03:59:08 GMT  
		Size: 10.1 KB (10060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f918938a31f3e45119487cfa30fb1c1402402d8c39c644de919eec00fe597464`  
		Last Modified: Tue, 24 Nov 2020 03:59:11 GMT  
		Size: 10.5 MB (10493506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:full` - linux; s390x

```console
$ docker pull open-liberty@sha256:eed3db11abf068b2f5d23e7cf2c9ef6ca7a1dbb363bf1089d783b095e5d6aaca
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.4 MB (280427439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c296a0de601cc1db9da69c6c62c6005dee80ba25360b5a9f2ab076882eb0653`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Oct 2020 19:09:19 GMT
ADD file:9b934c86e9ab1dd29cef318d8dd9cd1228b9d92124f434c50ad7d03ede1a5c76 in / 
# Fri, 23 Oct 2020 19:09:24 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Oct 2020 19:09:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Oct 2020 19:09:27 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Oct 2020 19:09:27 GMT
CMD ["/bin/bash"]
# Wed, 28 Oct 2020 17:41:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Oct 2020 17:41:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 19:43:34 GMT
ENV JAVA_VERSION=jdk8u275-b01_openj9-0.23.0
# Thu, 19 Nov 2020 19:45:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='44d9feb46d613b55a8b7f249bbf5c5db27102e21a2fb64c5af72d1742a27b808';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u275-b01_openj9-0.23.0/OpenJDK8U-jre_aarch64_linux_openj9_8u275b01_openj9-0.23.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8003472eb7f44d401cea9d3258ee5d5e55e38707c5b9c0b292d672e801325440';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u275-b01_openj9-0.23.0/OpenJDK8U-jre_ppc64le_linux_openj9_8u275b01_openj9-0.23.0.tar.gz';          ;;        s390x)          ESUM='3f02a8bcb9ebad4061a4bf4600b6af0670e08ad87f75adb9adf7556035943195';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u275-b01_openj9-0.23.0/OpenJDK8U-jre_s390x_linux_openj9_8u275b01_openj9-0.23.0.tar.gz';          ;;        amd64|x86_64)          ESUM='75850de26fe76a1686f838403a34b67925c573fddc492ecee0b752d30ee2545a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u275-b01_openj9-0.23.0/OpenJDK8U-jre_x64_linux_openj9_8u275b01_openj9-0.23.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 19 Nov 2020 19:45:50 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 19:45:50 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle
# Thu, 19 Nov 2020 19:47:21 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     SCC_GEN_RUNS_COUNT=3;     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     for i in $(seq 0 $SCC_GEN_RUNS_COUNT);     do         "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;         sleep 5;         "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh;         sleep 5;     done;         FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     for i in $(seq 0 $SCC_GEN_RUNS_COUNT);     do         "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;         sleep 5;         "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh;         sleep 5;     done;         FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 19 Nov 2020 19:47:22 GMT
ENV OPENJ9_JAVA_OPTIONS=-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 24 Nov 2020 01:50:29 GMT
ARG LIBERTY_VERSION=20.0.0.12
# Tue, 24 Nov 2020 01:51:58 GMT
ARG LIBERTY_SHA=18deec3a143a6a2ac46c717722a90678c524fa4e
# Tue, 24 Nov 2020 01:51:59 GMT
ARG LIBERTY_BUILD_LABEL=cl201220201111-0736
# Tue, 24 Nov 2020 01:51:59 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/20.0.0.12/openliberty-runtime-20.0.0.12.zip
# Tue, 24 Nov 2020 01:52:00 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Tue, 24 Nov 2020 01:52:01 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Tue, 24 Nov 2020 01:52:01 GMT
ARG OPENJ9_SCC=true
# Tue, 24 Nov 2020 01:52:02 GMT
ARG VERBOSE=false
# Tue, 24 Nov 2020 01:52:02 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl201220201111-0736 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=20.0.0.12
# Tue, 24 Nov 2020 01:52:03 GMT
COPY dir:7aff51efcc7f992aebc75df1ed45eed67c8a6f2121249c7fc7b35f23cc108b3d in /opt/ol/helpers 
# Tue, 24 Nov 2020 01:52:03 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Tue, 24 Nov 2020 01:52:27 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/20.0.0.12/openliberty-runtime-20.0.0.12.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=18deec3a143a6a2ac46c717722a90678c524fa4e LIBERTY_VERSION=20.0.0.12 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Tue, 24 Nov 2020 01:52:38 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 24 Nov 2020 01:52:40 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/20.0.0.12/openliberty-runtime-20.0.0.12.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=18deec3a143a6a2ac46c717722a90678c524fa4e LIBERTY_VERSION=20.0.0.12 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Tue, 24 Nov 2020 01:52:42 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/20.0.0.12/openliberty-runtime-20.0.0.12.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=18deec3a143a6a2ac46c717722a90678c524fa4e LIBERTY_VERSION=20.0.0.12 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Tue, 24 Nov 2020 01:53:19 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/20.0.0.12/openliberty-runtime-20.0.0.12.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=18deec3a143a6a2ac46c717722a90678c524fa4e LIBERTY_VERSION=20.0.0.12 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Tue, 24 Nov 2020 01:53:21 GMT
ENV RANDFILE=/tmp/.rnd
# Tue, 24 Nov 2020 01:53:21 GMT
USER 1001
# Tue, 24 Nov 2020 01:53:22 GMT
EXPOSE 9080 9443
# Tue, 24 Nov 2020 01:53:22 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 24 Nov 2020 01:53:23 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:d3e8e1a5d50716d6aabb0cef46599f9e7a722a560910d6f724737aaef0a7d6c3`  
		Last Modified: Mon, 12 Oct 2020 16:45:31 GMT  
		Size: 27.2 MB (27224393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04282efaafb3c9b53bba677fc3c06c478dc1613c1f21939bfa2c113aeef2f99c`  
		Last Modified: Fri, 23 Oct 2020 19:10:20 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6269ae100536d7559ae6ebe6606b4405ebb706c3d963926c5568b6e7fd954582`  
		Last Modified: Fri, 23 Oct 2020 19:10:19 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5cd8065d26d8f90607b2debf915de6242befbe898f8fb305dbd99dc8df92d3a`  
		Last Modified: Wed, 28 Oct 2020 17:59:30 GMT  
		Size: 15.8 MB (15772935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0b1fbe0a76f4faf6a1c8bc5e39d2af4c37d0008acc2423ef0e7890a22ad931`  
		Last Modified: Thu, 19 Nov 2020 19:51:05 GMT  
		Size: 48.8 MB (48789618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db73010105b38fe1b46be46b1363f5412190449bb56d6a5709d6c5972e76801`  
		Last Modified: Thu, 19 Nov 2020 19:50:59 GMT  
		Size: 4.5 MB (4472229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a94bca6b577989725aa37928cb1e2f8bcb96034452849a0cbb9ffb5009159a`  
		Last Modified: Tue, 24 Nov 2020 01:58:59 GMT  
		Size: 8.5 KB (8547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172c07fad3f099968bab95bf0189d7f6a3f481c13c5446de9e8f39b839b2da00`  
		Last Modified: Tue, 24 Nov 2020 01:58:56 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd4714ad37fa09b0664970a83b122b03b4ebf09622a8dde6d0595ffb231b84c`  
		Last Modified: Tue, 24 Nov 2020 01:59:06 GMT  
		Size: 173.6 MB (173562256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac2cdacffdfc4bcd2b78cedaecc6e113a706ee6d44c4111609593f619a50943`  
		Last Modified: Tue, 24 Nov 2020 01:58:58 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a45c2f182f51e4078348c6ba04cc7c0ec04b7de450c22c8e22bfe1abb3bc12`  
		Last Modified: Tue, 24 Nov 2020 01:58:56 GMT  
		Size: 10.0 KB (10045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c01009e4beaff98f2c631248b7783aad02e8a746adf15251bce584e7e0da3c`  
		Last Modified: Tue, 24 Nov 2020 01:58:58 GMT  
		Size: 10.6 MB (10584852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
