## `open-liberty:beta`

```console
$ docker pull open-liberty@sha256:229b4b7ee12e17e7eaf79ead0b187d14800cc3787600c2331fd38b00d2a6ea46
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
$ docker pull open-liberty@sha256:9b8fbe68ae0ed6ad1d6d363cb6a975adad9c080a79b9104ab27fef8c4c239246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.1 MB (451111618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ae104346afe7151ab5db58aa22ff903d519a3902638a583abb4560102f5485`
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
# Tue, 04 Jun 2024 05:42:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jun 2024 05:42:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_VERSION=jdk8u412-b08_openj9-0.44.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='08a41a48b79881590d65a09c62c56d8bcd9b8453f03420bcfd5dd3165bbba3c1';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='a15f8041250126c9f20e52f8877fea80e20219635811b59bf537bce756f75a09';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ac5022b52b33b22c51d8370655f6157fd999e5e24c6525f91d1e778f34abcb8b';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='2c5bb442ebf64d695f78c10687477ee15bf7037332ac6cbd8d71d763593f64dc';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
USER root
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_VERSION=24.0.0.7-beta
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_SHA=ced06392041d7ba439b48bdcb8f8400c0542e064
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.7-beta/openliberty-runtime-24.0.0.7-beta.zip
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_BUILD_LABEL=cl240620240603-2001
# Tue, 18 Jun 2024 19:00:56 GMT
ARG OPENJ9_SCC=true
# Tue, 18 Jun 2024 19:00:56 GMT
ARG VERBOSE=false
# Tue, 18 Jun 2024 19:00:56 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240620240603-2001 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=24.0.0.7-beta
# Tue, 18 Jun 2024 19:00:56 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7-beta LIBERTY_SHA=ced06392041d7ba439b48bdcb8f8400c0542e064 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.7-beta/openliberty-runtime-24.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7-beta LIBERTY_SHA=ced06392041d7ba439b48bdcb8f8400c0542e064 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.7-beta/openliberty-runtime-24.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7-beta LIBERTY_SHA=ced06392041d7ba439b48bdcb8f8400c0542e064 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.7-beta/openliberty-runtime-24.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7-beta LIBERTY_SHA=ced06392041d7ba439b48bdcb8f8400c0542e064 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.7-beta/openliberty-runtime-24.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7-beta LIBERTY_SHA=ced06392041d7ba439b48bdcb8f8400c0542e064 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.7-beta/openliberty-runtime-24.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
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
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf8ca7ede3a61286a327ee6fbb96aad14a0ab4e5635404a61b12aa9f68ac1d3`  
		Last Modified: Tue, 25 Jun 2024 22:57:40 GMT  
		Size: 12.2 MB (12156362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d05cad4bbcfdca7f05999a893e3b7319067f0e62ae382da8cb30d68fe26722d`  
		Last Modified: Tue, 25 Jun 2024 22:57:41 GMT  
		Size: 50.4 MB (50447690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3953a2ec11a58421ca7f41ec863a500870b5cd5d89cb1274d2adaa970b4fb277`  
		Last Modified: Tue, 25 Jun 2024 22:57:40 GMT  
		Size: 4.2 MB (4179237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f3820919520b84e0a249b0f5ba4bbee94063092308e1a147d2d2da0170d52f`  
		Last Modified: Tue, 25 Jun 2024 23:56:37 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68628182b99558464a7d8db8832f5722e6e6583af66582fd8783cee5679336c6`  
		Last Modified: Tue, 25 Jun 2024 23:56:37 GMT  
		Size: 10.0 KB (9993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46ca8bd9ebf15d9d346117b68416fbe96f706d369f4083791b774cb115cc498`  
		Last Modified: Tue, 25 Jun 2024 23:56:37 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170a3951fa7e032ac8eb3d2d6350667348ae5b94e1110b322e58772de8ebb377`  
		Last Modified: Tue, 25 Jun 2024 23:56:37 GMT  
		Size: 31.7 KB (31746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9567425febf6e2822f13bb18232356acc84f48582af558ab436c2925573c3d6`  
		Last Modified: Tue, 25 Jun 2024 23:56:45 GMT  
		Size: 341.5 MB (341474374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0481a9f8cfb3e60f099762ba76382933fa5e4a2e5923908b1cf8948ebaabc0d`  
		Last Modified: Tue, 25 Jun 2024 23:56:38 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10c6406379d43e8586524db2991e4348b3648694b23c6ff2304fb4aab447b2d`  
		Last Modified: Tue, 25 Jun 2024 23:56:38 GMT  
		Size: 11.4 KB (11360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc5a0fa402f850c4e92e37563c72c5a8c95df5882bd4a9ffc387293ce3a0e04`  
		Last Modified: Tue, 25 Jun 2024 23:56:41 GMT  
		Size: 13.3 MB (13264754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta` - unknown; unknown

```console
$ docker pull open-liberty@sha256:97114534c54ded7ce55e5c63b1cb221563ae1826e1d2ab20425d2081440bd2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5200833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:796a352bb14c2e05e89ec3c0cf6f2eb1c035e85a730999a9a6a5c74aca36f1b3`

```dockerfile
```

-	Layers:
	-	`sha256:6a2751b93035afc1b99533ee79218d3fc7665fc6237ecf7d929e29aabbd3a8e6`  
		Last Modified: Tue, 25 Jun 2024 23:56:37 GMT  
		Size: 5.2 MB (5162198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:320f8e1da59608de45ae79897c65ac7e1b5004ff444c22686fff557b758b3f89`  
		Last Modified: Tue, 25 Jun 2024 23:56:37 GMT  
		Size: 38.6 KB (38635 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:24fb44e0b1b276acf382fcbead5dd517c8590e3110217bfa4ba9cf53964190cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.5 MB (447498565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52b838e2a0ea8e4430bd44d901e712cdaa54f7fef0b504eeb05246d61e70906`
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
# Tue, 04 Jun 2024 05:42:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jun 2024 05:42:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_VERSION=jdk8u412-b08_openj9-0.44.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='08a41a48b79881590d65a09c62c56d8bcd9b8453f03420bcfd5dd3165bbba3c1';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='a15f8041250126c9f20e52f8877fea80e20219635811b59bf537bce756f75a09';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ac5022b52b33b22c51d8370655f6157fd999e5e24c6525f91d1e778f34abcb8b';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='2c5bb442ebf64d695f78c10687477ee15bf7037332ac6cbd8d71d763593f64dc';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
USER root
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_VERSION=24.0.0.7-beta
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_SHA=ced06392041d7ba439b48bdcb8f8400c0542e064
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.7-beta/openliberty-runtime-24.0.0.7-beta.zip
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_BUILD_LABEL=cl240620240603-2001
# Tue, 18 Jun 2024 19:00:56 GMT
ARG OPENJ9_SCC=true
# Tue, 18 Jun 2024 19:00:56 GMT
ARG VERBOSE=false
# Tue, 18 Jun 2024 19:00:56 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240620240603-2001 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=24.0.0.7-beta
# Tue, 18 Jun 2024 19:00:56 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7-beta LIBERTY_SHA=ced06392041d7ba439b48bdcb8f8400c0542e064 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.7-beta/openliberty-runtime-24.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7-beta LIBERTY_SHA=ced06392041d7ba439b48bdcb8f8400c0542e064 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.7-beta/openliberty-runtime-24.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7-beta LIBERTY_SHA=ced06392041d7ba439b48bdcb8f8400c0542e064 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.7-beta/openliberty-runtime-24.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7-beta LIBERTY_SHA=ced06392041d7ba439b48bdcb8f8400c0542e064 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.7-beta/openliberty-runtime-24.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7-beta LIBERTY_SHA=ced06392041d7ba439b48bdcb8f8400c0542e064 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.7-beta/openliberty-runtime-24.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
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
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ee6e790fe3be315f574c78a35fef5e2104480be37cd385884a99abf457a751`  
		Last Modified: Tue, 25 Jun 2024 23:02:58 GMT  
		Size: 12.1 MB (12115683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab03bc76208f1733b763057b8af20767123d2024ceb38337869d0c174fa64741`  
		Last Modified: Tue, 25 Jun 2024 23:06:57 GMT  
		Size: 49.7 MB (49726246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7b1f6abb0dc3856dbfe8487bece748873ebb39250a2b6f011d2cfa9076ec75`  
		Last Modified: Tue, 25 Jun 2024 23:06:55 GMT  
		Size: 4.0 MB (4029287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef83a1148e9da5915f811be2d3841d398f2af6c1abb531505cf4b5107e650cf`  
		Last Modified: Wed, 26 Jun 2024 00:45:37 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97152833bf7ff0cdb8aa397c1756ac3897c7b74e3659afe942e69c554f2233e3`  
		Last Modified: Wed, 26 Jun 2024 00:45:37 GMT  
		Size: 10.0 KB (9989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54418c4817cc1afd642a915ba7f1eba4c1c2c9e5d33e7aeb73664699451b6cc`  
		Last Modified: Wed, 26 Jun 2024 00:45:37 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc93b977b56d9964b37e632d9f6edad2f9c36ed5c57bab041e6289868ed807b7`  
		Last Modified: Wed, 26 Jun 2024 00:45:37 GMT  
		Size: 42.3 KB (42324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2eb9f32b50bfd5b5971eeafa85c6ebda4994830c83de13f83ad75ee841a64e`  
		Last Modified: Wed, 26 Jun 2024 00:45:46 GMT  
		Size: 341.5 MB (341476184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832504a8db44bd2192ef2de1fbd0609519e4d5ec41695e18be6dc374c4da524c`  
		Last Modified: Wed, 26 Jun 2024 00:45:38 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4778e5a5d00c2088f2199e7c4ea352d3bf6357b043351ebbecfd4e3cb46d96`  
		Last Modified: Wed, 26 Jun 2024 00:45:38 GMT  
		Size: 11.3 KB (11346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715235b0867fe523d33dc5d5252934275c7b99f2670964af5f080783e00395b4`  
		Last Modified: Wed, 26 Jun 2024 00:45:39 GMT  
		Size: 12.7 MB (12723377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta` - unknown; unknown

```console
$ docker pull open-liberty@sha256:ae9caa97325c2501b9cbf7181c2c0cd188c1bfb9710c2014f0534f5962a3148e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5201435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff15e14eee3e3034771527d46ba85b3b9d517d8a86bb4c8dc91ea2501a13ff1`

```dockerfile
```

-	Layers:
	-	`sha256:de042bf3e0b153f3ca8803445f3ef430d6493e2d615f1e299c4f481c5ec7b3cf`  
		Last Modified: Wed, 26 Jun 2024 00:45:37 GMT  
		Size: 5.2 MB (5162451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4481fee927e8854eb2edd6553df959074da75de618ca3aa9ebb47dd9735dcd3d`  
		Last Modified: Wed, 26 Jun 2024 00:45:37 GMT  
		Size: 39.0 KB (38984 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:dfbdfe55572f07a34777ba2a9c52b761d48428806009934ae4b07c15e85e4b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.7 MB (455741583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92a4f134c7ec512ee65d9ad7bf9bfa0ce0a22826092e2a21d145c3da49548e5`
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
# Tue, 04 Jun 2024 05:42:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jun 2024 05:42:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_VERSION=jdk8u412-b08_openj9-0.44.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='08a41a48b79881590d65a09c62c56d8bcd9b8453f03420bcfd5dd3165bbba3c1';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='a15f8041250126c9f20e52f8877fea80e20219635811b59bf537bce756f75a09';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ac5022b52b33b22c51d8370655f6157fd999e5e24c6525f91d1e778f34abcb8b';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='2c5bb442ebf64d695f78c10687477ee15bf7037332ac6cbd8d71d763593f64dc';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
USER root
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_VERSION=24.0.0.7-beta
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_SHA=ced06392041d7ba439b48bdcb8f8400c0542e064
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.7-beta/openliberty-runtime-24.0.0.7-beta.zip
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_BUILD_LABEL=cl240620240603-2001
# Tue, 18 Jun 2024 19:00:56 GMT
ARG OPENJ9_SCC=true
# Tue, 18 Jun 2024 19:00:56 GMT
ARG VERBOSE=false
# Tue, 18 Jun 2024 19:00:56 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240620240603-2001 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=24.0.0.7-beta
# Tue, 18 Jun 2024 19:00:56 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7-beta LIBERTY_SHA=ced06392041d7ba439b48bdcb8f8400c0542e064 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.7-beta/openliberty-runtime-24.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7-beta LIBERTY_SHA=ced06392041d7ba439b48bdcb8f8400c0542e064 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.7-beta/openliberty-runtime-24.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7-beta LIBERTY_SHA=ced06392041d7ba439b48bdcb8f8400c0542e064 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.7-beta/openliberty-runtime-24.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7-beta LIBERTY_SHA=ced06392041d7ba439b48bdcb8f8400c0542e064 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.7-beta/openliberty-runtime-24.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7-beta LIBERTY_SHA=ced06392041d7ba439b48bdcb8f8400c0542e064 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.7-beta/openliberty-runtime-24.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
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
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c866879b3eaab6a2be320ab73cc032a3c43ef798a2582028559e9055cc257b5`  
		Last Modified: Tue, 25 Jun 2024 23:04:25 GMT  
		Size: 12.9 MB (12887989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf752268dcc3e42bae3741522daa6d8766a35ad8ce78ac1c5c5ef1cd262b074`  
		Last Modified: Tue, 25 Jun 2024 23:09:29 GMT  
		Size: 51.7 MB (51706131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714bb245874efc0453ccb03cc20a96065bba04d33c97e32007a7293cb01ab74a`  
		Last Modified: Tue, 25 Jun 2024 23:09:27 GMT  
		Size: 3.5 MB (3460998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4629a403065cf08e7829d5c4c017b8de35c78ea79ce4869946796431e000038`  
		Last Modified: Wed, 26 Jun 2024 01:32:48 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1b3a5adc7c83bf63e8f2e663f33856147a717b2fbcbfc6e93867bb0c66c203`  
		Last Modified: Wed, 26 Jun 2024 01:32:48 GMT  
		Size: 10.0 KB (9992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52fa1b03f91b88f721a3fc9f9c6e1456d3a8572fb1ad38e7b1f298c73eb7a48`  
		Last Modified: Wed, 26 Jun 2024 01:32:48 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd07b7ad51922c89fbfd78029f9810efd53e5b32c6173852559d0608d87d507e`  
		Last Modified: Wed, 26 Jun 2024 01:32:48 GMT  
		Size: 36.5 KB (36496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d50a937bb74b9135f01b4d25cca6c9cb1f039569bdbbf58e0683a7d057e63d`  
		Last Modified: Wed, 26 Jun 2024 01:32:58 GMT  
		Size: 341.5 MB (341475013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f690ff86e276ddce08b8041155efb81eafd2de017464475f1009bffb8a300a73`  
		Last Modified: Wed, 26 Jun 2024 01:32:49 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e210748a15ac3ceb76b217e71f8c1c6859a3c03d6063d507ced461017ba67770`  
		Last Modified: Wed, 26 Jun 2024 01:32:49 GMT  
		Size: 11.4 KB (11358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b9ef570a47e08dc4034df07c651fccffcd8bbe26ca8d6f3211e0bb1c899065`  
		Last Modified: Wed, 26 Jun 2024 01:32:50 GMT  
		Size: 11.7 MB (11690566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta` - unknown; unknown

```console
$ docker pull open-liberty@sha256:6ca96cc0610402204a243f719bda0fa4ee2605d8f0318e0b207b686b8214f4f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78268a768cdeb18a8cf9a963e299d88649fea4f8b99ce888955391e4c6cec0d1`

```dockerfile
```

-	Layers:
	-	`sha256:b4b1a5665e7274cb8b5c9cd8912e2adbcafeea582f9d4ea00ac7cc3ed07e5c7d`  
		Last Modified: Wed, 26 Jun 2024 01:32:48 GMT  
		Size: 5.2 MB (5166680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:559bb348fa48bc731ab9e291260fb0583f4e88fc414c29a85fa8af3b8918047e`  
		Last Modified: Wed, 26 Jun 2024 01:32:48 GMT  
		Size: 38.7 KB (38669 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta` - linux; s390x

```console
$ docker pull open-liberty@sha256:99df46dc5e10fe576e82ef1d197365505b0910bc801f2116aeee3c1ba122c0a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.6 MB (449616977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2251f058ac24b1b8de62de0e9aa17cae5fda87c2ab1f5b05171b8300addf0e6e`
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
# Tue, 04 Jun 2024 05:42:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jun 2024 05:42:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_VERSION=jdk8u412-b08_openj9-0.44.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='08a41a48b79881590d65a09c62c56d8bcd9b8453f03420bcfd5dd3165bbba3c1';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='a15f8041250126c9f20e52f8877fea80e20219635811b59bf537bce756f75a09';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ac5022b52b33b22c51d8370655f6157fd999e5e24c6525f91d1e778f34abcb8b';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='2c5bb442ebf64d695f78c10687477ee15bf7037332ac6cbd8d71d763593f64dc';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u412-b08_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_8u412b08_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
USER root
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_VERSION=24.0.0.7-beta
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_SHA=ced06392041d7ba439b48bdcb8f8400c0542e064
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.7-beta/openliberty-runtime-24.0.0.7-beta.zip
# Tue, 18 Jun 2024 19:00:56 GMT
ARG LIBERTY_BUILD_LABEL=cl240620240603-2001
# Tue, 18 Jun 2024 19:00:56 GMT
ARG OPENJ9_SCC=true
# Tue, 18 Jun 2024 19:00:56 GMT
ARG VERBOSE=false
# Tue, 18 Jun 2024 19:00:56 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl240620240603-2001 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=24.0.0.7-beta
# Tue, 18 Jun 2024 19:00:56 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7-beta LIBERTY_SHA=ced06392041d7ba439b48bdcb8f8400c0542e064 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.7-beta/openliberty-runtime-24.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7-beta LIBERTY_SHA=ced06392041d7ba439b48bdcb8f8400c0542e064 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.7-beta/openliberty-runtime-24.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7-beta LIBERTY_SHA=ced06392041d7ba439b48bdcb8f8400c0542e064 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.7-beta/openliberty-runtime-24.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7-beta LIBERTY_SHA=ced06392041d7ba439b48bdcb8f8400c0542e064 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.7-beta/openliberty-runtime-24.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 18 Jun 2024 19:00:56 GMT
# ARGS: LIBERTY_VERSION=24.0.0.7-beta LIBERTY_SHA=ced06392041d7ba439b48bdcb8f8400c0542e064 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.7-beta/openliberty-runtime-24.0.0.7-beta.zip LIBERTY_BUILD_LABEL=cl240620240603-2001 OPENJ9_SCC=true VERBOSE=false
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
	-	`sha256:22512bbfe178a8ec7b5e4e48135f8a3e1ad0245ed3ee6a47f89947ce7ffb5d4f`  
		Last Modified: Mon, 03 Jun 2024 10:47:11 GMT  
		Size: 28.0 MB (28000515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7a4135208bd6a1c83ef4006ee13da7687af58d5df19772a183b62d4757a473`  
		Last Modified: Tue, 25 Jun 2024 23:02:32 GMT  
		Size: 12.2 MB (12203759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6055af015dffee15f993954476c262757af959102f4c9e6b46f2e81533f44e7`  
		Last Modified: Tue, 25 Jun 2024 23:05:05 GMT  
		Size: 50.2 MB (50232698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46220f4d63cae95ccd7a4a5086f504bb90ded4e860063d175030bd30515fd2f1`  
		Last Modified: Tue, 25 Jun 2024 23:05:03 GMT  
		Size: 4.3 MB (4322698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad86656f781a8782ccfec09d6a0c872b14a2b4d806bdea689672c7c734980347`  
		Last Modified: Tue, 25 Jun 2024 23:56:40 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0851a16ff25691efd94109b6c2ac386c9d0ef44778b9be9d80490a4409a43ef`  
		Last Modified: Tue, 25 Jun 2024 23:56:40 GMT  
		Size: 10.0 KB (9992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc101dcb2bfe2194068e3f4e58d8d4315939d2f0deb8e2d9f3f67d3b8f5882b`  
		Last Modified: Tue, 25 Jun 2024 23:56:40 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2fce535f0ed03064a1deeac6647e03e3d93e0f325541b4e318d733060b559b`  
		Last Modified: Tue, 25 Jun 2024 23:56:40 GMT  
		Size: 33.1 KB (33110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bdf016a2aff472312a895517ec2fb75f2c9012a01f1cee8c8427a2c239c4852`  
		Last Modified: Tue, 25 Jun 2024 23:56:46 GMT  
		Size: 341.5 MB (341474577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b395edebe63864b23cfd604552a9cdb37d284887157515d7dbf54e8be35e9f5e`  
		Last Modified: Tue, 25 Jun 2024 23:56:41 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281f199711bb8f19e928b646133a6808febb9f89e081af6c64901fd455c2671c`  
		Last Modified: Tue, 25 Jun 2024 23:56:41 GMT  
		Size: 11.3 KB (11350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0453a20b7e6b3b9431b7624cf773a85c59efe58896a2235ec18b35aefa89d7b5`  
		Last Modified: Tue, 25 Jun 2024 23:56:43 GMT  
		Size: 13.3 MB (13325934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta` - unknown; unknown

```console
$ docker pull open-liberty@sha256:87d84cf340314fe003035057e2ff5510bcdc29454d1c89305d20fb14dfa68788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5201152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73224971b481163af20b64cf073bf3d7e682f9d2ef1d0abab6ecb896c42aa817`

```dockerfile
```

-	Layers:
	-	`sha256:bae716f241209722d277940b0b9153eb50e5425f404083db7e0bd74d2e39360d`  
		Last Modified: Tue, 25 Jun 2024 23:56:40 GMT  
		Size: 5.2 MB (5162517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dbf0f390880f4f3eac2e7638afb0a0849eecaa6375ce56a8ca9831f89520022`  
		Last Modified: Tue, 25 Jun 2024 23:56:40 GMT  
		Size: 38.6 KB (38635 bytes)  
		MIME: application/vnd.in-toto+json
