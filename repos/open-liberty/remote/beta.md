## `open-liberty:beta`

```console
$ docker pull open-liberty@sha256:25dad70a8eceadf31d0b6d0ccb97707d119e92232f923d762c846de4c3b23826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `open-liberty:beta` - linux; amd64

```console
$ docker pull open-liberty@sha256:22a93b513efe42495d52a2114b1cb2071714678faa2e385936565300b1321da6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.2 MB (336154232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb949b9c5677fa407104a6ccf3eb26b4ac28f06eef5890b1baaf3fbb98c189a0`
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
# Tue, 24 Nov 2020 01:49:40 GMT
ARG LIBERTY_VERSION=21.0.0.1
# Tue, 24 Nov 2020 01:49:40 GMT
ARG LIBERTY_SHA=5abe9cb23bc2f9ab2443699dd502b41bdca13335
# Tue, 24 Nov 2020 01:49:40 GMT
ARG LIBERTY_BUILD_LABEL=cl201220201111-0736
# Tue, 24 Nov 2020 01:49:40 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.1-beta/openliberty-runtime-21.0.0.1-beta.zip
# Tue, 24 Nov 2020 01:49:41 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Tue, 24 Nov 2020 01:49:41 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Tue, 24 Nov 2020 01:49:41 GMT
ARG OPENJ9_SCC=true
# Tue, 24 Nov 2020 01:49:41 GMT
ARG VERBOSE=false
# Tue, 24 Nov 2020 01:49:41 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl201220201111-0736 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with AdoptOpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=21.0.0.1
# Tue, 24 Nov 2020 01:49:42 GMT
COPY dir:7aff51efcc7f992aebc75df1ed45eed67c8a6f2121249c7fc7b35f23cc108b3d in /opt/ol/helpers 
# Tue, 24 Nov 2020 01:49:42 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Tue, 24 Nov 2020 01:49:55 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.1-beta/openliberty-runtime-21.0.0.1-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=5abe9cb23bc2f9ab2443699dd502b41bdca13335 LIBERTY_VERSION=21.0.0.1 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Tue, 24 Nov 2020 01:49:55 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 24 Nov 2020 01:49:57 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.1-beta/openliberty-runtime-21.0.0.1-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=5abe9cb23bc2f9ab2443699dd502b41bdca13335 LIBERTY_VERSION=21.0.0.1 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Tue, 24 Nov 2020 01:49:58 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.1-beta/openliberty-runtime-21.0.0.1-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=5abe9cb23bc2f9ab2443699dd502b41bdca13335 LIBERTY_VERSION=21.0.0.1 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Tue, 24 Nov 2020 01:50:39 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.1-beta/openliberty-runtime-21.0.0.1-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=5abe9cb23bc2f9ab2443699dd502b41bdca13335 LIBERTY_VERSION=21.0.0.1 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Tue, 24 Nov 2020 01:50:39 GMT
ENV RANDFILE=/tmp/.rnd
# Tue, 24 Nov 2020 01:50:39 GMT
USER 1001
# Tue, 24 Nov 2020 01:50:39 GMT
EXPOSE 9080 9443
# Tue, 24 Nov 2020 01:50:39 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 24 Nov 2020 01:50:40 GMT
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
	-	`sha256:0057385b6709b06d72fd5ccae5d1cdb36e865f7cd7a5be892833e11f809a911b`  
		Last Modified: Tue, 24 Nov 2020 01:56:30 GMT  
		Size: 8.5 KB (8517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a97c16cb8ed7046316a44eed530407e4526b6ee678191fca98548e8ee0cf32a`  
		Last Modified: Tue, 24 Nov 2020 01:56:29 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25c09de95d379d5a444fdb87215b5f95e741c33d7c2797bfbba37dbc3a9c62c`  
		Last Modified: Tue, 24 Nov 2020 01:56:45 GMT  
		Size: 224.6 MB (224636347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d02d6ad049a84976bc8d24fa15a13c6d37793f4124e8564971be0e2a773cbb00`  
		Last Modified: Tue, 24 Nov 2020 01:56:29 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ed4f0f6d6ca9aeec982899457777067e673596cf57563b888229de4678a4d5`  
		Last Modified: Tue, 24 Nov 2020 01:56:30 GMT  
		Size: 9.9 KB (9900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e89da7c7796e042c746502d1d6ddbc7a399ef5d933dac6f62bb1e4152c08d6a`  
		Last Modified: Tue, 24 Nov 2020 01:56:32 GMT  
		Size: 13.4 MB (13386350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:beta` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:900903bcfe4d124dd73f6acdf84ce143c3f677a44794bc4c30d53a5732ac48aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.8 MB (338795302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da0a7dec0398ce73385f2fdfc4829edc8e87a7b4b37d62df8f38f015e782659`
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
# Tue, 24 Nov 2020 03:29:01 GMT
ARG LIBERTY_VERSION=21.0.0.1
# Tue, 24 Nov 2020 03:29:10 GMT
ARG LIBERTY_SHA=5abe9cb23bc2f9ab2443699dd502b41bdca13335
# Tue, 24 Nov 2020 03:29:17 GMT
ARG LIBERTY_BUILD_LABEL=cl201220201111-0736
# Tue, 24 Nov 2020 03:29:22 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.1-beta/openliberty-runtime-21.0.0.1-beta.zip
# Tue, 24 Nov 2020 03:29:28 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Tue, 24 Nov 2020 03:29:34 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Tue, 24 Nov 2020 03:29:38 GMT
ARG OPENJ9_SCC=true
# Tue, 24 Nov 2020 03:29:43 GMT
ARG VERBOSE=false
# Tue, 24 Nov 2020 03:29:48 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl201220201111-0736 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with AdoptOpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=21.0.0.1
# Tue, 24 Nov 2020 03:29:51 GMT
COPY dir:7aff51efcc7f992aebc75df1ed45eed67c8a6f2121249c7fc7b35f23cc108b3d in /opt/ol/helpers 
# Tue, 24 Nov 2020 03:29:52 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Tue, 24 Nov 2020 03:30:32 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.1-beta/openliberty-runtime-21.0.0.1-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=5abe9cb23bc2f9ab2443699dd502b41bdca13335 LIBERTY_VERSION=21.0.0.1 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Tue, 24 Nov 2020 03:30:41 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 24 Nov 2020 03:31:01 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.1-beta/openliberty-runtime-21.0.0.1-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=5abe9cb23bc2f9ab2443699dd502b41bdca13335 LIBERTY_VERSION=21.0.0.1 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Tue, 24 Nov 2020 03:31:22 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.1-beta/openliberty-runtime-21.0.0.1-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=5abe9cb23bc2f9ab2443699dd502b41bdca13335 LIBERTY_VERSION=21.0.0.1 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Tue, 24 Nov 2020 03:32:27 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.1-beta/openliberty-runtime-21.0.0.1-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=5abe9cb23bc2f9ab2443699dd502b41bdca13335 LIBERTY_VERSION=21.0.0.1 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Tue, 24 Nov 2020 03:32:32 GMT
ENV RANDFILE=/tmp/.rnd
# Tue, 24 Nov 2020 03:32:35 GMT
USER 1001
# Tue, 24 Nov 2020 03:32:37 GMT
EXPOSE 9080 9443
# Tue, 24 Nov 2020 03:32:41 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 24 Nov 2020 03:32:45 GMT
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
	-	`sha256:843e19e6153436432ff249ca53d232839efad365d8286d0c226acedbf1614121`  
		Last Modified: Tue, 24 Nov 2020 03:57:32 GMT  
		Size: 8.5 KB (8548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2e8d64ed6095db424798c4fab239ba8f870ee70b0bcbea4623e168b6910189`  
		Last Modified: Tue, 24 Nov 2020 03:57:29 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4fb6c7d66112db2f01ed406c7a9dd50e69f73e30eb305371bec487534eb002c`  
		Last Modified: Tue, 24 Nov 2020 03:57:54 GMT  
		Size: 224.6 MB (224637205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e077ac5d3476a328056791d3f0461fa4b7ba81cf65043067176652b851c53ab`  
		Last Modified: Tue, 24 Nov 2020 03:57:29 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2b3c581e6e34af4baa398fb160a4c030680cbea878d0b43e048c9beabdb96f`  
		Last Modified: Tue, 24 Nov 2020 03:57:29 GMT  
		Size: 10.1 KB (10078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:337068db25f0f617d89f4a6389e4cac12a2ebea776957b58c115ad0e89e6de7b`  
		Last Modified: Tue, 24 Nov 2020 03:57:31 GMT  
		Size: 10.5 MB (10509954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:beta` - linux; s390x

```console
$ docker pull open-liberty@sha256:da19488b47961f2b2c5197305ba4ee74ef3b8a275d79f9ecf8d646e3d7ebdc07
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.5 MB (331519636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957446c96ecf3592be53b558ae9b69f41f8e082eab2def6e5632749f264c0245`
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
# Tue, 24 Nov 2020 01:46:52 GMT
ARG LIBERTY_VERSION=21.0.0.1
# Tue, 24 Nov 2020 01:46:53 GMT
ARG LIBERTY_SHA=5abe9cb23bc2f9ab2443699dd502b41bdca13335
# Tue, 24 Nov 2020 01:46:53 GMT
ARG LIBERTY_BUILD_LABEL=cl201220201111-0736
# Tue, 24 Nov 2020 01:46:54 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.1-beta/openliberty-runtime-21.0.0.1-beta.zip
# Tue, 24 Nov 2020 01:46:54 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Tue, 24 Nov 2020 01:46:55 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Tue, 24 Nov 2020 01:46:56 GMT
ARG OPENJ9_SCC=true
# Tue, 24 Nov 2020 01:46:56 GMT
ARG VERBOSE=false
# Tue, 24 Nov 2020 01:46:57 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl201220201111-0736 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with AdoptOpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=21.0.0.1
# Tue, 24 Nov 2020 01:46:57 GMT
COPY dir:7aff51efcc7f992aebc75df1ed45eed67c8a6f2121249c7fc7b35f23cc108b3d in /opt/ol/helpers 
# Tue, 24 Nov 2020 01:46:58 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Tue, 24 Nov 2020 01:47:33 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.1-beta/openliberty-runtime-21.0.0.1-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=5abe9cb23bc2f9ab2443699dd502b41bdca13335 LIBERTY_VERSION=21.0.0.1 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Tue, 24 Nov 2020 01:47:46 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 24 Nov 2020 01:47:48 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.1-beta/openliberty-runtime-21.0.0.1-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=5abe9cb23bc2f9ab2443699dd502b41bdca13335 LIBERTY_VERSION=21.0.0.1 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Tue, 24 Nov 2020 01:47:51 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.1-beta/openliberty-runtime-21.0.0.1-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=5abe9cb23bc2f9ab2443699dd502b41bdca13335 LIBERTY_VERSION=21.0.0.1 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Tue, 24 Nov 2020 01:48:28 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.1-beta/openliberty-runtime-21.0.0.1-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=5abe9cb23bc2f9ab2443699dd502b41bdca13335 LIBERTY_VERSION=21.0.0.1 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Tue, 24 Nov 2020 01:48:30 GMT
ENV RANDFILE=/tmp/.rnd
# Tue, 24 Nov 2020 01:48:30 GMT
USER 1001
# Tue, 24 Nov 2020 01:48:31 GMT
EXPOSE 9080 9443
# Tue, 24 Nov 2020 01:48:32 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 24 Nov 2020 01:48:32 GMT
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
	-	`sha256:b967f3498412140d55086237bf871e4c6a9ecd21fb1e53e8c6936e21d78a032b`  
		Last Modified: Tue, 24 Nov 2020 01:57:57 GMT  
		Size: 8.5 KB (8547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a15174cf0ce26e12c4071f42945e9a0c47ff8c06f4db6804f43d927cdf5cc0a`  
		Last Modified: Tue, 24 Nov 2020 01:57:55 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d76b0ae441db493b356ce23f5ffbc805700ebbc8cddf883cb5295caa001b3b`  
		Last Modified: Tue, 24 Nov 2020 01:58:06 GMT  
		Size: 224.6 MB (224636687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86442d91adf4e6b0a62d8e9af47b2b7c180f50d7a32f8b8ef637d000ca52514d`  
		Last Modified: Tue, 24 Nov 2020 01:57:56 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cec3dd9fee38f5a9e21189b5fd0cee0d6a4e32e94f086ca82d0cbe8cd43f664`  
		Last Modified: Tue, 24 Nov 2020 01:57:55 GMT  
		Size: 10.1 KB (10058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f33bcaeee4521a2021395f312be56fb7247c09cf01bbe9bf7aae843f604beeb4`  
		Last Modified: Tue, 24 Nov 2020 01:57:59 GMT  
		Size: 10.6 MB (10602604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
