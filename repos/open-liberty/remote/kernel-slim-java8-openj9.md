## `open-liberty:kernel-slim-java8-openj9`

```console
$ docker pull open-liberty@sha256:6f4f60a9da3fa98fea6253be6f8ab37f26c8d3f1175a1c86be886af516180e98
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

### `open-liberty:kernel-slim-java8-openj9` - linux; amd64

```console
$ docker pull open-liberty@sha256:e283dc96f5f14dbeb97b0c157e18d16ae1926e249186dc469f9bc69f4ebe7a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118832081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980f4a44ffb3e13cb54e3c1487b82944b9d90e19d91c650fcf742900bbb16cf8`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:33:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:33:44 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:33:44 GMT
ENV JAVA_VERSION=jdk8u482-b08.1_openj9-0.57.0
# Tue, 17 Mar 2026 01:33:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='d8fcad671559ab383d55d331db6725a5957f110faffe17d766c7ca3b14e71abd';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_aarch64_linux_8.0.482.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='4b66859a60b250db44e6fe3b8bd8cb5f3908be50315bad0e946961c7ac03a59a';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_ppc64le_linux_8.0.482.1.tar.gz';          ;;        amd64|x86_64)          ESUM='0bf81e496b5fed8669fc5b624ba7fb45fe05d7b9c19485f441ab48d2edad68fe';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_x64_linux_8.0.482.1.tar.gz';          ;;        s390x)          ESUM='a91c33d74cc5a0826f56efe48aa2f1223c6e25189a6bb8a8444e6f67b2581765';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_s390x_linux_8.0.482.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Mar 2026 01:33:46 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:33:46 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Mar 2026 01:34:49 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 17 Mar 2026 02:42:07 GMT
USER root
# Tue, 17 Mar 2026 02:42:07 GMT
ARG LIBERTY_VERSION=26.0.0.2
# Tue, 17 Mar 2026 02:42:07 GMT
ARG LIBERTY_SHA=7264724ce8ed2514f0586e10d43ed3c1bb7ff26f
# Tue, 17 Mar 2026 02:42:07 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.2/openliberty-kernel-26.0.0.2.zip
# Tue, 17 Mar 2026 02:42:07 GMT
ARG LIBERTY_BUILD_LABEL=cl260220260207-1901
# Tue, 17 Mar 2026 02:42:07 GMT
ARG OPENJ9_SCC=true
# Tue, 17 Mar 2026 02:42:07 GMT
ARG VERBOSE=false
# Tue, 17 Mar 2026 02:42:07 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260220260207-1901 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=26.0.0.2 liberty.version=26.0.0.2 io.openliberty.version=26.0.0.2
# Tue, 17 Mar 2026 02:42:07 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 17 Mar 2026 02:42:07 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 17 Mar 2026 02:42:07 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 17 Mar 2026 02:42:07 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=7264724ce8ed2514f0586e10d43ed3c1bb7ff26f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.2/openliberty-kernel-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 17 Mar 2026 02:42:17 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=7264724ce8ed2514f0586e10d43ed3c1bb7ff26f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.2/openliberty-kernel-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 17 Mar 2026 02:42:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 17 Mar 2026 02:42:18 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=7264724ce8ed2514f0586e10d43ed3c1bb7ff26f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.2/openliberty-kernel-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 17 Mar 2026 02:42:18 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=7264724ce8ed2514f0586e10d43ed3c1bb7ff26f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.2/openliberty-kernel-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Tue, 17 Mar 2026 02:42:21 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=7264724ce8ed2514f0586e10d43ed3c1bb7ff26f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.2/openliberty-kernel-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 17 Mar 2026 02:42:21 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 17 Mar 2026 02:42:21 GMT
USER 1001
# Tue, 17 Mar 2026 02:42:21 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 17 Mar 2026 02:42:21 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 17 Mar 2026 02:42:21 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059f6885c3a59396e58185af50c67086e7395194e4bdf3f9c1a6ec6d7b1140d7`  
		Last Modified: Tue, 17 Mar 2026 01:35:01 GMT  
		Size: 12.8 MB (12805219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb143f5dc096332f7a83a030ee6388fd2e95fb37cb7e0727bfc4ca68f2baff0`  
		Last Modified: Tue, 17 Mar 2026 01:35:02 GMT  
		Size: 54.0 MB (53997193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82fed6933c4a2c709fdbe73e3aecf4664714bce3cd447b2bab1f029aec998bef`  
		Last Modified: Tue, 17 Mar 2026 01:35:00 GMT  
		Size: 4.3 MB (4253834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c08632ef0409002534ff0122b06eae3c1508977a69dd675e55eaa5786f88b93`  
		Last Modified: Tue, 17 Mar 2026 02:42:29 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cbcd85fa33f7b66e6e4e97ebfb51ebdb10c16623042768a1d0dc34642895b28`  
		Last Modified: Tue, 17 Mar 2026 02:42:29 GMT  
		Size: 11.8 KB (11825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ffbe2df6b93af21a43b534d102ca2eac8e182f15d4bea7dc8d6a3a2a811322`  
		Last Modified: Tue, 17 Mar 2026 02:42:29 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcc90e79c9e12e19a3b2649999f61635e3369fa835fcc4430fb2c59b1e6469b`  
		Last Modified: Tue, 17 Mar 2026 02:42:29 GMT  
		Size: 31.7 KB (31748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48e425fed794ebd43a4a518ab9d2790d7b9bd29a9841a9a4c76a8998f2fd940`  
		Last Modified: Tue, 17 Mar 2026 02:42:31 GMT  
		Size: 15.2 MB (15237394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473b482788699485999ac914c2503f38e23f5143b3917c38b0c6c33c7016077a`  
		Last Modified: Tue, 17 Mar 2026 02:42:30 GMT  
		Size: 740.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31f2fed2cfd8842a69c2ca1fe56daab410f56b92667766c6191fe33d5ef45b7`  
		Last Modified: Tue, 17 Mar 2026 02:42:30 GMT  
		Size: 12.9 KB (12922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4334fb49af074ac0d12015dcd6809bf47b20d0f2719d5f89d1285cb960c86d8`  
		Last Modified: Tue, 17 Mar 2026 02:42:31 GMT  
		Size: 2.7 MB (2747922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:kernel-slim-java8-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:ceabd056d6ba86eabdc7576ebef75427fc0b1042e214c09ade15d813b8f4fb8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3375836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69121e9231a7bfcd6ad9a2cadf5dc6b51e2e97eaaeed2e4b44ee8568ea201467`

```dockerfile
```

-	Layers:
	-	`sha256:d90cc9cb41a69c5b7bb64fa6c2d00fc24466a1f55e05ff0c6dd3764dc39a59a6`  
		Last Modified: Tue, 17 Mar 2026 02:42:29 GMT  
		Size: 3.3 MB (3336046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5093f2ca078be1068f8bf97eff8e2491b50dc1f9353bd76097f669d9fb2c0cd`  
		Last Modified: Tue, 17 Mar 2026 02:42:29 GMT  
		Size: 39.8 KB (39790 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:kernel-slim-java8-openj9` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:e01e42bb520c4694d67228e99cb4b49a9a8bc4b7b57bec89f3bc30fc28f491e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117595011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b59051e3ed8d65f43ccac5cbf23e04e86e928b8b878e386b6e9c01c7bb42cf8b`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:35:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:35:00 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:35:00 GMT
ENV JAVA_VERSION=jdk8u482-b08.1_openj9-0.57.0
# Tue, 17 Mar 2026 01:35:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='d8fcad671559ab383d55d331db6725a5957f110faffe17d766c7ca3b14e71abd';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_aarch64_linux_8.0.482.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='4b66859a60b250db44e6fe3b8bd8cb5f3908be50315bad0e946961c7ac03a59a';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_ppc64le_linux_8.0.482.1.tar.gz';          ;;        amd64|x86_64)          ESUM='0bf81e496b5fed8669fc5b624ba7fb45fe05d7b9c19485f441ab48d2edad68fe';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_x64_linux_8.0.482.1.tar.gz';          ;;        s390x)          ESUM='a91c33d74cc5a0826f56efe48aa2f1223c6e25189a6bb8a8444e6f67b2581765';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_s390x_linux_8.0.482.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Mar 2026 01:35:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:35:02 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Mar 2026 01:36:05 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 17 Mar 2026 02:46:27 GMT
USER root
# Tue, 17 Mar 2026 02:46:27 GMT
ARG LIBERTY_VERSION=26.0.0.2
# Tue, 17 Mar 2026 02:46:27 GMT
ARG LIBERTY_SHA=7264724ce8ed2514f0586e10d43ed3c1bb7ff26f
# Tue, 17 Mar 2026 02:46:27 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.2/openliberty-kernel-26.0.0.2.zip
# Tue, 17 Mar 2026 02:46:27 GMT
ARG LIBERTY_BUILD_LABEL=cl260220260207-1901
# Tue, 17 Mar 2026 02:46:27 GMT
ARG OPENJ9_SCC=true
# Tue, 17 Mar 2026 02:46:27 GMT
ARG VERBOSE=false
# Tue, 17 Mar 2026 02:46:27 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260220260207-1901 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=26.0.0.2 liberty.version=26.0.0.2 io.openliberty.version=26.0.0.2
# Tue, 17 Mar 2026 02:46:27 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 17 Mar 2026 02:46:27 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 17 Mar 2026 02:46:27 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 17 Mar 2026 02:46:27 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=7264724ce8ed2514f0586e10d43ed3c1bb7ff26f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.2/openliberty-kernel-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 17 Mar 2026 02:46:40 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=7264724ce8ed2514f0586e10d43ed3c1bb7ff26f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.2/openliberty-kernel-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 17 Mar 2026 02:46:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 17 Mar 2026 02:46:41 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=7264724ce8ed2514f0586e10d43ed3c1bb7ff26f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.2/openliberty-kernel-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 17 Mar 2026 02:46:41 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=7264724ce8ed2514f0586e10d43ed3c1bb7ff26f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.2/openliberty-kernel-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Tue, 17 Mar 2026 02:46:45 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=7264724ce8ed2514f0586e10d43ed3c1bb7ff26f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.2/openliberty-kernel-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 17 Mar 2026 02:46:45 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 17 Mar 2026 02:46:45 GMT
USER 1001
# Tue, 17 Mar 2026 02:46:45 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 17 Mar 2026 02:46:45 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 17 Mar 2026 02:46:45 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4d74baf060663279eeeb890b897566f7cd73e2daf822b7072afed2d7383943`  
		Last Modified: Tue, 17 Mar 2026 01:36:17 GMT  
		Size: 12.8 MB (12837534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48073fd700af09e12a53edcc3978bd58f433e7cc32086a2f42d97be1c9ce7b23`  
		Last Modified: Tue, 17 Mar 2026 01:36:18 GMT  
		Size: 53.7 MB (53702900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ffcd50baf446fc05677f89c76c26981f7a5b400f09f9d75e0d853c42ad43c4`  
		Last Modified: Tue, 17 Mar 2026 01:36:17 GMT  
		Size: 4.1 MB (4114825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c6ef1a08ff0bab1f9654f1df3cf8e2495092dbffbcb7c4a145c01c58d445de`  
		Last Modified: Tue, 17 Mar 2026 02:46:53 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96866f7135cbb75d439a4f4b88aaecaf7d63c7ab691a8ddaa14a93efd2cb296a`  
		Last Modified: Tue, 17 Mar 2026 02:46:53 GMT  
		Size: 11.8 KB (11818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcb7514e58c1cc97133f836424259d13ec20b6ce012fb252932a8aea68d83a7`  
		Last Modified: Tue, 17 Mar 2026 02:46:53 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f6e20a5d7b55c0e5498e0002d82dd08cad7370421e1f5cd2cc7e79104c0d2a`  
		Last Modified: Tue, 17 Mar 2026 02:46:53 GMT  
		Size: 42.3 KB (42324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f11cbb1c4debebe56d5b71afc9ef0e416f100f48eff4a90cf6fe4afc56ad61`  
		Last Modified: Tue, 17 Mar 2026 02:46:55 GMT  
		Size: 15.2 MB (15237504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14991df9031f9353f3da3e8818ace1d94a303ecc21e1f88a16936ca59454c83`  
		Last Modified: Tue, 17 Mar 2026 02:46:54 GMT  
		Size: 737.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12cb15be0d88cc97360163125fba9d2b0e23f3bebd6b27ff67ed29a5792845d`  
		Last Modified: Tue, 17 Mar 2026 02:46:55 GMT  
		Size: 12.9 KB (12918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18e70515ed21cecd257b6f3181d73c81f2280ac0dc8cf748e772af9231240c9`  
		Last Modified: Tue, 17 Mar 2026 02:46:55 GMT  
		Size: 2.8 MB (2763454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:kernel-slim-java8-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:b894df2e78dbd5d0e40060ecb256404278c8f3b077a744ccd7aef14ed41c59ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3376602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:697fc7de5884cde796657aa29a75999b78502b145debbcfe53bdc26ad2ae8d19`

```dockerfile
```

-	Layers:
	-	`sha256:a01c5eb0f3b8957cd55b24d987130e0c4985a2326bf16cfdd12a6e3d156d40d2`  
		Last Modified: Tue, 17 Mar 2026 02:46:54 GMT  
		Size: 3.3 MB (3336659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4be8942a25289158d844ae74ec07838975e10916ddee89ba8663793d3580f2e6`  
		Last Modified: Tue, 17 Mar 2026 02:46:53 GMT  
		Size: 39.9 KB (39943 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:kernel-slim-java8-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:d1320ca2ef3ec0a9d17da437860e3c86b857909da58db252b6913d649c5d6b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125172177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:595a6e5d71f9a958278722a8d92c5de29ee8895425d9e5cb1e6d90f839528aae`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:28:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:28:56 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:28:56 GMT
ENV JAVA_VERSION=jdk8u482-b08.1_openj9-0.57.0
# Tue, 03 Mar 2026 20:12:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='d8fcad671559ab383d55d331db6725a5957f110faffe17d766c7ca3b14e71abd';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_aarch64_linux_8.0.482.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='4b66859a60b250db44e6fe3b8bd8cb5f3908be50315bad0e946961c7ac03a59a';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_ppc64le_linux_8.0.482.1.tar.gz';          ;;        amd64|x86_64)          ESUM='0bf81e496b5fed8669fc5b624ba7fb45fe05d7b9c19485f441ab48d2edad68fe';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_x64_linux_8.0.482.1.tar.gz';          ;;        s390x)          ESUM='a91c33d74cc5a0826f56efe48aa2f1223c6e25189a6bb8a8444e6f67b2581765';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_s390x_linux_8.0.482.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 03 Mar 2026 20:12:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Mar 2026 20:12:58 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 03 Mar 2026 20:14:03 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 03 Mar 2026 22:40:35 GMT
USER root
# Tue, 03 Mar 2026 22:40:35 GMT
ARG LIBERTY_VERSION=26.0.0.2
# Tue, 03 Mar 2026 22:40:35 GMT
ARG LIBERTY_SHA=7264724ce8ed2514f0586e10d43ed3c1bb7ff26f
# Tue, 03 Mar 2026 22:40:35 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.2/openliberty-kernel-26.0.0.2.zip
# Tue, 03 Mar 2026 22:40:35 GMT
ARG LIBERTY_BUILD_LABEL=cl260220260207-1901
# Tue, 03 Mar 2026 22:40:35 GMT
ARG OPENJ9_SCC=true
# Tue, 03 Mar 2026 22:40:35 GMT
ARG VERBOSE=false
# Tue, 03 Mar 2026 22:40:35 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260220260207-1901 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=26.0.0.2 liberty.version=26.0.0.2 io.openliberty.version=26.0.0.2
# Tue, 03 Mar 2026 22:40:35 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 03 Mar 2026 22:43:24 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 03 Mar 2026 22:43:26 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 03 Mar 2026 22:43:28 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=7264724ce8ed2514f0586e10d43ed3c1bb7ff26f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.2/openliberty-kernel-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 03 Mar 2026 22:43:46 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=7264724ce8ed2514f0586e10d43ed3c1bb7ff26f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.2/openliberty-kernel-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 03 Mar 2026 22:43:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 03 Mar 2026 22:43:49 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=7264724ce8ed2514f0586e10d43ed3c1bb7ff26f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.2/openliberty-kernel-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 03 Mar 2026 22:43:54 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=7264724ce8ed2514f0586e10d43ed3c1bb7ff26f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.2/openliberty-kernel-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Tue, 03 Mar 2026 22:44:01 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=7264724ce8ed2514f0586e10d43ed3c1bb7ff26f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.2/openliberty-kernel-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 03 Mar 2026 22:44:01 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 03 Mar 2026 22:44:01 GMT
USER 1001
# Tue, 03 Mar 2026 22:44:01 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 03 Mar 2026 22:44:01 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 03 Mar 2026 22:44:01 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bc74705b5205a118b6fdfc67d17a8b658c02f7792610bbbab1a9a9579b5bc8`  
		Last Modified: Tue, 17 Feb 2026 20:30:36 GMT  
		Size: 13.8 MB (13799621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123c70fa2182ac012b07cdad1e195ee76ed55742bf9836eb005c1614bb3561ca`  
		Last Modified: Tue, 03 Mar 2026 20:14:35 GMT  
		Size: 55.6 MB (55597413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d94a3ea6ca35b4f8f1ea6e2ac724c0cdfe51d96daf785f8fc5db5db693d719c`  
		Last Modified: Tue, 03 Mar 2026 20:14:33 GMT  
		Size: 3.5 MB (3499449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08001c2726bf2fb76af48b6294ef587bb43d96120695aeefb3202e7b3e652e1`  
		Last Modified: Tue, 03 Mar 2026 22:42:51 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f1f166c1ed56529372697058387d0c264974afdcccfc382138db5bff0cafae`  
		Last Modified: Tue, 03 Mar 2026 22:44:34 GMT  
		Size: 11.8 KB (11823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71abd17b7e39d8afbf8517f46a9e778066778e2710c060c07a79684f8feba3e8`  
		Last Modified: Tue, 03 Mar 2026 22:44:34 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cceb88079c8ddac2c7d68ca90354aa1a5db1414b2e0e54b79b17cac4f3fad34`  
		Last Modified: Tue, 03 Mar 2026 22:44:34 GMT  
		Size: 36.5 KB (36497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6dfa58f885213d374f879d4176635dee449aee165ecffbf76776ae779c9420`  
		Last Modified: Tue, 03 Mar 2026 22:44:34 GMT  
		Size: 15.2 MB (15237826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a826239742d5088216029090ab466032c45e2b537e2e82acf53a4a76d0c8e3`  
		Last Modified: Tue, 03 Mar 2026 22:44:35 GMT  
		Size: 736.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd5fa096a7f35836409ebfba7ee4679475f5173b18dd08d3a25b1e406b5ffc0`  
		Last Modified: Tue, 03 Mar 2026 22:44:35 GMT  
		Size: 13.0 KB (12951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f677fb1c0393ec126067b39b594fbefb0a680523bafa0967e85228b8469f03ae`  
		Last Modified: Tue, 03 Mar 2026 22:44:35 GMT  
		Size: 2.7 MB (2667661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:kernel-slim-java8-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:ce4232a70345a795eaf3f2ca707549f9041a4360f4de8b1b9d2b981f03b86237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3380659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26d39053fdf2f50d009b5d29d817992bc18dec9a0103d2f8055b9835b8d512c`

```dockerfile
```

-	Layers:
	-	`sha256:e367424fcd7bea81031981b4ba32d5f8f2a144f84923001d7431bbc445a4f58f`  
		Last Modified: Tue, 03 Mar 2026 22:44:34 GMT  
		Size: 3.3 MB (3340822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10115ab09cb3f747db775e6c9d7eb7ed430ce869f66b8107bea05b9d4ee2d157`  
		Last Modified: Tue, 03 Mar 2026 22:44:34 GMT  
		Size: 39.8 KB (39837 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:kernel-slim-java8-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:a430bd2912c5436b2f23a4def2085507f803098ec87cd3ea0c94a1112f6e2584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.1 MB (119091494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607c703d5aaac85b66eaa06b046664b1629100c9a5313b82c69a6c30eff09e1b`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:51 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:51 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:52 GMT
ADD file:be1799101a7a15f881e3aebea1e86fa6a156760dc7688b1affe179e948814a3b in / 
# Tue, 10 Feb 2026 16:50:52 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:17:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:17:22 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:17:22 GMT
ENV JAVA_VERSION=jdk8u482-b08.1_openj9-0.57.0
# Tue, 03 Mar 2026 20:12:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='d8fcad671559ab383d55d331db6725a5957f110faffe17d766c7ca3b14e71abd';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_aarch64_linux_8.0.482.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='4b66859a60b250db44e6fe3b8bd8cb5f3908be50315bad0e946961c7ac03a59a';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_ppc64le_linux_8.0.482.1.tar.gz';          ;;        amd64|x86_64)          ESUM='0bf81e496b5fed8669fc5b624ba7fb45fe05d7b9c19485f441ab48d2edad68fe';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_x64_linux_8.0.482.1.tar.gz';          ;;        s390x)          ESUM='a91c33d74cc5a0826f56efe48aa2f1223c6e25189a6bb8a8444e6f67b2581765';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_s390x_linux_8.0.482.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 03 Mar 2026 20:12:15 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Mar 2026 20:12:15 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 03 Mar 2026 20:13:19 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 03 Mar 2026 21:11:24 GMT
USER root
# Tue, 03 Mar 2026 21:11:24 GMT
ARG LIBERTY_VERSION=26.0.0.2
# Tue, 03 Mar 2026 21:11:24 GMT
ARG LIBERTY_SHA=7264724ce8ed2514f0586e10d43ed3c1bb7ff26f
# Tue, 03 Mar 2026 21:11:24 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.2/openliberty-kernel-26.0.0.2.zip
# Tue, 03 Mar 2026 21:11:24 GMT
ARG LIBERTY_BUILD_LABEL=cl260220260207-1901
# Tue, 03 Mar 2026 21:11:24 GMT
ARG OPENJ9_SCC=true
# Tue, 03 Mar 2026 21:11:24 GMT
ARG VERBOSE=false
# Tue, 03 Mar 2026 21:11:24 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260220260207-1901 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=26.0.0.2 liberty.version=26.0.0.2 io.openliberty.version=26.0.0.2
# Tue, 03 Mar 2026 21:11:24 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 03 Mar 2026 21:11:24 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 03 Mar 2026 21:11:24 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 03 Mar 2026 21:11:25 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=7264724ce8ed2514f0586e10d43ed3c1bb7ff26f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.2/openliberty-kernel-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 03 Mar 2026 21:11:34 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=7264724ce8ed2514f0586e10d43ed3c1bb7ff26f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.2/openliberty-kernel-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 03 Mar 2026 21:11:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 03 Mar 2026 21:11:34 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=7264724ce8ed2514f0586e10d43ed3c1bb7ff26f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.2/openliberty-kernel-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 03 Mar 2026 21:11:34 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=7264724ce8ed2514f0586e10d43ed3c1bb7ff26f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.2/openliberty-kernel-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Tue, 03 Mar 2026 21:11:41 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=7264724ce8ed2514f0586e10d43ed3c1bb7ff26f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.2/openliberty-kernel-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 03 Mar 2026 21:11:41 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 03 Mar 2026 21:11:41 GMT
USER 1001
# Tue, 03 Mar 2026 21:11:41 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 03 Mar 2026 21:11:41 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 03 Mar 2026 21:11:41 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:8b6ba492713239cba0554ce53d24405e1285684fa64bcfb05df4af8037ba5836`  
		Last Modified: Tue, 10 Feb 2026 17:42:12 GMT  
		Size: 29.9 MB (29909784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2ce3b2a70015000a5b0ceaa4885f1aceec67cb23d3ef542311e0f5506c39b0`  
		Last Modified: Tue, 17 Feb 2026 20:19:02 GMT  
		Size: 13.1 MB (13118433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619338c4c938f44748491da4f05dedfe89338ec466a3e37eca89f029c5ad514a`  
		Last Modified: Tue, 03 Mar 2026 20:13:46 GMT  
		Size: 53.4 MB (53424186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d481366c4d54c197a48cee1a2da27c0c8e73d9bbcb4f3c103128be1f1e41dc`  
		Last Modified: Tue, 03 Mar 2026 20:13:45 GMT  
		Size: 4.4 MB (4429846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66328dc7c25beb1cf4a004f0975a24bb4a334eef55998b80c64ec3a2e92fcd9`  
		Last Modified: Tue, 03 Mar 2026 21:11:55 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3054026ae2a1b5d55800ae92bb6eb87c7a1f62b72dc8f45af567e4ed2ea860`  
		Last Modified: Tue, 03 Mar 2026 21:11:55 GMT  
		Size: 11.8 KB (11814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f4281a5f41f02f2b039d4a2c2eec8fe27c29c776989a49808d8bd5cabfe90b`  
		Last Modified: Tue, 03 Mar 2026 21:11:56 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee53bb59d98194fd3823d1bb5f51e6d626eccce9ab0b49abdde21b5c0ddc107`  
		Last Modified: Tue, 03 Mar 2026 21:11:56 GMT  
		Size: 33.1 KB (33113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d27fce8343d0f21c1f7a0a5edf0ee28dd43a313adc5fc52719156057be53df`  
		Last Modified: Tue, 03 Mar 2026 21:11:57 GMT  
		Size: 15.2 MB (15237280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26710bbb190737beeeff594fbff6b7d29e0ca09414514af27260584690928ad`  
		Last Modified: Tue, 03 Mar 2026 21:11:56 GMT  
		Size: 739.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265aa03943e94828e7af5c1976f8b4fd2711c72e622ff058e8c60e12b3a101f9`  
		Last Modified: Tue, 03 Mar 2026 21:11:57 GMT  
		Size: 12.9 KB (12921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8920572614efe12da89c5b5aeab7882e132cd373b43eb721c114acc4dedbbf49`  
		Last Modified: Tue, 03 Mar 2026 21:11:57 GMT  
		Size: 2.9 MB (2912095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:kernel-slim-java8-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:3a345bfe05bdcfb31af964593c9aacb7a00528a502bfd463565a9fb2e7abbcdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3377431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c404ac5596037d5a86cc1fec3cbea18046bc4d9d63402c0a4d4ee4850e4fc8`

```dockerfile
```

-	Layers:
	-	`sha256:5206ff66d89fd3989be921bb6f30de97083dc08e5765daa79e1ae8e936b72e5f`  
		Last Modified: Tue, 03 Mar 2026 21:11:56 GMT  
		Size: 3.3 MB (3337641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4a84fcb4641393bc885e996ec0e0610c1766933d53e45b38e2e40789c5d12c2`  
		Last Modified: Tue, 03 Mar 2026 21:11:55 GMT  
		Size: 39.8 KB (39790 bytes)  
		MIME: application/vnd.in-toto+json
