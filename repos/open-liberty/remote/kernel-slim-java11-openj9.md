## `open-liberty:kernel-slim-java11-openj9`

```console
$ docker pull open-liberty@sha256:7bf432cc046865c3b38d71b6b1e050a701073400c4f2b502b7b55d56d0a293dd
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

### `open-liberty:kernel-slim-java11-openj9` - linux; amd64

```console
$ docker pull open-liberty@sha256:29f746b140ea8667bb59c01e0dee6fd485c7ba3e6e674575bc0e180aabb49e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119611320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5754abf5af0c47690c7e941c2f16f1cae587c8c9f669714bf9350525cc6ef992`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 29 Sep 2025 16:59:55 GMT
ARG RELEASE
# Mon, 29 Sep 2025 16:59:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Sep 2025 16:59:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Sep 2025 16:59:55 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 29 Sep 2025 16:59:55 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Mon, 29 Sep 2025 16:59:55 GMT
CMD ["/bin/bash"]
# Mon, 29 Sep 2025 16:59:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Sep 2025 16:59:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_VERSION=jdk-11.0.28+6_openj9-0.53.0
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4f4fe23f89ff85bf3715ec5fed8ef7e93699308ee57297bd8934cfa6675b14c9';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_aarch64_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='36670add16de97abf89151d8adeea0990c4148bf36ea130e5bf97fb6d1020247';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_ppc64le_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='690d72d2662eba4a6c1ad04a99d1557e36d86d58e9a5cba60597ae393ba8ef26';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_x64_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='a7d40e586d08746a4373ba77b72344c4122cf30ed1b3a792d33d6cf6e5c96aee';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_s390x_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7";     TOMCAT_VERSION="9.0.109";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
USER root
# Thu, 09 Oct 2025 13:17:23 GMT
ARG LIBERTY_VERSION=25.0.0.10
# Thu, 09 Oct 2025 13:17:23 GMT
ARG LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca
# Thu, 09 Oct 2025 13:17:23 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip
# Thu, 09 Oct 2025 13:17:23 GMT
ARG LIBERTY_BUILD_LABEL=cl251020250923-1355
# Thu, 09 Oct 2025 13:17:23 GMT
ARG OPENJ9_SCC=true
# Thu, 09 Oct 2025 13:17:23 GMT
ARG VERBOSE=false
# Thu, 09 Oct 2025 13:17:23 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251020250923-1355 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.10 liberty.version=25.0.0.10 io.openliberty.version=25.0.0.10
# Thu, 09 Oct 2025 13:17:23 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
COPY helpers /opt/ol/helpers # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 09 Oct 2025 13:17:23 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 09 Oct 2025 13:17:23 GMT
USER 1001
# Thu, 09 Oct 2025 13:17:23 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 09 Oct 2025 13:17:23 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 09 Oct 2025 13:17:23 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591ada44228002b3c6361204e28e11424c5abd9ba0b21d0a7d3a5f63c89fa186`  
		Last Modified: Thu, 02 Oct 2025 05:06:59 GMT  
		Size: 12.2 MB (12171658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b35eabc2bd9a153176051e03f9dbf7a280fa4d750abe2531b222e8f0558b34d`  
		Last Modified: Thu, 02 Oct 2025 05:07:03 GMT  
		Size: 55.8 MB (55756677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31155da32fa7cabe438222eff20d9abc6f89b6c63b737514babfd60950f86af4`  
		Last Modified: Thu, 02 Oct 2025 05:06:59 GMT  
		Size: 4.4 MB (4401529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f745244106b68a34bde2117dd2609925c381d5bef644278e43f9775c0e6e49`  
		Last Modified: Thu, 16 Oct 2025 00:41:38 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6965ec52c3307cd8e301077792679bf0a7580a56b3c9cd8ec651a0fc9a5383`  
		Last Modified: Thu, 16 Oct 2025 00:41:38 GMT  
		Size: 12.1 KB (12106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0b53f4e42b468c7495752ed269f541d30ad973304d557cdff8844d63747732`  
		Last Modified: Thu, 16 Oct 2025 00:41:38 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df427d638a770a5c71b8d460905e28d8a46ba7a98dcf9b013636f323d19b1fd`  
		Last Modified: Thu, 16 Oct 2025 00:41:38 GMT  
		Size: 31.7 KB (31748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531090ab6c4edcd773c1f58b61305dccd2e0a3b5234b0e638d5f2e3ffde69490`  
		Last Modified: Thu, 16 Oct 2025 00:41:40 GMT  
		Size: 14.9 MB (14868345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d183a6b167aab9c0085035389b996f383bab67295850d9be71e47200592d126`  
		Last Modified: Thu, 16 Oct 2025 00:41:38 GMT  
		Size: 737.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ca9e1298d616989861efa120fde65b5208c157b8180d1b38aea6273e620190`  
		Last Modified: Thu, 16 Oct 2025 00:41:38 GMT  
		Size: 13.2 KB (13208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3755e47d6a870895ad9198221c5961e88789bb33b091d8efdf7ce4a74b4e1fc7`  
		Last Modified: Thu, 16 Oct 2025 00:41:38 GMT  
		Size: 2.8 MB (2817201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:kernel-slim-java11-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:90677582aaa9e8da71922ec19ab339cfd0a0d7ddb5380ef18930b97e3610fe0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3920003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cbdda537f17b6c1bc63ff85f6ad05e2cd5e34c946e551eb78d1b83d13a90aca`

```dockerfile
```

-	Layers:
	-	`sha256:02f1d8722e02830d7062ddec831e0cbfa17016ac1047fbff13bbe5345f215c11`  
		Last Modified: Thu, 16 Oct 2025 02:46:26 GMT  
		Size: 3.9 MB (3880466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ae1529da8227db3521a6391a74e9b1ce322ff607f13977cc7a0acafca05e525`  
		Last Modified: Thu, 16 Oct 2025 02:46:26 GMT  
		Size: 39.5 KB (39537 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:kernel-slim-java11-openj9` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:09e04e5a634bc17fb0a79187f2c9e5279df5d0df0c63dea5440164722edb7851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115363667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7229ff42bd1c24069943bef603fdcb7020078833fa89352d02fe98410e6aeb4e`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 29 Sep 2025 16:59:55 GMT
ARG RELEASE
# Mon, 29 Sep 2025 16:59:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Sep 2025 16:59:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Sep 2025 16:59:55 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 29 Sep 2025 16:59:55 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Mon, 29 Sep 2025 16:59:55 GMT
CMD ["/bin/bash"]
# Mon, 29 Sep 2025 16:59:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Sep 2025 16:59:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_VERSION=jdk-11.0.28+6_openj9-0.53.0
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4f4fe23f89ff85bf3715ec5fed8ef7e93699308ee57297bd8934cfa6675b14c9';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_aarch64_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='36670add16de97abf89151d8adeea0990c4148bf36ea130e5bf97fb6d1020247';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_ppc64le_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='690d72d2662eba4a6c1ad04a99d1557e36d86d58e9a5cba60597ae393ba8ef26';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_x64_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='a7d40e586d08746a4373ba77b72344c4122cf30ed1b3a792d33d6cf6e5c96aee';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_s390x_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7";     TOMCAT_VERSION="9.0.109";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
USER root
# Thu, 09 Oct 2025 13:17:23 GMT
ARG LIBERTY_VERSION=25.0.0.10
# Thu, 09 Oct 2025 13:17:23 GMT
ARG LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca
# Thu, 09 Oct 2025 13:17:23 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip
# Thu, 09 Oct 2025 13:17:23 GMT
ARG LIBERTY_BUILD_LABEL=cl251020250923-1355
# Thu, 09 Oct 2025 13:17:23 GMT
ARG OPENJ9_SCC=true
# Thu, 09 Oct 2025 13:17:23 GMT
ARG VERBOSE=false
# Thu, 09 Oct 2025 13:17:23 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251020250923-1355 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.10 liberty.version=25.0.0.10 io.openliberty.version=25.0.0.10
# Thu, 09 Oct 2025 13:17:23 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
COPY helpers /opt/ol/helpers # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 09 Oct 2025 13:17:23 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 09 Oct 2025 13:17:23 GMT
USER 1001
# Thu, 09 Oct 2025 13:17:23 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 09 Oct 2025 13:17:23 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 09 Oct 2025 13:17:23 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0901b492a72eb5c61bc854697c0b53198a3079d3ba0817b8fd6b6da1a1cb6a`  
		Last Modified: Thu, 02 Oct 2025 01:22:20 GMT  
		Size: 12.1 MB (12129478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec35fa45ef05436ca82ff65b4205d76d43c136ad011174f0f1aaa46fc0b289e`  
		Last Modified: Thu, 02 Oct 2025 01:22:21 GMT  
		Size: 54.0 MB (54012661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b65735b5ab398c2a7c68a972c24c935acec05eb15dbd5e5fd5b7a6ae91fab0`  
		Last Modified: Thu, 02 Oct 2025 01:22:19 GMT  
		Size: 4.2 MB (4172712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e748a51791d94f99c893bf6cff56e5babb0a62d4150432330a7c462e040e75c4`  
		Last Modified: Thu, 16 Oct 2025 00:41:47 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898b91820aa53490c11838770ac9ca6c1399208d5e9b3bceae280af5be803fff`  
		Last Modified: Thu, 16 Oct 2025 00:41:47 GMT  
		Size: 12.1 KB (12102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3bdaf7cc4c745371229d5ca3b605915c59a07c72a15908d81d02ca49ab9f72`  
		Last Modified: Thu, 16 Oct 2025 00:41:48 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9a5061de687e88cb1669e74ec09d2a0de6e0985c0fc5c710235121f5cfc616`  
		Last Modified: Thu, 16 Oct 2025 00:41:48 GMT  
		Size: 42.3 KB (42324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd79c0000cf8b614b929d4d64bcd79cb685a79642c86de9c2c9d314eb8a2c0c`  
		Last Modified: Thu, 16 Oct 2025 00:41:51 GMT  
		Size: 14.9 MB (14868556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c314b3ffa2b1a690fc083d5ee4426f3e21b46d9973afe57379df36d7dce663`  
		Last Modified: Thu, 16 Oct 2025 00:41:48 GMT  
		Size: 738.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f6e2203e5371664c4e4b02180ca5aab2ed9317e8f0c07b9005097ff6430a05`  
		Last Modified: Thu, 16 Oct 2025 00:41:49 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0c72a3485c44f323ec99bea43a7bd25253b62c061d0aabc485549a5b424d61`  
		Last Modified: Thu, 16 Oct 2025 00:41:50 GMT  
		Size: 2.7 MB (2727495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:kernel-slim-java11-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:a43afac592dfdc70c9edcc1d7288d214c41159832de3b78faddb54c06da6ab52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3918514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b62f151b560d865513cf56fe6dfb31e5d53339febc52644cea8dc9ee6c8b7c0`

```dockerfile
```

-	Layers:
	-	`sha256:5deb5212a4ec243995ade38b8e1a8812a19eb111267e7db4229cea7516729c2c`  
		Last Modified: Thu, 16 Oct 2025 02:46:30 GMT  
		Size: 3.9 MB (3878838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:244e7a04ee9ba954750834342c1e3de9ea20606f829dac9b2ae8df9c03ec2396`  
		Last Modified: Thu, 16 Oct 2025 02:46:31 GMT  
		Size: 39.7 KB (39676 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:kernel-slim-java11-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:b5961a8deb935903fce86469c847f5bdeee2e429400ed1c4d5892cfd50022a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.1 MB (126057032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17580abfa6ab0f2af6bff52f6c9fcb131a43d2f220ff7f7328ae4d6c8d790a51`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 29 Sep 2025 16:59:55 GMT
ARG RELEASE
# Mon, 29 Sep 2025 16:59:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Sep 2025 16:59:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Sep 2025 16:59:55 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 29 Sep 2025 16:59:55 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Mon, 29 Sep 2025 16:59:55 GMT
CMD ["/bin/bash"]
# Mon, 29 Sep 2025 16:59:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Sep 2025 16:59:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_VERSION=jdk-11.0.28+6_openj9-0.53.0
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4f4fe23f89ff85bf3715ec5fed8ef7e93699308ee57297bd8934cfa6675b14c9';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_aarch64_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='36670add16de97abf89151d8adeea0990c4148bf36ea130e5bf97fb6d1020247';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_ppc64le_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='690d72d2662eba4a6c1ad04a99d1557e36d86d58e9a5cba60597ae393ba8ef26';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_x64_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='a7d40e586d08746a4373ba77b72344c4122cf30ed1b3a792d33d6cf6e5c96aee';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_s390x_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7";     TOMCAT_VERSION="9.0.109";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
USER root
# Thu, 09 Oct 2025 13:17:23 GMT
ARG LIBERTY_VERSION=25.0.0.10
# Thu, 09 Oct 2025 13:17:23 GMT
ARG LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca
# Thu, 09 Oct 2025 13:17:23 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip
# Thu, 09 Oct 2025 13:17:23 GMT
ARG LIBERTY_BUILD_LABEL=cl251020250923-1355
# Thu, 09 Oct 2025 13:17:23 GMT
ARG OPENJ9_SCC=true
# Thu, 09 Oct 2025 13:17:23 GMT
ARG VERBOSE=false
# Thu, 09 Oct 2025 13:17:23 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251020250923-1355 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.10 liberty.version=25.0.0.10 io.openliberty.version=25.0.0.10
# Thu, 09 Oct 2025 13:17:23 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
COPY helpers /opt/ol/helpers # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 09 Oct 2025 13:17:23 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 09 Oct 2025 13:17:23 GMT
USER 1001
# Thu, 09 Oct 2025 13:17:23 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 09 Oct 2025 13:17:23 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 09 Oct 2025 13:17:23 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f986968cada567143a317eb39ea1ab589db364ae569c4ecbd454ac3aa78be10`  
		Last Modified: Thu, 02 Oct 2025 03:15:18 GMT  
		Size: 12.9 MB (12893853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dda16e149f420b4adb54c553d658e20b43e7e0594baeb0f838de086f97861eb`  
		Last Modified: Thu, 02 Oct 2025 02:01:01 GMT  
		Size: 57.6 MB (57604802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d6f5e032c277f974c3e6617c6f80e00194ddac18e7cb2bf6457983a7c5bb55`  
		Last Modified: Thu, 02 Oct 2025 02:00:58 GMT  
		Size: 3.5 MB (3506823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7be3a3daefb5c68000b4fa96b1fb88c37d368c2d818b321ee5e959097617bdb`  
		Last Modified: Thu, 16 Oct 2025 00:45:44 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc0913d2d8f708756f6513ba133901fdff8af03d88656416c0a98747fe9bbc6`  
		Last Modified: Thu, 16 Oct 2025 00:51:23 GMT  
		Size: 12.1 KB (12106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd4454d2860fb74343157a20079f597411fa62119cd3c68b32e548c09f2f13c`  
		Last Modified: Thu, 16 Oct 2025 00:51:23 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a95c515802ec2f406c1330450739c54c763230df799ec0c38d8e441facd5582`  
		Last Modified: Thu, 16 Oct 2025 00:51:23 GMT  
		Size: 36.5 KB (36502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc92a9d035a930ce718d5eee53c2d34ba99b714238478e71954a1abe0dff4dfa`  
		Last Modified: Thu, 16 Oct 2025 00:51:25 GMT  
		Size: 14.9 MB (14868711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3321bba0169c9cbfa7b43687f723a4cde26326de43b8a577bd76cc3c507ee5a1`  
		Last Modified: Thu, 16 Oct 2025 00:51:23 GMT  
		Size: 736.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543f3ba0b16198cef13b9cb6c2bd8e063b576522a78eb083b9a7281772ffcdc3`  
		Last Modified: Thu, 16 Oct 2025 00:51:23 GMT  
		Size: 13.2 KB (13233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d58a0680ce8c42417c74096f53083bed1b546b67db4680f271933281fc1d01e`  
		Last Modified: Thu, 16 Oct 2025 00:51:23 GMT  
		Size: 2.7 MB (2672180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:kernel-slim-java11-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:dfecb9c07e9bed407038fedf96870591abaa732f192e81e332bcf6157480eb9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3924670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5740a9a8d207b7cfdf49b7275147c1b1144e2c2cead2ef42ec5fe4275ff5312d`

```dockerfile
```

-	Layers:
	-	`sha256:34c9881b6cacf0f01cd7f401ca51fc7a388d20305ce51b61f503cc1144075c0d`  
		Last Modified: Thu, 16 Oct 2025 02:46:35 GMT  
		Size: 3.9 MB (3885093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b5e7d923444433130460b69bf7edc0cbe280db98f2bd3529820e5b9d6616751`  
		Last Modified: Thu, 16 Oct 2025 02:46:35 GMT  
		Size: 39.6 KB (39577 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:kernel-slim-java11-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:d717bba13634943991597d299c98fc70c4970b70e704ac45451c500373a2cf91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116837211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31d4d60fbf88ff8a9baf262c7b4f53e607f7ac0df87a5b75de813b93cd7f503e`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 29 Sep 2025 16:59:55 GMT
ARG RELEASE
# Mon, 29 Sep 2025 16:59:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Sep 2025 16:59:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Sep 2025 16:59:55 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 29 Sep 2025 16:59:55 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Mon, 29 Sep 2025 16:59:55 GMT
CMD ["/bin/bash"]
# Mon, 29 Sep 2025 16:59:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Sep 2025 16:59:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_VERSION=jdk-11.0.28+6_openj9-0.53.0
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4f4fe23f89ff85bf3715ec5fed8ef7e93699308ee57297bd8934cfa6675b14c9';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_aarch64_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='36670add16de97abf89151d8adeea0990c4148bf36ea130e5bf97fb6d1020247';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_ppc64le_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='690d72d2662eba4a6c1ad04a99d1557e36d86d58e9a5cba60597ae393ba8ef26';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_x64_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='a7d40e586d08746a4373ba77b72344c4122cf30ed1b3a792d33d6cf6e5c96aee';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_s390x_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7";     TOMCAT_VERSION="9.0.109";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
USER root
# Thu, 09 Oct 2025 13:17:23 GMT
ARG LIBERTY_VERSION=25.0.0.10
# Thu, 09 Oct 2025 13:17:23 GMT
ARG LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca
# Thu, 09 Oct 2025 13:17:23 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip
# Thu, 09 Oct 2025 13:17:23 GMT
ARG LIBERTY_BUILD_LABEL=cl251020250923-1355
# Thu, 09 Oct 2025 13:17:23 GMT
ARG OPENJ9_SCC=true
# Thu, 09 Oct 2025 13:17:23 GMT
ARG VERBOSE=false
# Thu, 09 Oct 2025 13:17:23 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251020250923-1355 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.10 liberty.version=25.0.0.10 io.openliberty.version=25.0.0.10
# Thu, 09 Oct 2025 13:17:23 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
COPY helpers /opt/ol/helpers # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 09 Oct 2025 13:17:23 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Thu, 09 Oct 2025 13:17:23 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 09 Oct 2025 13:17:23 GMT
USER 1001
# Thu, 09 Oct 2025 13:17:23 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 09 Oct 2025 13:17:23 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 09 Oct 2025 13:17:23 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:e4a5a322dd65d010805129ca793d5d5e6b07872cbc2f41d566a84091b39c794e`  
		Last Modified: Thu, 02 Oct 2025 00:25:04 GMT  
		Size: 28.0 MB (28003413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e783d3ecc7650f1487649a3d3acaf91cf431f4d1c5824fec7b102501fe16e7be`  
		Last Modified: Thu, 02 Oct 2025 03:16:37 GMT  
		Size: 12.2 MB (12219551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdac61a1da7eb8e47a7ba212109e5b9bf1a1b6cc5b4b53b35ec34a740f321cc8`  
		Last Modified: Thu, 02 Oct 2025 01:38:58 GMT  
		Size: 54.3 MB (54330698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b088b15ee266a9dfba32ef1803e0a01b781b18f92b450ff28d851202122287e6`  
		Last Modified: Thu, 02 Oct 2025 01:38:55 GMT  
		Size: 4.6 MB (4594966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f071548dda7d78ab055b282dab9208bca59475ec13b910f94265474e9c72ad`  
		Last Modified: Thu, 16 Oct 2025 01:18:22 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0606542746e9bd5c154b218704dbe8c91b98d873c36e2bea43e3d6587114e6ac`  
		Last Modified: Thu, 16 Oct 2025 00:49:11 GMT  
		Size: 12.1 KB (12108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518c91e573a1a35e7b04472c7391f32acd60491510e159d819e820418afd02e1`  
		Last Modified: Thu, 16 Oct 2025 00:49:11 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0d23397c60597c04245abc2c432c7cdbd0ec1a013f33d444410445eb04c2ff`  
		Last Modified: Thu, 16 Oct 2025 00:49:13 GMT  
		Size: 33.1 KB (33112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c66bf923910354ec879cfb5c6e4afb7167b14915d257a3206ef9bf8eec3ca8e`  
		Last Modified: Thu, 16 Oct 2025 00:49:15 GMT  
		Size: 14.9 MB (14868060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3eef8d7fa9ed137e2a40b6432dabb6e5138fe1d90d332bff7ec88d797e922a`  
		Last Modified: Thu, 16 Oct 2025 00:49:13 GMT  
		Size: 739.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ecafb931ed1e27a2ca9d7be900f012c96f437ce7e2f3f925754eb49a878f2d`  
		Last Modified: Thu, 16 Oct 2025 00:49:13 GMT  
		Size: 13.2 KB (13213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5ed2b6af4440f51878491ce3f5d97d971f9a08bb63c6a58a8c397241714bed`  
		Last Modified: Thu, 16 Oct 2025 00:49:14 GMT  
		Size: 2.8 MB (2760054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:kernel-slim-java11-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:5c2ddffdb50753fc03dcdddfdd17af1faad12752bb85150a241b0e4ad6642186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2fdca0c7b732c1abe5d7bce4e066387990474abe3f5da0018b20a5a0b1e100`

```dockerfile
```

-	Layers:
	-	`sha256:efc1dceae42ce41514cd55626cb30b4e82e48c8ea5ce4af1e001cb3c5d734d85`  
		Last Modified: Thu, 16 Oct 2025 02:46:41 GMT  
		Size: 3.9 MB (3881483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92e37d7ab119a9f766e5f20386252987ac53cbc644c68b53041142e11d7f3b7a`  
		Last Modified: Thu, 16 Oct 2025 02:46:41 GMT  
		Size: 39.5 KB (39536 bytes)  
		MIME: application/vnd.in-toto+json
