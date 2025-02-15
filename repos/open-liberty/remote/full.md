## `open-liberty:full`

```console
$ docker pull open-liberty@sha256:ce9923d28cbbdf649828a4744a516d8fe569dcbd83f84e783c91be3998f86adf
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
$ docker pull open-liberty@sha256:59aa1ddcc8a26fd77c55afe14eb5e4228a845f1e1f3b8b2ea39090406deec24a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.8 MB (446811689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b219da498906e01483be9717f03c941abbf102d6c356b01225efcf773be0c48`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Tue, 28 Jan 2025 17:39:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 28 Jan 2025 17:39:44 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
ENV JAVA_VERSION=jdk8u442-b06_openj9-0.49.0
# Tue, 28 Jan 2025 17:39:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='7975d93310af64c805c76b5bcab8b195121d76321ebf72d1ff9bb2bff2426277';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jre_aarch64_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='2c5acea578d59fdab41f8544beddfa6af0893d91cde4b92233ed158c35ac3397';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jre_ppc64le_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='d665f2e041c18de11f15955164c935961e7da0bf9358182769466611d83c5b32';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jre_x64_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='2af59a4f3600e41b7e0d6b8ab18006d852af0d81895902dc6d46feeab1f5b195';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jre_s390x_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 17:39:44 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 28 Jan 2025 17:39:44 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="bf406b3e288e1732d82d08f54e160095451a6cc969f72adf395c074d6d08893ef1ccd2afcd55f01ca8e54131f587c88055832f36330a1ede0cc2f84440cf54df";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.99/bin/apache-tomcat-9.0.99.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
USER root
# Tue, 28 Jan 2025 17:39:44 GMT
ARG LIBERTY_VERSION=25.0.0.1
# Tue, 28 Jan 2025 17:39:44 GMT
ARG LIBERTY_SHA=f889eab11f1ef7ece29dac622d2842208aa602c3
# Tue, 28 Jan 2025 17:39:44 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.1/openliberty-runtime-25.0.0.1.zip
# Tue, 28 Jan 2025 17:39:44 GMT
ARG LIBERTY_BUILD_LABEL=cl250120250113-0302
# Tue, 28 Jan 2025 17:39:44 GMT
ARG OPENJ9_SCC=true
# Tue, 28 Jan 2025 17:39:44 GMT
ARG VERBOSE=false
# Tue, 28 Jan 2025 17:39:44 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250120250113-0302 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.1 liberty.version=25.0.0.1 io.openliberty.version=25.0.0.1
# Tue, 28 Jan 2025 17:39:44 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
# ARGS: LIBERTY_VERSION=25.0.0.1 LIBERTY_SHA=f889eab11f1ef7ece29dac622d2842208aa602c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.1/openliberty-runtime-25.0.0.1.zip LIBERTY_BUILD_LABEL=cl250120250113-0302 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
# ARGS: LIBERTY_VERSION=25.0.0.1 LIBERTY_SHA=f889eab11f1ef7ece29dac622d2842208aa602c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.1/openliberty-runtime-25.0.0.1.zip LIBERTY_BUILD_LABEL=cl250120250113-0302 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 28 Jan 2025 17:39:44 GMT
# ARGS: LIBERTY_VERSION=25.0.0.1 LIBERTY_SHA=f889eab11f1ef7ece29dac622d2842208aa602c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.1/openliberty-runtime-25.0.0.1.zip LIBERTY_BUILD_LABEL=cl250120250113-0302 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
# ARGS: LIBERTY_VERSION=25.0.0.1 LIBERTY_SHA=f889eab11f1ef7ece29dac622d2842208aa602c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.1/openliberty-runtime-25.0.0.1.zip LIBERTY_BUILD_LABEL=cl250120250113-0302 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
# ARGS: LIBERTY_VERSION=25.0.0.1 LIBERTY_SHA=f889eab11f1ef7ece29dac622d2842208aa602c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.1/openliberty-runtime-25.0.0.1.zip LIBERTY_BUILD_LABEL=cl250120250113-0302 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 28 Jan 2025 17:39:44 GMT
USER 1001
# Tue, 28 Jan 2025 17:39:44 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 28 Jan 2025 17:39:44 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 28 Jan 2025 17:39:44 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5c87ac894c18ebaaefd577877954e6b37b15c96c5aef00108587beeeccb153`  
		Last Modified: Fri, 14 Feb 2025 23:28:59 GMT  
		Size: 12.2 MB (12166730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19679bf6a4a3596742288b9b3382b0d1b8d16a0b86954d0180bdf464f39398c1`  
		Last Modified: Fri, 14 Feb 2025 23:29:02 GMT  
		Size: 50.4 MB (50438005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0763e0156aa892026a423c25d79bff52f9a200a0143568d9eadb3646ad7bbbad`  
		Last Modified: Fri, 14 Feb 2025 23:28:58 GMT  
		Size: 4.2 MB (4228213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c06aaad9691f323a8940fa78441d5fa034816756af914bf6659bec66d3b9abc`  
		Last Modified: Sat, 15 Feb 2025 00:55:44 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6667971a3768cf3ea35a7bbd52bb1e1ac11fe3b6e297ea2b377b546ba973e585`  
		Last Modified: Sat, 15 Feb 2025 00:55:44 GMT  
		Size: 10.1 KB (10105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6107b646ff9023c74838f1ef1fbdef3178c2bd0747a9935e1c1340b4e53ef8`  
		Last Modified: Sat, 15 Feb 2025 00:55:45 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b33aa148d34a4b8d1fb89dc85d1f8867570da6d0b8c437ac39d1169b58badbc`  
		Last Modified: Sat, 15 Feb 2025 00:55:44 GMT  
		Size: 31.7 KB (31749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba9b724d801e6e07655c7ef2e35efdab7bd9c725fdf6d836e1bb4ed06c4a8b1`  
		Last Modified: Sat, 15 Feb 2025 00:55:59 GMT  
		Size: 336.9 MB (336891844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819b408231ed564f522bc3a55f7aad30281d83a5b2fde79a25371e232f567737`  
		Last Modified: Sat, 15 Feb 2025 00:55:45 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f047c5e3ec197705a025e22e256f758dfbcb7cdc9d8f64605a924672f826d117`  
		Last Modified: Sat, 15 Feb 2025 00:55:45 GMT  
		Size: 11.5 KB (11471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555e2a47a1a0659bc83e886e1424c5a9daf5dbd39b751477dafa538a5a6b879b`  
		Last Modified: Sat, 15 Feb 2025 00:55:46 GMT  
		Size: 13.5 MB (13495281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full` - unknown; unknown

```console
$ docker pull open-liberty@sha256:516a8536620e6315addfdea1a66a52aab0912c800e2b0273a8111c2483f5c21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5577525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd228e6f62927ba6ca145390b0c6aa2fbfc627bac2862fb5828857cea6ad2fdc`

```dockerfile
```

-	Layers:
	-	`sha256:95742cb3724afe8d4a0ef3146596104b0b181313287988a470166468c6d0edf6`  
		Last Modified: Sat, 15 Feb 2025 00:47:13 GMT  
		Size: 5.5 MB (5538210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:886c225b76124d4520527e905d645c6809ff4cfe582950acb399c31fba48924c`  
		Last Modified: Sat, 15 Feb 2025 00:47:14 GMT  
		Size: 39.3 KB (39315 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:91b5aa362f6f361a51b7b89f710c5985582df6812b7e3894af5b9f853bef81fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **443.2 MB (443244653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e512ad63ff46d636213f2e1dd2b131ed5c679f09bf5fcd930696c74ef0f18e9b`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 17 Dec 2024 06:18:06 GMT
ARG RELEASE
# Tue, 17 Dec 2024 06:18:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Dec 2024 06:18:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Dec 2024 06:18:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 17 Dec 2024 06:18:06 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Tue, 17 Dec 2024 06:18:06 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2024 06:18:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Dec 2024 06:18:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_VERSION=jdk8u432-b06_openj9-0.48.0
# Tue, 17 Dec 2024 06:18:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='01e57b0ada3dc34b08d2f4644b64244f7a1e9a63cf885f47b9baadf663230b5d';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jre_aarch64_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8ba759756722e415ae011bee0c4045f38e2b8e15535488944420fb8c1932d710';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jre_ppc64le_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b38ef6c7520463822affa424b4ad0e16686b86b01255b0c9912743d3f6e98a73';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jre_x64_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='5bcb556f2cd0352c14205321afdeac37615249f874ae37e84601287f5eb5be5b';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jre_s390x_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Dec 2024 06:18:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.98/bin/apache-tomcat-9.0.98.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
USER root
# Tue, 28 Jan 2025 17:39:44 GMT
ARG LIBERTY_VERSION=25.0.0.1
# Tue, 28 Jan 2025 17:39:44 GMT
ARG LIBERTY_SHA=f889eab11f1ef7ece29dac622d2842208aa602c3
# Tue, 28 Jan 2025 17:39:44 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.1/openliberty-runtime-25.0.0.1.zip
# Tue, 28 Jan 2025 17:39:44 GMT
ARG LIBERTY_BUILD_LABEL=cl250120250113-0302
# Tue, 28 Jan 2025 17:39:44 GMT
ARG OPENJ9_SCC=true
# Tue, 28 Jan 2025 17:39:44 GMT
ARG VERBOSE=false
# Tue, 28 Jan 2025 17:39:44 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250120250113-0302 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.1 liberty.version=25.0.0.1 io.openliberty.version=25.0.0.1
# Tue, 28 Jan 2025 17:39:44 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
# ARGS: LIBERTY_VERSION=25.0.0.1 LIBERTY_SHA=f889eab11f1ef7ece29dac622d2842208aa602c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.1/openliberty-runtime-25.0.0.1.zip LIBERTY_BUILD_LABEL=cl250120250113-0302 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
# ARGS: LIBERTY_VERSION=25.0.0.1 LIBERTY_SHA=f889eab11f1ef7ece29dac622d2842208aa602c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.1/openliberty-runtime-25.0.0.1.zip LIBERTY_BUILD_LABEL=cl250120250113-0302 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 28 Jan 2025 17:39:44 GMT
# ARGS: LIBERTY_VERSION=25.0.0.1 LIBERTY_SHA=f889eab11f1ef7ece29dac622d2842208aa602c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.1/openliberty-runtime-25.0.0.1.zip LIBERTY_BUILD_LABEL=cl250120250113-0302 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
# ARGS: LIBERTY_VERSION=25.0.0.1 LIBERTY_SHA=f889eab11f1ef7ece29dac622d2842208aa602c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.1/openliberty-runtime-25.0.0.1.zip LIBERTY_BUILD_LABEL=cl250120250113-0302 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
# ARGS: LIBERTY_VERSION=25.0.0.1 LIBERTY_SHA=f889eab11f1ef7ece29dac622d2842208aa602c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.1/openliberty-runtime-25.0.0.1.zip LIBERTY_BUILD_LABEL=cl250120250113-0302 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 28 Jan 2025 17:39:44 GMT
USER 1001
# Tue, 28 Jan 2025 17:39:44 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 28 Jan 2025 17:39:44 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 28 Jan 2025 17:39:44 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc27324a20ba7e580ad161f241011b423fdcd169bcae5cc324e63f8db8fe6b2`  
		Last Modified: Wed, 05 Feb 2025 00:32:28 GMT  
		Size: 12.1 MB (12123437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d82fca0d864d57b96ada2f41763e12a50d70893733b44847eab155e1860131`  
		Last Modified: Wed, 05 Feb 2025 04:01:26 GMT  
		Size: 49.8 MB (49805608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28af106710dac110102541f4beb6395aa2c4f8e2640f8c7da88eca55cda3485`  
		Last Modified: Wed, 05 Feb 2025 04:01:31 GMT  
		Size: 4.1 MB (4063080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17eb2516df613521ce2b32d86ab3bf22a7d159a0e85dac57faf9dbf9ecaab46d`  
		Last Modified: Tue, 04 Feb 2025 21:43:53 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb62e4cf79b6feb0c82439cb5fa4d37e4e7e2ead32f436299c6095722fdc61b`  
		Last Modified: Wed, 05 Feb 2025 21:33:21 GMT  
		Size: 10.1 KB (10107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea74e64169a93f369a5e1db8f62f13325cefd6077af3524dabdda1aa4ec01f6`  
		Last Modified: Wed, 05 Feb 2025 21:33:22 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4dc377cd3d71ad2d28ac03efe78fa44891439f01616d55ebdaf46b6684cb8bf`  
		Last Modified: Wed, 05 Feb 2025 21:33:22 GMT  
		Size: 42.3 KB (42324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faca4ae1b651be3e2f275eb651390e432ceb6292dd95ab1b2cc971526f2956aa`  
		Last Modified: Wed, 05 Feb 2025 21:33:34 GMT  
		Size: 336.9 MB (336891871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468a4ed9dab3256ae12068616224f9f46cce7b80aba031afbfc3d9318a49787a`  
		Last Modified: Wed, 05 Feb 2025 21:33:22 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5cc9d23c67622bb446373e66443887cac674c6ce0d916e8ccea01df352b222`  
		Last Modified: Wed, 05 Feb 2025 21:33:23 GMT  
		Size: 11.5 KB (11488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e6915fe70ea08e1909f4c4b591e25d0dd3a16883f6476cf150eea91575955c`  
		Last Modified: Wed, 05 Feb 2025 21:33:24 GMT  
		Size: 12.9 MB (12936210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full` - unknown; unknown

```console
$ docker pull open-liberty@sha256:f50bb7734d5344e8b6de69f14c0bd62749bc89e201df8cfad0888363635c755d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5575886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c99566805fa02dbde112b21eec556c4a7d734e5e9ed887bb5bfdde76ae23002`

```dockerfile
```

-	Layers:
	-	`sha256:8555f3978d455305e8668a6beb7aa03576047bd98fe7ef80a6e1000044f34847`  
		Last Modified: Wed, 05 Feb 2025 08:44:15 GMT  
		Size: 5.5 MB (5536418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:600229a216cf20b1ba0271f0cff184a06ccf8d46801c45264090531929a5c390`  
		Last Modified: Mon, 10 Feb 2025 18:38:24 GMT  
		Size: 39.5 KB (39468 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:4b24f3e1cd0b7b45ab366d816e83995cb8a849fec8d878fc6ecd355ce8dd6296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.4 MB (451409907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c05403ede4fda140d057c8d143a440710f0e6bff1f9f9992d0c8ca3a15f7fd`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:49 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:54 GMT
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Sun, 26 Jan 2025 05:31:54 GMT
CMD ["/bin/bash"]
# Tue, 28 Jan 2025 17:39:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 28 Jan 2025 17:39:44 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
ENV JAVA_VERSION=jdk8u442-b06_openj9-0.49.0
# Tue, 28 Jan 2025 17:39:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='7975d93310af64c805c76b5bcab8b195121d76321ebf72d1ff9bb2bff2426277';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jre_aarch64_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='2c5acea578d59fdab41f8544beddfa6af0893d91cde4b92233ed158c35ac3397';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jre_ppc64le_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='d665f2e041c18de11f15955164c935961e7da0bf9358182769466611d83c5b32';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jre_x64_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='2af59a4f3600e41b7e0d6b8ab18006d852af0d81895902dc6d46feeab1f5b195';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jre_s390x_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 17:39:44 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 28 Jan 2025 17:39:44 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="bf406b3e288e1732d82d08f54e160095451a6cc969f72adf395c074d6d08893ef1ccd2afcd55f01ca8e54131f587c88055832f36330a1ede0cc2f84440cf54df";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.99/bin/apache-tomcat-9.0.99.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
USER root
# Tue, 28 Jan 2025 17:39:44 GMT
ARG LIBERTY_VERSION=25.0.0.1
# Tue, 28 Jan 2025 17:39:44 GMT
ARG LIBERTY_SHA=f889eab11f1ef7ece29dac622d2842208aa602c3
# Tue, 28 Jan 2025 17:39:44 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.1/openliberty-runtime-25.0.0.1.zip
# Tue, 28 Jan 2025 17:39:44 GMT
ARG LIBERTY_BUILD_LABEL=cl250120250113-0302
# Tue, 28 Jan 2025 17:39:44 GMT
ARG OPENJ9_SCC=true
# Tue, 28 Jan 2025 17:39:44 GMT
ARG VERBOSE=false
# Tue, 28 Jan 2025 17:39:44 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250120250113-0302 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.1 liberty.version=25.0.0.1 io.openliberty.version=25.0.0.1
# Tue, 28 Jan 2025 17:39:44 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
# ARGS: LIBERTY_VERSION=25.0.0.1 LIBERTY_SHA=f889eab11f1ef7ece29dac622d2842208aa602c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.1/openliberty-runtime-25.0.0.1.zip LIBERTY_BUILD_LABEL=cl250120250113-0302 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
# ARGS: LIBERTY_VERSION=25.0.0.1 LIBERTY_SHA=f889eab11f1ef7ece29dac622d2842208aa602c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.1/openliberty-runtime-25.0.0.1.zip LIBERTY_BUILD_LABEL=cl250120250113-0302 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 28 Jan 2025 17:39:44 GMT
# ARGS: LIBERTY_VERSION=25.0.0.1 LIBERTY_SHA=f889eab11f1ef7ece29dac622d2842208aa602c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.1/openliberty-runtime-25.0.0.1.zip LIBERTY_BUILD_LABEL=cl250120250113-0302 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
# ARGS: LIBERTY_VERSION=25.0.0.1 LIBERTY_SHA=f889eab11f1ef7ece29dac622d2842208aa602c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.1/openliberty-runtime-25.0.0.1.zip LIBERTY_BUILD_LABEL=cl250120250113-0302 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
# ARGS: LIBERTY_VERSION=25.0.0.1 LIBERTY_SHA=f889eab11f1ef7ece29dac622d2842208aa602c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.1/openliberty-runtime-25.0.0.1.zip LIBERTY_BUILD_LABEL=cl250120250113-0302 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 28 Jan 2025 17:39:44 GMT
USER 1001
# Tue, 28 Jan 2025 17:39:44 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 28 Jan 2025 17:39:44 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 28 Jan 2025 17:39:44 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Tue, 04 Feb 2025 07:01:41 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9757f7d530f6b57a9f7086a87275499eba37462ad62756a55dcd465daa91caa2`  
		Last Modified: Wed, 05 Feb 2025 08:43:21 GMT  
		Size: 12.9 MB (12894981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81735207281899bd98eec233d3e89b4608876ea96661ec6eb121a30a8bc2e76`  
		Last Modified: Sat, 15 Feb 2025 02:10:56 GMT  
		Size: 51.8 MB (51832707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365fbcecde2824a783ec0ba5ce9722572df45e5a6a69322aacfb1092163e5b22`  
		Last Modified: Sat, 15 Feb 2025 02:10:54 GMT  
		Size: 3.5 MB (3471871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec03d3755e43744a05fc3c3831af1c383ae6d5aad4a1abce70e1c789b6f7d625`  
		Last Modified: Sat, 15 Feb 2025 06:09:49 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74b3a0586e956f7094706220f270183da4a654a185021d94f58ee3ceefed5ac`  
		Last Modified: Sat, 15 Feb 2025 05:22:31 GMT  
		Size: 10.1 KB (10108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34610b173daf8d67f6958fa46a8c2d92ebacb491a70e6566bf32eccd16f3b15e`  
		Last Modified: Sat, 15 Feb 2025 05:22:32 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7cce3eae55df772a44f10358fa6a1eadd760ba6ad7fb96d442c0fafb48ff800`  
		Last Modified: Sat, 15 Feb 2025 05:34:10 GMT  
		Size: 36.5 KB (36497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84655e6fadba6f73339d4aaafca7768119db1ab6cd8822accda74e4a03591f9f`  
		Last Modified: Sat, 15 Feb 2025 05:34:31 GMT  
		Size: 336.9 MB (336892016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb79ff0e2fced95f108f058eeacadf63ee8af6c5c9c232c918d75fc4c70f4619`  
		Last Modified: Sat, 15 Feb 2025 05:34:10 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885536d1b70b379db4f530e64f5690b3c5542e29ff968cce51a22089e2bda053`  
		Last Modified: Sat, 15 Feb 2025 05:34:10 GMT  
		Size: 11.5 KB (11489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8485b57fbdde82ce26e4d6e961a24ca5ede1cc2b0be75ecc6f114411f403a165`  
		Last Modified: Sat, 15 Feb 2025 05:34:12 GMT  
		Size: 11.8 MB (11809950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full` - unknown; unknown

```console
$ docker pull open-liberty@sha256:584cbe3ba69d7e13ce8087d00d85da100f60550b256f76b86c1792673be729fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5580624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2033c7540d69af7276489038e337aec4940a0d40f6628c30d4be1840dba149`

```dockerfile
```

-	Layers:
	-	`sha256:77c0f5791e238df370a042ea1d6f39c3a7455b006262c767fe2500978caeec58`  
		Last Modified: Sat, 15 Feb 2025 06:47:14 GMT  
		Size: 5.5 MB (5541263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26431679d61114035928f79c0b36be87f875479562250918055f92e46e62f8ac`  
		Last Modified: Sat, 15 Feb 2025 06:47:15 GMT  
		Size: 39.4 KB (39361 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full` - linux; s390x

```console
$ docker pull open-liberty@sha256:9014c33008dde004e4b944f641de967c8a10a10c348646e079ad03359501e170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.3 MB (445252718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484b5205fb6b08525423e409454ae4a965f4f03bf85f3bd045fa6191b8d5ae34`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 17 Dec 2024 06:18:06 GMT
ARG RELEASE
# Tue, 17 Dec 2024 06:18:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Dec 2024 06:18:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Dec 2024 06:18:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 17 Dec 2024 06:18:06 GMT
ADD file:39a6583c8b71c00e0ea7562cadb2b343caf5c0c274178520c7476e53faed2e3e in / 
# Tue, 17 Dec 2024 06:18:06 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2024 06:18:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Dec 2024 06:18:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_VERSION=jdk8u432-b06_openj9-0.48.0
# Tue, 17 Dec 2024 06:18:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='01e57b0ada3dc34b08d2f4644b64244f7a1e9a63cf885f47b9baadf663230b5d';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jre_aarch64_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8ba759756722e415ae011bee0c4045f38e2b8e15535488944420fb8c1932d710';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jre_ppc64le_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b38ef6c7520463822affa424b4ad0e16686b86b01255b0c9912743d3f6e98a73';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jre_x64_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='5bcb556f2cd0352c14205321afdeac37615249f874ae37e84601287f5eb5be5b';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jre_s390x_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Dec 2024 06:18:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Dec 2024 06:18:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.98/bin/apache-tomcat-9.0.98.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
USER root
# Tue, 28 Jan 2025 17:39:44 GMT
ARG LIBERTY_VERSION=25.0.0.1
# Tue, 28 Jan 2025 17:39:44 GMT
ARG LIBERTY_SHA=f889eab11f1ef7ece29dac622d2842208aa602c3
# Tue, 28 Jan 2025 17:39:44 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.1/openliberty-runtime-25.0.0.1.zip
# Tue, 28 Jan 2025 17:39:44 GMT
ARG LIBERTY_BUILD_LABEL=cl250120250113-0302
# Tue, 28 Jan 2025 17:39:44 GMT
ARG OPENJ9_SCC=true
# Tue, 28 Jan 2025 17:39:44 GMT
ARG VERBOSE=false
# Tue, 28 Jan 2025 17:39:44 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250120250113-0302 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.1 liberty.version=25.0.0.1 io.openliberty.version=25.0.0.1
# Tue, 28 Jan 2025 17:39:44 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
# ARGS: LIBERTY_VERSION=25.0.0.1 LIBERTY_SHA=f889eab11f1ef7ece29dac622d2842208aa602c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.1/openliberty-runtime-25.0.0.1.zip LIBERTY_BUILD_LABEL=cl250120250113-0302 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
# ARGS: LIBERTY_VERSION=25.0.0.1 LIBERTY_SHA=f889eab11f1ef7ece29dac622d2842208aa602c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.1/openliberty-runtime-25.0.0.1.zip LIBERTY_BUILD_LABEL=cl250120250113-0302 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 28 Jan 2025 17:39:44 GMT
# ARGS: LIBERTY_VERSION=25.0.0.1 LIBERTY_SHA=f889eab11f1ef7ece29dac622d2842208aa602c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.1/openliberty-runtime-25.0.0.1.zip LIBERTY_BUILD_LABEL=cl250120250113-0302 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
# ARGS: LIBERTY_VERSION=25.0.0.1 LIBERTY_SHA=f889eab11f1ef7ece29dac622d2842208aa602c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.1/openliberty-runtime-25.0.0.1.zip LIBERTY_BUILD_LABEL=cl250120250113-0302 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
# ARGS: LIBERTY_VERSION=25.0.0.1 LIBERTY_SHA=f889eab11f1ef7ece29dac622d2842208aa602c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.1/openliberty-runtime-25.0.0.1.zip LIBERTY_BUILD_LABEL=cl250120250113-0302 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 28 Jan 2025 17:39:44 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 28 Jan 2025 17:39:44 GMT
USER 1001
# Tue, 28 Jan 2025 17:39:44 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 28 Jan 2025 17:39:44 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 28 Jan 2025 17:39:44 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:7ed94a91c4e77c2e320a028b45fcefc9419c4df2b3d6494bf92ab5d08bba4d77`  
		Last Modified: Tue, 04 Feb 2025 06:45:54 GMT  
		Size: 28.0 MB (28000931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9a504edea95fbee01cd3ff3d84972a695acb9423b1d0fea8abc1fa3cac5e26`  
		Last Modified: Wed, 05 Feb 2025 08:43:39 GMT  
		Size: 12.2 MB (12212279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0aa1bc40cc106905638b838296fa7de7092f86654308debe68babf80c703434`  
		Last Modified: Wed, 05 Feb 2025 04:02:53 GMT  
		Size: 50.3 MB (50340171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9037b9148ccd1f5e7a38e08fb323f0ece8f2d364a6983cd576fb0dc5207086`  
		Last Modified: Mon, 10 Feb 2025 18:39:03 GMT  
		Size: 4.4 MB (4363104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36219a166c81e6e6c7fa63d2aea2ebb96f6878f32c7b8b198ea246da6fb46d2e`  
		Last Modified: Wed, 05 Feb 2025 04:02:55 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998bd4d23ab28b7aa31391410e12f99af1902529ab2a2656faed2e74ecb6e025`  
		Last Modified: Mon, 10 Feb 2025 18:39:02 GMT  
		Size: 10.1 KB (10111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b10f1572243c09d39c176d3027522ca8c1af9f7b642421ecf7157fec0509919`  
		Last Modified: Wed, 05 Feb 2025 08:44:22 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b9d0d1495feff9ef90bfae49b33d8b3b99ca96430fdd24f1d52d9b3be203eb`  
		Last Modified: Mon, 10 Feb 2025 18:39:04 GMT  
		Size: 33.1 KB (33113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a8d8c0589e6f0fdc6f9ed2c9b8c150529947fe3c81b0b9e645070c0ba1ad8c`  
		Last Modified: Wed, 05 Feb 2025 08:44:31 GMT  
		Size: 336.9 MB (336891386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12953b1b11b5ba2b7800287f1a8be9434bfdc3684c065d308b07ad3b7d9e38bb`  
		Last Modified: Mon, 10 Feb 2025 18:39:05 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51e0c9a2fd23192f9c39b17d7ff49636fb2fb312b3f5e589dfcbfc2b6eaec59`  
		Last Modified: Wed, 05 Feb 2025 08:44:51 GMT  
		Size: 11.5 KB (11477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c62c23c245c1bae3cc4848e2edc97a6816ecb07e9eef0162a826e0295b5a62`  
		Last Modified: Mon, 10 Feb 2025 18:39:07 GMT  
		Size: 13.4 MB (13387797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full` - unknown; unknown

```console
$ docker pull open-liberty@sha256:439f3b80b91dec4502f5fc6d311c547ccee6ebc1ab5695212c1986c753a5c4c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5576935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720af15c42f5783e1ac8bb4bc723ecfffcab1931b569d5dfec3645b379877bf4`

```dockerfile
```

-	Layers:
	-	`sha256:f9472967fa67157c933a34d0548cc1976625386c52600f33f4168c387b5f06dd`  
		Last Modified: Mon, 10 Feb 2025 18:39:29 GMT  
		Size: 5.5 MB (5537619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d708298acf9b59561798c97c69cf1934c4845254c52f303a805c00e0d2d49af4`  
		Last Modified: Sat, 15 Feb 2025 00:47:22 GMT  
		Size: 39.3 KB (39316 bytes)  
		MIME: application/vnd.in-toto+json
