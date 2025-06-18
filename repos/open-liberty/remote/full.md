## `open-liberty:full`

```console
$ docker pull open-liberty@sha256:bd524f31f067b1f71bb9322bd4aef1f4ebe09050f70b6ce8747f1750b0ab2621
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

### `open-liberty:full` - linux; amd64

```console
$ docker pull open-liberty@sha256:fb4ff56685e051aef38778f9d23407baead58185844db675a71cbbf7ba237488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.2 MB (447221451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb3b418b882079c4f16c8ebd2feb5ccce3f58d6c94f3cc7035ad9f834903b37`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Tue, 17 Jun 2025 14:26:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Jun 2025 14:26:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_VERSION=jdk8u452-b09_openj9-0.51.0
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='89cf44e225cb1daa274e805a615f59bb0140dbd4bddcfbe4cecc12dd8c3a9fed';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='59b6b66a14f4c264e81aca7a35339fc2eb907211a1953d61c44c9882fa79153c';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='0ac75bf18399ece85749ebf63f1fd6210daa63f6df595205edcc7a45400ba13c';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='512b7127dce034ee0e0430e11ddcf25c91bbe4356d66c5e4ede311be7fbca16d';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956";     TOMCAT_VERSION="9.0.105";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
USER root
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_VERSION=25.0.0.6
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_SHA=a26724573f5c4f04fb9a39706a715e6bb85490c6
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.6/openliberty-runtime-25.0.0.6.zip
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_BUILD_LABEL=cl250620250602-1102
# Tue, 17 Jun 2025 15:25:00 GMT
ARG OPENJ9_SCC=true
# Tue, 17 Jun 2025 15:25:00 GMT
ARG VERBOSE=false
# Tue, 17 Jun 2025 15:25:00 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250620250602-1102 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.6 liberty.version=25.0.0.6 io.openliberty.version=25.0.0.6
# Tue, 17 Jun 2025 15:25:00 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=a26724573f5c4f04fb9a39706a715e6bb85490c6 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.6/openliberty-runtime-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=a26724573f5c4f04fb9a39706a715e6bb85490c6 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.6/openliberty-runtime-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=a26724573f5c4f04fb9a39706a715e6bb85490c6 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.6/openliberty-runtime-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=a26724573f5c4f04fb9a39706a715e6bb85490c6 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.6/openliberty-runtime-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=a26724573f5c4f04fb9a39706a715e6bb85490c6 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.6/openliberty-runtime-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 17 Jun 2025 15:25:00 GMT
USER 1001
# Tue, 17 Jun 2025 15:25:00 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 17 Jun 2025 15:25:00 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 17 Jun 2025 15:25:00 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c1d839f35e48aa488dd92ad8c2526a2933d83c324d647f298bf3630a573d35e`  
		Last Modified: Tue, 17 Jun 2025 17:12:18 GMT  
		Size: 12.2 MB (12172061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ba0181ecf4c7eba4c29e9a7cb04dae1a68155e9a642dd19f05fb33eb050f01`  
		Last Modified: Tue, 17 Jun 2025 17:12:21 GMT  
		Size: 50.5 MB (50498637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3971a3b7eb370e4b8c4facd79e482a0f33ac3ce0503db7ddc5818b21a86a7a0`  
		Last Modified: Tue, 17 Jun 2025 17:12:18 GMT  
		Size: 4.3 MB (4316220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5dfdeb467f7c3e3a49066a51f2213340d1392a5a7a53a8da4a1d9e8e2d35fe8`  
		Last Modified: Tue, 17 Jun 2025 22:34:53 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa967c170f19b20e386a0227de170a5f1ae5ab73953c149725687048c8dc1a5`  
		Last Modified: Tue, 17 Jun 2025 22:34:52 GMT  
		Size: 12.5 KB (12461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e43a0e699471cefe4d8d782a053a463b0dc6338dcbb9cb51f23c1b52bda4959`  
		Last Modified: Tue, 17 Jun 2025 22:34:52 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b01c9ad2017feb1381560e628dff26d9a8d7b366d0fa3dd2ddc17447623107`  
		Last Modified: Tue, 17 Jun 2025 22:34:52 GMT  
		Size: 31.7 KB (31742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e87ed312023043bbec9a4ef0ae609bb1c2d9a2f62e78b087bb3170b67e3c70b`  
		Last Modified: Wed, 18 Jun 2025 01:24:03 GMT  
		Size: 337.2 MB (337197493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566eb66ccc86f897ae187ec27adcf15af3bf4b9aeed20a3d4405bc22d12eedee`  
		Last Modified: Tue, 17 Jun 2025 22:34:52 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0ec272b4525616769ecbff6bcdc163418bc539c7f13facb587ef885175be28`  
		Last Modified: Tue, 17 Jun 2025 22:34:53 GMT  
		Size: 13.9 KB (13857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b915eb333c1cf09df94f0366a79de55cba2bdc11ced2b4db8abd464e7437489`  
		Last Modified: Tue, 17 Jun 2025 22:34:54 GMT  
		Size: 13.4 MB (13443629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full` - unknown; unknown

```console
$ docker pull open-liberty@sha256:a2d5415c6bd96d06b2318f30a4a01983c400ac183b0070c1d17d78d4c75a748d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5751448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecac923979cc971fa246d5b4e1d658c8863e372cf8af20899fe1e32690b56ef2`

```dockerfile
```

-	Layers:
	-	`sha256:6385843b8e790886d85824a2693b15efeee0002414417e30655c0c7820fcab40`  
		Last Modified: Tue, 17 Jun 2025 23:48:23 GMT  
		Size: 5.7 MB (5712028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b66db6526d0f4d107dc7dab441daa6aceca8df72bf605c58b4b6aa74dd3a5265`  
		Last Modified: Tue, 17 Jun 2025 23:48:24 GMT  
		Size: 39.4 KB (39420 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:542d75084a1b7cad3d9ce9d0fff55022fa32e8667b72d25e6e0e7c36482334eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **443.8 MB (443755795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:647aff8950995f5c9f4f282142d04e5676b47916a05bfa31db1c1f4c8a0f7311`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Tue, 17 Jun 2025 14:26:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Jun 2025 14:26:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_VERSION=jdk8u452-b09_openj9-0.51.0
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='89cf44e225cb1daa274e805a615f59bb0140dbd4bddcfbe4cecc12dd8c3a9fed';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='59b6b66a14f4c264e81aca7a35339fc2eb907211a1953d61c44c9882fa79153c';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='0ac75bf18399ece85749ebf63f1fd6210daa63f6df595205edcc7a45400ba13c';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='512b7127dce034ee0e0430e11ddcf25c91bbe4356d66c5e4ede311be7fbca16d';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956";     TOMCAT_VERSION="9.0.105";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
USER root
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_VERSION=25.0.0.6
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_SHA=a26724573f5c4f04fb9a39706a715e6bb85490c6
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.6/openliberty-runtime-25.0.0.6.zip
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_BUILD_LABEL=cl250620250602-1102
# Tue, 17 Jun 2025 15:25:00 GMT
ARG OPENJ9_SCC=true
# Tue, 17 Jun 2025 15:25:00 GMT
ARG VERBOSE=false
# Tue, 17 Jun 2025 15:25:00 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250620250602-1102 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.6 liberty.version=25.0.0.6 io.openliberty.version=25.0.0.6
# Tue, 17 Jun 2025 15:25:00 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=a26724573f5c4f04fb9a39706a715e6bb85490c6 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.6/openliberty-runtime-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=a26724573f5c4f04fb9a39706a715e6bb85490c6 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.6/openliberty-runtime-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=a26724573f5c4f04fb9a39706a715e6bb85490c6 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.6/openliberty-runtime-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=a26724573f5c4f04fb9a39706a715e6bb85490c6 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.6/openliberty-runtime-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=a26724573f5c4f04fb9a39706a715e6bb85490c6 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.6/openliberty-runtime-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 17 Jun 2025 15:25:00 GMT
USER 1001
# Tue, 17 Jun 2025 15:25:00 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 17 Jun 2025 15:25:00 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 17 Jun 2025 15:25:00 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbff14187feb7082a330fc6604f5d950114fba77a27a3564014bdeb0c0a7e399`  
		Last Modified: Tue, 17 Jun 2025 17:39:17 GMT  
		Size: 12.1 MB (12129302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e715985617e74aadaa3f006a1e13df6bb2c624e67cec932b6be82ac608308a41`  
		Last Modified: Tue, 17 Jun 2025 20:47:27 GMT  
		Size: 49.9 MB (49934833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b27401a0481420071070da108a6a0a0d5d0f5a29dea23bb3c763c01afdaa27`  
		Last Modified: Tue, 17 Jun 2025 18:16:43 GMT  
		Size: 4.0 MB (4043887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2a5ea3bed843c68b10ee247bde1ba9c9df6552f821c16aad5834a49f351a6d`  
		Last Modified: Tue, 17 Jun 2025 18:09:39 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f5c1191149a3c9729e29808ee772299eff05c3c9ebfdb434207e4e402cd536`  
		Last Modified: Tue, 17 Jun 2025 22:34:35 GMT  
		Size: 12.5 KB (12468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4449eeae57d6abbba4a5e3b9a48bfb1981060e8771954491d030affcdd4e024d`  
		Last Modified: Tue, 17 Jun 2025 22:34:35 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6540c6cab8ce0f93768ea0251a83c56ba0e64e8c57b36f4f73d618e49985a7f9`  
		Last Modified: Tue, 17 Jun 2025 22:41:16 GMT  
		Size: 42.3 KB (42324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c662950ee7526a060202e87fd4cdbcedd38010b6ac60edbae8f113d6926379`  
		Last Modified: Wed, 18 Jun 2025 00:11:05 GMT  
		Size: 337.2 MB (337197537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3556279128a75d0e29ea8ff7fe5a610b8c2a3923a6a15bdad464088dea0a4d7f`  
		Last Modified: Tue, 17 Jun 2025 22:41:16 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99276c925c5eaa8f5912e05b402af05a5b1bf38ac9912344f9e13b4fc2a4a7a`  
		Last Modified: Tue, 17 Jun 2025 22:41:16 GMT  
		Size: 13.9 KB (13868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8181959f198740dce928d5b2399c8e89fa6696b9eea59635aa56792a28fbac2c`  
		Last Modified: Tue, 17 Jun 2025 22:41:17 GMT  
		Size: 13.0 MB (13023642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full` - unknown; unknown

```console
$ docker pull open-liberty@sha256:22b7e7d5752a9ece6ff1a77240fe83f5358b520f32437127ead626e344a0378d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5751416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ebbe5f8f47736fb81941a7498efbbcf9549b6edadce94e6dfd6ddc7a9fc673e`

```dockerfile
```

-	Layers:
	-	`sha256:be8ad0f8915c696ff59c0212e78f34e18791aa5539c28f3d61455507b0e143f2`  
		Last Modified: Tue, 17 Jun 2025 23:48:33 GMT  
		Size: 5.7 MB (5711844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0aef6dbeda4605c4bafe3926d1e8c8867bfe1855c34d2fa3ba5c0af92d87cea`  
		Last Modified: Tue, 17 Jun 2025 23:48:34 GMT  
		Size: 39.6 KB (39572 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:5328ec1ff2d07a24e70e4683bc17578435d25d088afe2e7a1c3216938c6540cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.8 MB (451823482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60055f4308322d05b49d4559e06c53be1cab485a241326f478df2fa398f70db`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 30 May 2025 22:33:39 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:39 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:43 GMT
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Fri, 30 May 2025 22:33:43 GMT
CMD ["/bin/bash"]
# Tue, 17 Jun 2025 14:26:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Jun 2025 14:26:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_VERSION=jdk8u452-b09_openj9-0.51.0
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='89cf44e225cb1daa274e805a615f59bb0140dbd4bddcfbe4cecc12dd8c3a9fed';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='59b6b66a14f4c264e81aca7a35339fc2eb907211a1953d61c44c9882fa79153c';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='0ac75bf18399ece85749ebf63f1fd6210daa63f6df595205edcc7a45400ba13c';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='512b7127dce034ee0e0430e11ddcf25c91bbe4356d66c5e4ede311be7fbca16d';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956";     TOMCAT_VERSION="9.0.105";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
USER root
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_VERSION=25.0.0.6
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_SHA=a26724573f5c4f04fb9a39706a715e6bb85490c6
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.6/openliberty-runtime-25.0.0.6.zip
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_BUILD_LABEL=cl250620250602-1102
# Tue, 17 Jun 2025 15:25:00 GMT
ARG OPENJ9_SCC=true
# Tue, 17 Jun 2025 15:25:00 GMT
ARG VERBOSE=false
# Tue, 17 Jun 2025 15:25:00 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250620250602-1102 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.6 liberty.version=25.0.0.6 io.openliberty.version=25.0.0.6
# Tue, 17 Jun 2025 15:25:00 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=a26724573f5c4f04fb9a39706a715e6bb85490c6 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.6/openliberty-runtime-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=a26724573f5c4f04fb9a39706a715e6bb85490c6 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.6/openliberty-runtime-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=a26724573f5c4f04fb9a39706a715e6bb85490c6 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.6/openliberty-runtime-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=a26724573f5c4f04fb9a39706a715e6bb85490c6 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.6/openliberty-runtime-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=a26724573f5c4f04fb9a39706a715e6bb85490c6 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.6/openliberty-runtime-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 17 Jun 2025 15:25:00 GMT
USER 1001
# Tue, 17 Jun 2025 15:25:00 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 17 Jun 2025 15:25:00 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 17 Jun 2025 15:25:00 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c0a1fca7ea07c8c5a127826c7981b2bbb00fab8901f776e93777f6b6e7e19f`  
		Last Modified: Tue, 17 Jun 2025 17:55:19 GMT  
		Size: 12.9 MB (12893311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f7686cc23870dc282918b8e5557c73348592e01a584a1eda1d981855a61167`  
		Last Modified: Tue, 17 Jun 2025 17:58:23 GMT  
		Size: 51.9 MB (51920024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bddb1dbea42de5d17dba8d8603245be2a430091847530cc1640c455719e6892a`  
		Last Modified: Tue, 17 Jun 2025 17:58:17 GMT  
		Size: 3.5 MB (3451926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcaca2a3d3381921aff9cd2acdeadafd79f74f076c2fb1237ab2fa051662ffd9`  
		Last Modified: Tue, 17 Jun 2025 18:19:44 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349f14576e95960e6cd6da1f78dbe07fc169c48160f344d1b306d033be238b1c`  
		Last Modified: Tue, 17 Jun 2025 22:36:00 GMT  
		Size: 12.5 KB (12467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618798d794bbe4071837e94d4ad34575ddf4286d4efd661a906e8f016e8b3379`  
		Last Modified: Tue, 17 Jun 2025 22:36:00 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0dacdec85493ddf6285b9416ea668eea2880e0ba46f4b7bcd145b65a3cf88e7`  
		Last Modified: Tue, 17 Jun 2025 22:46:44 GMT  
		Size: 36.5 KB (36497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714795de09f34618a252332a48c6993d4e8d1767b6e18988f8aa1beb0d964bc3`  
		Last Modified: Wed, 18 Jun 2025 00:11:33 GMT  
		Size: 337.2 MB (337197779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915ed3007f5427ad8235cf4d063cdcca7e75f36dbdaa7dd4cc3f77b512ba63ab`  
		Last Modified: Tue, 17 Jun 2025 22:46:44 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac7f6e70c702c506f32820a33d1d4ee731e0e40b0a99e1f8e689fc0f8d44325`  
		Last Modified: Tue, 17 Jun 2025 22:46:44 GMT  
		Size: 13.9 KB (13881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0237fcb63993c4bbd5f02a93e8706db7a2e6936226427363cd28f97601f9022`  
		Last Modified: Tue, 17 Jun 2025 22:46:45 GMT  
		Size: 11.9 MB (11854888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full` - unknown; unknown

```console
$ docker pull open-liberty@sha256:7acf52fe0c797690afd8dd0e1e7c5c18c4b17b370b2a127db90d0d5b71c6cbfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5756293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3edf49e80847116d58fac793cd17562b66b040c8f789900899c2fddd4ad5dd`

```dockerfile
```

-	Layers:
	-	`sha256:91cf279876560663076555a7d30c245cf7932fd2967c248bfc88c3621925a7b4`  
		Last Modified: Tue, 17 Jun 2025 23:48:41 GMT  
		Size: 5.7 MB (5716827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac22ecd6bb6756a0ce506740d68d7c8e3795328318638384388e604024f45cd5`  
		Last Modified: Tue, 17 Jun 2025 23:48:41 GMT  
		Size: 39.5 KB (39466 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full` - linux; s390x

```console
$ docker pull open-liberty@sha256:fd873dfde11a0a3e5932ef8ec557404fddb7fbbfe1a639312424a29f7dd154df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.8 MB (445829024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945b039552dd088cc043e7e2df8ad09a1b768deb98e6d7535c5d962aaa9f7a9a`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 30 May 2025 22:31:10 GMT
ARG RELEASE
# Fri, 30 May 2025 22:31:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:31:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:31:10 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:31:12 GMT
ADD file:f153a831e3d8b37cf290a0e64d208348b0231dc123ac8127decb555f982fe306 in / 
# Fri, 30 May 2025 22:31:12 GMT
CMD ["/bin/bash"]
# Tue, 17 Jun 2025 14:26:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Jun 2025 14:26:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_VERSION=jdk8u452-b09_openj9-0.51.0
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='89cf44e225cb1daa274e805a615f59bb0140dbd4bddcfbe4cecc12dd8c3a9fed';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='59b6b66a14f4c264e81aca7a35339fc2eb907211a1953d61c44c9882fa79153c';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='0ac75bf18399ece85749ebf63f1fd6210daa63f6df595205edcc7a45400ba13c';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='512b7127dce034ee0e0430e11ddcf25c91bbe4356d66c5e4ede311be7fbca16d';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956";     TOMCAT_VERSION="9.0.105";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
USER root
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_VERSION=25.0.0.6
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_SHA=a26724573f5c4f04fb9a39706a715e6bb85490c6
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.6/openliberty-runtime-25.0.0.6.zip
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_BUILD_LABEL=cl250620250602-1102
# Tue, 17 Jun 2025 15:25:00 GMT
ARG OPENJ9_SCC=true
# Tue, 17 Jun 2025 15:25:00 GMT
ARG VERBOSE=false
# Tue, 17 Jun 2025 15:25:00 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250620250602-1102 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.6 liberty.version=25.0.0.6 io.openliberty.version=25.0.0.6
# Tue, 17 Jun 2025 15:25:00 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=a26724573f5c4f04fb9a39706a715e6bb85490c6 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.6/openliberty-runtime-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=a26724573f5c4f04fb9a39706a715e6bb85490c6 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.6/openliberty-runtime-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=a26724573f5c4f04fb9a39706a715e6bb85490c6 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.6/openliberty-runtime-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=a26724573f5c4f04fb9a39706a715e6bb85490c6 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.6/openliberty-runtime-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=a26724573f5c4f04fb9a39706a715e6bb85490c6 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.6/openliberty-runtime-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 17 Jun 2025 15:25:00 GMT
USER 1001
# Tue, 17 Jun 2025 15:25:00 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 17 Jun 2025 15:25:00 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 17 Jun 2025 15:25:00 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:cfa1809998a055f097abf4f27759694a126f64b86912d130052f49642e2be80b`  
		Last Modified: Tue, 03 Jun 2025 13:35:34 GMT  
		Size: 28.0 MB (28000600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a592dff2b7023a1eb4d0588791417d7ab44efe41ce34295948fbb1653b7e87`  
		Last Modified: Tue, 17 Jun 2025 21:00:33 GMT  
		Size: 12.2 MB (12219457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f9a11241be129350bbf9eefeee59c369d1f93eaeec203ee96fafe7498c45e7`  
		Last Modified: Wed, 18 Jun 2025 00:06:32 GMT  
		Size: 50.4 MB (50447233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1a01f10d855070783c6afb6bcd77e93282a21b38b97f7aaa165d6f7fedac9d`  
		Last Modified: Tue, 17 Jun 2025 18:13:33 GMT  
		Size: 4.4 MB (4365350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de2e20a2f4e6b7bcccfa43fc0e4da4c78149880b1518b4f51b6c4527d6d1198`  
		Last Modified: Tue, 17 Jun 2025 19:06:45 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50b6834511cb59bf26697abf3440422f53aa4a476e2e5bbeb037367c2d8a3dd`  
		Last Modified: Tue, 17 Jun 2025 22:35:12 GMT  
		Size: 12.5 KB (12468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e1066708a3e8bdda656392d9c83820f54c4c888f4a11b2c37764922aa76ec85`  
		Last Modified: Tue, 17 Jun 2025 22:35:13 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87312a6dd296e64a04a1972a49284238c95947c4cb2af2ef0ec7a9999e494fc`  
		Last Modified: Tue, 17 Jun 2025 23:00:15 GMT  
		Size: 33.1 KB (33112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4345298176874d659a6a6d897d87c5ae48ffea952d543d8b982fddb34bc2481e`  
		Last Modified: Wed, 18 Jun 2025 00:12:48 GMT  
		Size: 337.2 MB (337197120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9160d2af9e0cef4c48e060b32e98ce2ae54be156ff16af59832a56102e761b5b`  
		Last Modified: Tue, 17 Jun 2025 23:00:25 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0434dd963438a0b82c569b8b2bd9f03349bdbbf6cdfba92e470fdae9858cf61f`  
		Last Modified: Tue, 17 Jun 2025 23:00:29 GMT  
		Size: 13.9 KB (13873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e3e958d31a68050df1835f77697441f0e1c047754f00345187cdf09c9814f7`  
		Last Modified: Wed, 18 Jun 2025 00:11:54 GMT  
		Size: 13.5 MB (13537461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full` - unknown; unknown

```console
$ docker pull open-liberty@sha256:3928a7c14f01b4e265fb2328a6ba4343404ae928220fceddfadf9eacf40c5061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5752465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936e93e04849c0d267b5a5a2748adcbb334b74e07dc44f8c70b0ef6855e8e7f4`

```dockerfile
```

-	Layers:
	-	`sha256:c3a1f8da902e3259e916576aa23d0b683f1ab1c1dc622626fea6e34a8ba3ae03`  
		Last Modified: Tue, 17 Jun 2025 23:48:51 GMT  
		Size: 5.7 MB (5713045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e00923c8f6bb9186a782e30883e289efbf48380bbbcbf3f184637a96aa2c5c0a`  
		Last Modified: Tue, 17 Jun 2025 23:48:52 GMT  
		Size: 39.4 KB (39420 bytes)  
		MIME: application/vnd.in-toto+json
