## `open-liberty:beta`

```console
$ docker pull open-liberty@sha256:cceab65b7bc93f101a4d3418c56bceb558b2f9259631316d201d66537744f952
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

### `open-liberty:beta` - linux; amd64

```console
$ docker pull open-liberty@sha256:1522045a7011c27c96fbc8fffdc605faead3061fc92fdcebb49400109aa36e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **475.6 MB (475618557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb67533c477261ef7f01e6592827e1067139438d6f0b12c7507fdd8a6c3ced40`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 17 Jun 2025 14:26:50 GMT
ARG RELEASE
# Tue, 17 Jun 2025 14:26:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Jun 2025 14:26:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Jun 2025 14:26:50 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 17 Jun 2025 14:26:50 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Tue, 17 Jun 2025 14:26:50 GMT
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
ARG LIBERTY_VERSION=25.0.0.7-beta
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_SHA=8746c118b9f1616908949a6135dae57ebc5f8feb
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.7-beta/openliberty-runtime-25.0.0.7-beta.zip
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_BUILD_LABEL=cl250620250602-1102
# Tue, 17 Jun 2025 15:25:00 GMT
ARG OPENJ9_SCC=true
# Tue, 17 Jun 2025 15:25:00 GMT
ARG VERBOSE=false
# Tue, 17 Jun 2025 15:25:00 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250620250602-1102 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=25.0.0.7-beta liberty.version=25.0.0.7-beta io.openliberty.version=25.0.0.7-beta
# Tue, 17 Jun 2025 15:25:00 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.7-beta LIBERTY_SHA=8746c118b9f1616908949a6135dae57ebc5f8feb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.7-beta/openliberty-runtime-25.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.7-beta LIBERTY_SHA=8746c118b9f1616908949a6135dae57ebc5f8feb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.7-beta/openliberty-runtime-25.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.7-beta LIBERTY_SHA=8746c118b9f1616908949a6135dae57ebc5f8feb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.7-beta/openliberty-runtime-25.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.7-beta LIBERTY_SHA=8746c118b9f1616908949a6135dae57ebc5f8feb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.7-beta/openliberty-runtime-25.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.7-beta LIBERTY_SHA=8746c118b9f1616908949a6135dae57ebc5f8feb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.7-beta/openliberty-runtime-25.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
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
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2d2e1a062eeda7592b7c46b227001a4e9fddcbb5a3d65db311044b4ecbcb28`  
		Last Modified: Wed, 02 Jul 2025 03:11:06 GMT  
		Size: 12.2 MB (12172008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f89cd4121a57d16cc4f25201b02023f00fe5b21d5dee31fb4d433ba9f0b5f2`  
		Last Modified: Wed, 02 Jul 2025 03:11:08 GMT  
		Size: 50.5 MB (50498656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5826bda29218a7f9d360dd3fc868044be5efae8a08fcbff2292eb92946e4ee47`  
		Last Modified: Wed, 02 Jul 2025 03:11:06 GMT  
		Size: 4.3 MB (4340352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f809415603c98be40905ff715315abc6e4bb212b9130456df2e8b1bf7059d6c`  
		Last Modified: Wed, 02 Jul 2025 06:09:33 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25faeb60d046954bdaced6e90e1ba78f574fb16451ce587dc3d6c4d72989c0a1`  
		Last Modified: Wed, 02 Jul 2025 06:09:35 GMT  
		Size: 12.5 KB (12463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383a632eccc789d60068da66031585bb248bcf0c00ab711257237b6ec5aba656`  
		Last Modified: Wed, 02 Jul 2025 06:09:39 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e0d45188824eddedd7a78e7da6212fac9b1610941e6b6297e6f3308a7ff447`  
		Last Modified: Wed, 02 Jul 2025 05:57:27 GMT  
		Size: 31.7 KB (31748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1f6d68e6d95bfa13ae6bdb540f0015c818f41e9f89f65cbb2d6ab083bdcb7b`  
		Last Modified: Wed, 02 Jul 2025 13:41:23 GMT  
		Size: 365.5 MB (365547733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b148fbaafa02b548af1b968ff7d978693f5363cc8e9090d5e0f2b445dabbca`  
		Last Modified: Wed, 02 Jul 2025 06:09:43 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db4204ca684ea5fdbdf68e0e5053e4524f228bddbb1a4f694f0bc58200e10bb0`  
		Last Modified: Wed, 02 Jul 2025 06:09:46 GMT  
		Size: 13.9 KB (13865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d3c07697f3dfc637794b64d3b1f7ecfa35bf11f9de44b112cb7085c6d57642`  
		Last Modified: Wed, 02 Jul 2025 13:42:19 GMT  
		Size: 13.5 MB (13463698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta` - unknown; unknown

```console
$ docker pull open-liberty@sha256:0082a8e759f13f6ee760ed5897f8b32f73f78e110a12ce114b027c2c648865c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5843773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f952477a5d0ee6c224facdd17e58204a7b1018cac986aded7037ac38cda605bf`

```dockerfile
```

-	Layers:
	-	`sha256:244f26522a01b7e6334526548dec5f1f23b187d95062fabbb18a83fd6103b73e`  
		Last Modified: Wed, 02 Jul 2025 08:47:58 GMT  
		Size: 5.8 MB (5804859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:055be2dde53f605696cd60edb515016048a3f766a080f5e8cbee6d6e86620fdc`  
		Last Modified: Wed, 02 Jul 2025 08:47:59 GMT  
		Size: 38.9 KB (38914 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:07253730b1ac064ab94e9f3f3f02ac28c1aec2cba5e7b041a17676104da7a814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **472.1 MB (472101151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332390757142fb9419a4c8b291425fc2d2b8618004ba24c71dd513bbe1594995`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 17 Jun 2025 14:26:50 GMT
ARG RELEASE
# Tue, 17 Jun 2025 14:26:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Jun 2025 14:26:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Jun 2025 14:26:50 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 17 Jun 2025 14:26:50 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Tue, 17 Jun 2025 14:26:50 GMT
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
ARG LIBERTY_VERSION=25.0.0.7-beta
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_SHA=8746c118b9f1616908949a6135dae57ebc5f8feb
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.7-beta/openliberty-runtime-25.0.0.7-beta.zip
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_BUILD_LABEL=cl250620250602-1102
# Tue, 17 Jun 2025 15:25:00 GMT
ARG OPENJ9_SCC=true
# Tue, 17 Jun 2025 15:25:00 GMT
ARG VERBOSE=false
# Tue, 17 Jun 2025 15:25:00 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250620250602-1102 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=25.0.0.7-beta liberty.version=25.0.0.7-beta io.openliberty.version=25.0.0.7-beta
# Tue, 17 Jun 2025 15:25:00 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.7-beta LIBERTY_SHA=8746c118b9f1616908949a6135dae57ebc5f8feb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.7-beta/openliberty-runtime-25.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.7-beta LIBERTY_SHA=8746c118b9f1616908949a6135dae57ebc5f8feb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.7-beta/openliberty-runtime-25.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.7-beta LIBERTY_SHA=8746c118b9f1616908949a6135dae57ebc5f8feb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.7-beta/openliberty-runtime-25.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.7-beta LIBERTY_SHA=8746c118b9f1616908949a6135dae57ebc5f8feb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.7-beta/openliberty-runtime-25.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.7-beta LIBERTY_SHA=8746c118b9f1616908949a6135dae57ebc5f8feb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.7-beta/openliberty-runtime-25.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
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
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a289e598f42b384d895a5b849fe0c447bf26864e10dfb4c08dd439287ba95ca7`  
		Last Modified: Wed, 02 Jul 2025 05:27:01 GMT  
		Size: 12.1 MB (12129342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa725b7b5362f9e99863fc5387b5d6e908b37d0b8642c48732036980ebf0f6d`  
		Last Modified: Wed, 02 Jul 2025 05:28:56 GMT  
		Size: 49.9 MB (49934834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ce3442a41711065d68824c177c7843a4282b07dc4827462d5eb9168e05d4b5`  
		Last Modified: Wed, 02 Jul 2025 05:29:09 GMT  
		Size: 4.1 MB (4068034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1714ccde6de122e99e2ba7826a745754fbc09fd670c717a09a08c0e2bd1f43c`  
		Last Modified: Wed, 02 Jul 2025 08:51:28 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4e8f75293bff2aa48d53fe6c2d5d830dbe87cd05c14f545096c2488e4a6dc7`  
		Last Modified: Wed, 02 Jul 2025 08:51:28 GMT  
		Size: 12.5 KB (12458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c4be5b319f12e7d0780e084ff6615c4f857c93907fb25db37a4102766126d0`  
		Last Modified: Wed, 02 Jul 2025 08:51:28 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21424449e65eb375f5c2834f0e2517fadaf556f695b7fb07a48649bade251415`  
		Last Modified: Wed, 02 Jul 2025 08:51:28 GMT  
		Size: 42.3 KB (42325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa17916d0243c78ee1886e1cae9d2fd9d25094145e34e714d9dab48d663eb7d1`  
		Last Modified: Wed, 02 Jul 2025 08:51:21 GMT  
		Size: 365.5 MB (365548045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27017b3d1b1ff6339155e160be0c180420734e7c800463126f1a939210805d0b`  
		Last Modified: Wed, 02 Jul 2025 08:51:29 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2e4d3cf1c2eaed849772eba53a8b050aecea5d93c95ffde23dcce627e07b2f`  
		Last Modified: Wed, 02 Jul 2025 08:51:28 GMT  
		Size: 13.9 KB (13862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d551f5d3148170a7bdf1ff40dfd7557acde65da41455de0399e2534f22706aa`  
		Last Modified: Wed, 02 Jul 2025 08:51:29 GMT  
		Size: 13.0 MB (12990630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta` - unknown; unknown

```console
$ docker pull open-liberty@sha256:0453e6f7a3b0a04f9b61df6bf9f4c363b5d2e56c0341e6040502eabe92253618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5843693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af76ed1805b6d7dd9d20cf77c536cc7b0ccb95abcd81949091c8ae4344814cc`

```dockerfile
```

-	Layers:
	-	`sha256:db2e361108e7671cc23f2f68f1a90e7d9ba4ca8cb5f17996de710364eafea770`  
		Last Modified: Wed, 02 Jul 2025 11:46:37 GMT  
		Size: 5.8 MB (5804651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b050793a67ed4b46776ee75e1651f945e9b4d21cdd0a045a00807d35bc86d10`  
		Last Modified: Wed, 02 Jul 2025 11:46:38 GMT  
		Size: 39.0 KB (39042 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:6ca7e3f0015962309d9b49eba0518173a973a9aa67a583f13a1bb570454de510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.2 MB (480238000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec8fdd3ec599a01d2bd636eec8466d4fbff8a5b5bdb6c672e444e014a642948`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 17 Jun 2025 14:26:50 GMT
ARG RELEASE
# Tue, 17 Jun 2025 14:26:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Jun 2025 14:26:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Jun 2025 14:26:50 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 17 Jun 2025 14:26:50 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Tue, 17 Jun 2025 14:26:50 GMT
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
ARG LIBERTY_VERSION=25.0.0.7-beta
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_SHA=8746c118b9f1616908949a6135dae57ebc5f8feb
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.7-beta/openliberty-runtime-25.0.0.7-beta.zip
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_BUILD_LABEL=cl250620250602-1102
# Tue, 17 Jun 2025 15:25:00 GMT
ARG OPENJ9_SCC=true
# Tue, 17 Jun 2025 15:25:00 GMT
ARG VERBOSE=false
# Tue, 17 Jun 2025 15:25:00 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250620250602-1102 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=25.0.0.7-beta liberty.version=25.0.0.7-beta io.openliberty.version=25.0.0.7-beta
# Tue, 17 Jun 2025 15:25:00 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.7-beta LIBERTY_SHA=8746c118b9f1616908949a6135dae57ebc5f8feb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.7-beta/openliberty-runtime-25.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.7-beta LIBERTY_SHA=8746c118b9f1616908949a6135dae57ebc5f8feb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.7-beta/openliberty-runtime-25.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.7-beta LIBERTY_SHA=8746c118b9f1616908949a6135dae57ebc5f8feb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.7-beta/openliberty-runtime-25.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.7-beta LIBERTY_SHA=8746c118b9f1616908949a6135dae57ebc5f8feb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.7-beta/openliberty-runtime-25.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.7-beta LIBERTY_SHA=8746c118b9f1616908949a6135dae57ebc5f8feb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.7-beta/openliberty-runtime-25.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
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
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eadc2c3c98e81c215197904badede29a92518c461aab0c7b9d0848370fef917`  
		Last Modified: Wed, 02 Jul 2025 03:32:25 GMT  
		Size: 12.9 MB (12893371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9568e32429608a09f341b5aadc72c195a1a76ade8d75046263a4ea26a7a3f3b`  
		Last Modified: Wed, 02 Jul 2025 03:35:22 GMT  
		Size: 51.9 MB (51920019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e098fd9118ab7e9e55e639e49be86b02c5c4a9ecef809314462a6d985c2036a9`  
		Last Modified: Wed, 02 Jul 2025 03:35:16 GMT  
		Size: 3.5 MB (3456554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:692207d16b47423f341d97d0615a596a920d91a3d694010336419c74d9f20471`  
		Last Modified: Wed, 02 Jul 2025 05:38:07 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e3276247a8fee33079932cb5e01b228ee617def0e47ac93c159619a845a333`  
		Last Modified: Wed, 02 Jul 2025 05:38:07 GMT  
		Size: 12.5 KB (12460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d9e547f70242468172e7c064327ecdad94517e80b455d0936b4077f7b68a3`  
		Last Modified: Wed, 02 Jul 2025 05:38:07 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567ff68c9fe87d69d50969c611d5d88d46ab010cc09e75a5967c94bedbe76a8d`  
		Last Modified: Wed, 02 Jul 2025 05:38:07 GMT  
		Size: 36.5 KB (36497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac95746d885cf038df626f8852a2b3c658a7b60db1b839210724b03d80e07a42`  
		Last Modified: Wed, 02 Jul 2025 05:38:01 GMT  
		Size: 365.5 MB (365548175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d967da1a97b335e288a252e646b8b9a794e38526c8a43384470812701eae11f`  
		Last Modified: Wed, 02 Jul 2025 05:38:07 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cc8373c962e28b5aaf43ae2fb814f6681d43dc082690774b99d14bf7dc647e`  
		Last Modified: Wed, 02 Jul 2025 05:38:07 GMT  
		Size: 13.9 KB (13861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95dab9d309b8d677d199988f76b3838100bd9124c461a7ae09f72d140e084f6e`  
		Last Modified: Wed, 02 Jul 2025 05:38:09 GMT  
		Size: 11.9 MB (11912095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta` - unknown; unknown

```console
$ docker pull open-liberty@sha256:975e89785ed6f7a5d572a55bd60862e00d1a75c168ef63f573bf52c9bde77966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5848594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d177aca6483230549c8e3f49cc3cdabe75599481f3e000bd624b97cc6a3db418`

```dockerfile
```

-	Layers:
	-	`sha256:8a1280ce527602e2bda8d3b04f2b29322f058c0f74c2dbf368e36ea8116c00d4`  
		Last Modified: Wed, 02 Jul 2025 08:48:10 GMT  
		Size: 5.8 MB (5809646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac047b5c1706516934718016dcacaf596e2cc4e6b2fe6f576a3380d4c6b3d8b7`  
		Last Modified: Wed, 02 Jul 2025 08:48:11 GMT  
		Size: 38.9 KB (38948 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta` - linux; s390x

```console
$ docker pull open-liberty@sha256:4984079d5c765a606ac6b5666fcca9ee30bc7b695662015c5eadf525536eb1c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **474.2 MB (474187714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4f4572ff5bd7309523774265eff8441a95fa0ffad3967377d4c9a80dc67ebc`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 17 Jun 2025 14:26:50 GMT
ARG RELEASE
# Tue, 17 Jun 2025 14:26:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Jun 2025 14:26:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Jun 2025 14:26:50 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 17 Jun 2025 14:26:50 GMT
ADD file:dad9a012cce363ba4f28e2a6f3efa82869330e872362e4867be1bd507ed8963a in / 
# Tue, 17 Jun 2025 14:26:50 GMT
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
ARG LIBERTY_VERSION=25.0.0.7-beta
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_SHA=8746c118b9f1616908949a6135dae57ebc5f8feb
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.7-beta/openliberty-runtime-25.0.0.7-beta.zip
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_BUILD_LABEL=cl250620250602-1102
# Tue, 17 Jun 2025 15:25:00 GMT
ARG OPENJ9_SCC=true
# Tue, 17 Jun 2025 15:25:00 GMT
ARG VERBOSE=false
# Tue, 17 Jun 2025 15:25:00 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250620250602-1102 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=25.0.0.7-beta liberty.version=25.0.0.7-beta io.openliberty.version=25.0.0.7-beta
# Tue, 17 Jun 2025 15:25:00 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.7-beta LIBERTY_SHA=8746c118b9f1616908949a6135dae57ebc5f8feb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.7-beta/openliberty-runtime-25.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.7-beta LIBERTY_SHA=8746c118b9f1616908949a6135dae57ebc5f8feb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.7-beta/openliberty-runtime-25.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.7-beta LIBERTY_SHA=8746c118b9f1616908949a6135dae57ebc5f8feb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.7-beta/openliberty-runtime-25.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.7-beta LIBERTY_SHA=8746c118b9f1616908949a6135dae57ebc5f8feb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.7-beta/openliberty-runtime-25.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.7-beta LIBERTY_SHA=8746c118b9f1616908949a6135dae57ebc5f8feb LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.7-beta/openliberty-runtime-25.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
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
	-	`sha256:8d24804db3a6eaf32ea752d2dd82fb21273e4e2494ca124217c93f38bc823ca5`  
		Last Modified: Wed, 02 Jul 2025 03:43:01 GMT  
		Size: 28.0 MB (28002175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a788032c33b6158b1f575b583e28cd102180464b55e1900dc45ca278fc0a68f`  
		Last Modified: Wed, 02 Jul 2025 04:27:00 GMT  
		Size: 12.2 MB (12219341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa244966f7f98048a948f75b9297e4df8e65d1a811795df6b7a21e53da440b1a`  
		Last Modified: Wed, 02 Jul 2025 04:29:18 GMT  
		Size: 50.4 MB (50447209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f55f83cfa933aed4642227f6961fdff53f5c0aa7d8b7b5f72c3b79a01c40dae`  
		Last Modified: Wed, 02 Jul 2025 04:28:59 GMT  
		Size: 4.4 MB (4353052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579508be22ba538d033f588e7f0d1c93d6579616418660e2505a909cb516b25d`  
		Last Modified: Wed, 02 Jul 2025 05:34:00 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f8aa02c137b470fcf9ac803cbfe83c81ffb0642748e29f78ec9021ed196a1d`  
		Last Modified: Wed, 02 Jul 2025 05:34:00 GMT  
		Size: 12.5 KB (12456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d872c20f0127cc7cd82d332b400a47a64dbc98c4d626dd6a0722661ffdb7e36b`  
		Last Modified: Wed, 02 Jul 2025 05:34:01 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2a19de6be3ddf8e7ed79c996018e5c497b02d826e7cdaf8826d759006f4cb3`  
		Last Modified: Wed, 02 Jul 2025 05:34:00 GMT  
		Size: 33.1 KB (33112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ebbddd50d0add157cf69dd8074e73b331bb889720b5d5324cdd64a7844c664`  
		Last Modified: Wed, 02 Jul 2025 05:33:53 GMT  
		Size: 365.5 MB (365547549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6709261d373a02da43721613bd43bbfd32634249f8779a65e9e0c639cff3e94b`  
		Last Modified: Wed, 02 Jul 2025 05:34:00 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03888f560b36dcc056789fd555fad96f645b32211d4899e4ddd02827bf1bb443`  
		Last Modified: Wed, 02 Jul 2025 05:34:00 GMT  
		Size: 13.9 KB (13856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3258b2a6b9d5e0c8487fa96f6b6d463a96505aad4d8bf3fb267b29e133420e8f`  
		Last Modified: Wed, 02 Jul 2025 05:34:02 GMT  
		Size: 13.6 MB (13556623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta` - unknown; unknown

```console
$ docker pull open-liberty@sha256:7d12e23aaee551a2d4a0f891048465d14f5e10c2502742b8c78aa6dafa90bef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5844790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:274cf5e43a03af4da00a5bad762ce56bcf32d7c25c8f0394f826dc40b847b57d`

```dockerfile
```

-	Layers:
	-	`sha256:e410d009c46d10f80527a3cb5c961e1206a839a3363b4519fd4fd2d88450ee5d`  
		Last Modified: Wed, 02 Jul 2025 08:48:16 GMT  
		Size: 5.8 MB (5805876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ad483961cf8db544d5fb6cd8cb39aed1b8f81213fe264a7e98213a4cd847e84`  
		Last Modified: Wed, 02 Jul 2025 08:48:17 GMT  
		Size: 38.9 KB (38914 bytes)  
		MIME: application/vnd.in-toto+json
