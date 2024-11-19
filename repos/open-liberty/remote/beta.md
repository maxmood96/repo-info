## `open-liberty:beta`

```console
$ docker pull open-liberty@sha256:64838f5e905f1a0a2bbf66bb9553f9b06232fb4489f50fc2a3005f10d82343fe
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
$ docker pull open-liberty@sha256:b38fefe3e8add95d46e78aead3ce802b1d428a2e222c18f03e77690964b2a68d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **469.5 MB (469529635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee7a9b18649165cae04da1c6670ff2e485424a849ec3fcfbe9bc1588bd9403e`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Wed, 06 Nov 2024 14:56:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Nov 2024 14:56:24 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
ENV JAVA_VERSION=jdk8u432-b06_openj9-0.48.0
# Wed, 06 Nov 2024 14:56:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='01e57b0ada3dc34b08d2f4644b64244f7a1e9a63cf885f47b9baadf663230b5d';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jre_aarch64_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8ba759756722e415ae011bee0c4045f38e2b8e15535488944420fb8c1932d710';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jre_ppc64le_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b38ef6c7520463822affa424b4ad0e16686b86b01255b0c9912743d3f6e98a73';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jre_x64_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='5bcb556f2cd0352c14205321afdeac37615249f874ae37e84601287f5eb5be5b';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jre_s390x_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 14:56:24 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 06 Nov 2024 14:56:24 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="537dbbfc03b37312c2ec282c6906828298cb74e42aca6e3e6835d44bf6923fd8c5db77e98bf6ce9ef19e1922729de53b20546149176e07ac04087df786a62fd9";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.97/bin/apache-tomcat-9.0.97.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
USER root
# Wed, 06 Nov 2024 14:56:24 GMT
ARG LIBERTY_VERSION=24.0.0.12-beta
# Wed, 06 Nov 2024 14:56:24 GMT
ARG LIBERTY_SHA=f390f288633eef7667b16301f3928462d5d39e57
# Wed, 06 Nov 2024 14:56:24 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.12-beta/openliberty-runtime-24.0.0.12-beta.zip
# Wed, 06 Nov 2024 14:56:24 GMT
ARG LIBERTY_BUILD_LABEL=cl241120241021-1102
# Wed, 06 Nov 2024 14:56:24 GMT
ARG OPENJ9_SCC=true
# Wed, 06 Nov 2024 14:56:24 GMT
ARG VERBOSE=false
# Wed, 06 Nov 2024 14:56:24 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl241120241021-1102 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=24.0.0.12-beta
# Wed, 06 Nov 2024 14:56:24 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12-beta LIBERTY_SHA=f390f288633eef7667b16301f3928462d5d39e57 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.12-beta/openliberty-runtime-24.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl241120241021-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12-beta LIBERTY_SHA=f390f288633eef7667b16301f3928462d5d39e57 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.12-beta/openliberty-runtime-24.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl241120241021-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 06 Nov 2024 14:56:24 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12-beta LIBERTY_SHA=f390f288633eef7667b16301f3928462d5d39e57 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.12-beta/openliberty-runtime-24.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl241120241021-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12-beta LIBERTY_SHA=f390f288633eef7667b16301f3928462d5d39e57 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.12-beta/openliberty-runtime-24.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl241120241021-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12-beta LIBERTY_SHA=f390f288633eef7667b16301f3928462d5d39e57 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.12-beta/openliberty-runtime-24.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl241120241021-1102 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 06 Nov 2024 14:56:24 GMT
USER 1001
# Wed, 06 Nov 2024 14:56:24 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 06 Nov 2024 14:56:24 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 06 Nov 2024 14:56:24 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f31ffe48b9539638a827b1414527ddeaa2cb45ebfb6dbbd79d00fc15168264a`  
		Last Modified: Mon, 18 Nov 2024 19:05:52 GMT  
		Size: 12.2 MB (12175054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2606e243aef7b7b748f682673d86c7aa62b9d50df576349801ba14c7c99a21`  
		Last Modified: Mon, 18 Nov 2024 19:05:53 GMT  
		Size: 50.4 MB (50401662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda771d4f2cbdc37bda45ffe7802662a4e734721e0f0655384ef6f9675281e01`  
		Last Modified: Mon, 18 Nov 2024 19:05:52 GMT  
		Size: 4.3 MB (4259877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83aa27f734b735575b50c7aa44286b68ee04cdb965da36ef8786de2ae3dfaf41`  
		Last Modified: Mon, 18 Nov 2024 20:09:01 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f449f61384de1f12c0d51420d60e8089e371e86a5ffadb6759bcb593fe277d`  
		Last Modified: Mon, 18 Nov 2024 20:09:01 GMT  
		Size: 10.0 KB (9984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8deb540e8c51b20593262a51c47a0ffe327efc533d709c0077689c126c4caa0d`  
		Last Modified: Mon, 18 Nov 2024 20:09:01 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c8db43e1b8836c3e15b272eadbc9773756be5723cbe4ff537923bb84167988`  
		Last Modified: Mon, 18 Nov 2024 20:09:01 GMT  
		Size: 31.7 KB (31748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5771fa1f6557b76e5065bff26633ab6dd77a9506a86263dac0b1cb3b4157600e`  
		Last Modified: Mon, 18 Nov 2024 20:09:07 GMT  
		Size: 359.6 MB (359550911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81c8ecd6809f9539eb64e44b3faeae7fc6d283829e8a3bb00d49142fc714c07`  
		Last Modified: Mon, 18 Nov 2024 20:09:01 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6acd1709ed9956aea7c501aa5349ee8d03f79a3b6c97fa2520028a9e8cfa1c7`  
		Last Modified: Mon, 18 Nov 2024 20:09:02 GMT  
		Size: 11.3 KB (11334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9abad4b199ad9dbaa80b79332676d7a8a2b5ececc63d4b4aa7813a76fb8b6959`  
		Last Modified: Mon, 18 Nov 2024 20:09:02 GMT  
		Size: 13.6 MB (13551031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta` - unknown; unknown

```console
$ docker pull open-liberty@sha256:52dba5478b6fc39518953d6b5d70e050437ceccf07e4ca2c377b8c2c2547da7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5764614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cafa956c674e9467d1392046c58f161bc6adf3cc4be9aa40c9b4a7a76fb8d942`

```dockerfile
```

-	Layers:
	-	`sha256:c9970cb8917a68e01e91d7e4327ff1fd7406b2b730e9dda0eb2b56186db6c8bc`  
		Last Modified: Mon, 18 Nov 2024 20:09:01 GMT  
		Size: 5.7 MB (5725926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce31abb04a5841461cc4aa9b1ecd07318e609131b0e77cc10e5ac1833c6e08ff`  
		Last Modified: Mon, 18 Nov 2024 20:09:01 GMT  
		Size: 38.7 KB (38688 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:59eea7e8311d4d4c4fa6daa9ea69bdc6c5010fa172d7ab6eb92509036781c139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **465.9 MB (465885189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537be3a60a9c6f203d2feb9ab40dc7cbb66898109dd79e2f6e7d885f5d708ecb`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Wed, 06 Nov 2024 14:56:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Nov 2024 14:56:24 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
ENV JAVA_VERSION=jdk8u432-b06_openj9-0.48.0
# Wed, 06 Nov 2024 14:56:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='01e57b0ada3dc34b08d2f4644b64244f7a1e9a63cf885f47b9baadf663230b5d';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jre_aarch64_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8ba759756722e415ae011bee0c4045f38e2b8e15535488944420fb8c1932d710';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jre_ppc64le_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b38ef6c7520463822affa424b4ad0e16686b86b01255b0c9912743d3f6e98a73';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jre_x64_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='5bcb556f2cd0352c14205321afdeac37615249f874ae37e84601287f5eb5be5b';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jre_s390x_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 14:56:24 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 06 Nov 2024 14:56:24 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="537dbbfc03b37312c2ec282c6906828298cb74e42aca6e3e6835d44bf6923fd8c5db77e98bf6ce9ef19e1922729de53b20546149176e07ac04087df786a62fd9";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.97/bin/apache-tomcat-9.0.97.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
USER root
# Wed, 06 Nov 2024 14:56:24 GMT
ARG LIBERTY_VERSION=24.0.0.12-beta
# Wed, 06 Nov 2024 14:56:24 GMT
ARG LIBERTY_SHA=f390f288633eef7667b16301f3928462d5d39e57
# Wed, 06 Nov 2024 14:56:24 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.12-beta/openliberty-runtime-24.0.0.12-beta.zip
# Wed, 06 Nov 2024 14:56:24 GMT
ARG LIBERTY_BUILD_LABEL=cl241120241021-1102
# Wed, 06 Nov 2024 14:56:24 GMT
ARG OPENJ9_SCC=true
# Wed, 06 Nov 2024 14:56:24 GMT
ARG VERBOSE=false
# Wed, 06 Nov 2024 14:56:24 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl241120241021-1102 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=24.0.0.12-beta
# Wed, 06 Nov 2024 14:56:24 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12-beta LIBERTY_SHA=f390f288633eef7667b16301f3928462d5d39e57 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.12-beta/openliberty-runtime-24.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl241120241021-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12-beta LIBERTY_SHA=f390f288633eef7667b16301f3928462d5d39e57 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.12-beta/openliberty-runtime-24.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl241120241021-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 06 Nov 2024 14:56:24 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12-beta LIBERTY_SHA=f390f288633eef7667b16301f3928462d5d39e57 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.12-beta/openliberty-runtime-24.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl241120241021-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12-beta LIBERTY_SHA=f390f288633eef7667b16301f3928462d5d39e57 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.12-beta/openliberty-runtime-24.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl241120241021-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12-beta LIBERTY_SHA=f390f288633eef7667b16301f3928462d5d39e57 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.12-beta/openliberty-runtime-24.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl241120241021-1102 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 06 Nov 2024 14:56:24 GMT
USER 1001
# Wed, 06 Nov 2024 14:56:24 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 06 Nov 2024 14:56:24 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 06 Nov 2024 14:56:24 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e2579fa9ed432452dd8563d1dc040de22c49fcfc4a3cd906b5e75b095c2926`  
		Last Modified: Mon, 18 Nov 2024 19:12:40 GMT  
		Size: 12.1 MB (12128239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c41bd0f748485e01d958dd11a2c5ba0dd06fc6d6ad311125a1146cad7f5cd4`  
		Last Modified: Mon, 18 Nov 2024 19:14:57 GMT  
		Size: 49.8 MB (49805628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5b70f8f50633e07f9d0c5a673ef1e56bad2c5f0c6e9fe78fa3a2535d6a5004`  
		Last Modified: Mon, 18 Nov 2024 19:14:55 GMT  
		Size: 4.1 MB (4050504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00661db8b3990b885c0d7b9e645b6cb3f723191573436471e13f095f1ac9acc`  
		Last Modified: Mon, 18 Nov 2024 20:48:56 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f6cd65bbe485c9238dd6212c96413b3c2dd5bb0696e75807a65ac7b0b1bd34`  
		Last Modified: Mon, 18 Nov 2024 20:48:56 GMT  
		Size: 10.0 KB (9982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861f4bf6201ed78260444986575484563decbb65d74215994f2714f46c85284c`  
		Last Modified: Mon, 18 Nov 2024 20:48:56 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8135ce44f2ae7a09ac638011675baf73ffae4bb87d4e603c04d48bf3e302262`  
		Last Modified: Mon, 18 Nov 2024 20:48:57 GMT  
		Size: 42.3 KB (42325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ec5e1f835b3b42eafbb98572b28a25bc3e0437c39b8047a19a03578785138a`  
		Last Modified: Mon, 18 Nov 2024 20:49:06 GMT  
		Size: 359.6 MB (359551274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1789d8394d90596fde578ad79f4be0bc4afcfaca2cf20269d36a47a60c92f35f`  
		Last Modified: Mon, 18 Nov 2024 20:48:57 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bcf7afa4d42c0ec23083c95ce743d95db7f31aa5c115f8012a0846cd09aa03`  
		Last Modified: Mon, 18 Nov 2024 20:48:57 GMT  
		Size: 11.3 KB (11337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6726093f0930864860ba35284b9908bba6e67612d1c231164ee7370091c1ca`  
		Last Modified: Mon, 18 Nov 2024 20:48:58 GMT  
		Size: 12.9 MB (12925224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta` - unknown; unknown

```console
$ docker pull open-liberty@sha256:85372eea3fcaff7eddd589656bce0ed8dea9b3508b37bebdd2be092165b77fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5764532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49057b12446b04e857dd05f8f7f00c764105cd5e9399def882a8dd7a6f107232`

```dockerfile
```

-	Layers:
	-	`sha256:574d0c73877c3714b8b259db5a1772d64de007fc79b7a482d4eb0bd43a58dd16`  
		Last Modified: Mon, 18 Nov 2024 20:48:56 GMT  
		Size: 5.7 MB (5725716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46feac05721a5e17e4af39af43900c2074eb0f9afb13649a32c3825560fa5e37`  
		Last Modified: Mon, 18 Nov 2024 20:48:56 GMT  
		Size: 38.8 KB (38816 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:80acb82c8482e63e2788c66eebb05379db557475f4f29a6fab50c0f91287bc43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **474.0 MB (474001332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23047762b01ffd412f5e723f1263704f3afb83c950f5394d4b8372c34506b966`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Wed, 06 Nov 2024 14:56:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Nov 2024 14:56:24 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
ENV JAVA_VERSION=jdk8u432-b06_openj9-0.48.0
# Wed, 06 Nov 2024 14:56:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='01e57b0ada3dc34b08d2f4644b64244f7a1e9a63cf885f47b9baadf663230b5d';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jre_aarch64_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8ba759756722e415ae011bee0c4045f38e2b8e15535488944420fb8c1932d710';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jre_ppc64le_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b38ef6c7520463822affa424b4ad0e16686b86b01255b0c9912743d3f6e98a73';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jre_x64_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='5bcb556f2cd0352c14205321afdeac37615249f874ae37e84601287f5eb5be5b';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jre_s390x_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 14:56:24 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 06 Nov 2024 14:56:24 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="537dbbfc03b37312c2ec282c6906828298cb74e42aca6e3e6835d44bf6923fd8c5db77e98bf6ce9ef19e1922729de53b20546149176e07ac04087df786a62fd9";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.97/bin/apache-tomcat-9.0.97.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
USER root
# Wed, 06 Nov 2024 14:56:24 GMT
ARG LIBERTY_VERSION=24.0.0.12-beta
# Wed, 06 Nov 2024 14:56:24 GMT
ARG LIBERTY_SHA=f390f288633eef7667b16301f3928462d5d39e57
# Wed, 06 Nov 2024 14:56:24 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.12-beta/openliberty-runtime-24.0.0.12-beta.zip
# Wed, 06 Nov 2024 14:56:24 GMT
ARG LIBERTY_BUILD_LABEL=cl241120241021-1102
# Wed, 06 Nov 2024 14:56:24 GMT
ARG OPENJ9_SCC=true
# Wed, 06 Nov 2024 14:56:24 GMT
ARG VERBOSE=false
# Wed, 06 Nov 2024 14:56:24 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl241120241021-1102 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=24.0.0.12-beta
# Wed, 06 Nov 2024 14:56:24 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12-beta LIBERTY_SHA=f390f288633eef7667b16301f3928462d5d39e57 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.12-beta/openliberty-runtime-24.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl241120241021-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12-beta LIBERTY_SHA=f390f288633eef7667b16301f3928462d5d39e57 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.12-beta/openliberty-runtime-24.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl241120241021-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 06 Nov 2024 14:56:24 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12-beta LIBERTY_SHA=f390f288633eef7667b16301f3928462d5d39e57 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.12-beta/openliberty-runtime-24.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl241120241021-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12-beta LIBERTY_SHA=f390f288633eef7667b16301f3928462d5d39e57 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.12-beta/openliberty-runtime-24.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl241120241021-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12-beta LIBERTY_SHA=f390f288633eef7667b16301f3928462d5d39e57 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.12-beta/openliberty-runtime-24.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl241120241021-1102 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 06 Nov 2024 14:56:24 GMT
USER 1001
# Wed, 06 Nov 2024 14:56:24 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 06 Nov 2024 14:56:24 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 06 Nov 2024 14:56:24 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6230a31e14b4a918b32fc7a3b685fad8ecafe0901deee916736d3e6f4db6ad`  
		Last Modified: Tue, 17 Sep 2024 01:15:01 GMT  
		Size: 12.9 MB (12888132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a5a7c9cd6661827c230668595f63add950a51562dba611f5487e5245c34349`  
		Last Modified: Mon, 18 Nov 2024 19:11:30 GMT  
		Size: 51.8 MB (51803594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953dd616e57e58d02e661b6de760cb07b4cd411c3331bfdb333c8a1a5f2b2ab4`  
		Last Modified: Mon, 18 Nov 2024 19:11:29 GMT  
		Size: 3.5 MB (3463117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4268661b4f61086692cc7d1f825699cc923ef472070650d79479076dc02cc7aa`  
		Last Modified: Tue, 19 Nov 2024 00:04:52 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2b63d6891c51dba90c417e0c019c23de26565dceb99d3f60dd225d2f9b5d03`  
		Last Modified: Tue, 19 Nov 2024 00:04:52 GMT  
		Size: 10.0 KB (9988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5f171ef968b36ff424090ab3b3b4def8afc488a54a5e2ea8916bf96c1eae84`  
		Last Modified: Tue, 19 Nov 2024 00:04:52 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86705ffbe56770a98d07c4c7789e51a2bba8668c8f9d3a857f26974a2d36d96`  
		Last Modified: Tue, 19 Nov 2024 00:04:52 GMT  
		Size: 36.5 KB (36500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a345dbb78c3358d1c4318ab25a25e3223ce9283f30e495d98bcf62ec72a154`  
		Last Modified: Tue, 19 Nov 2024 00:05:04 GMT  
		Size: 359.6 MB (359551635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c539483691c9021d64e4f0b2404d05a07750f6c183a608667aaa7ce96f9814d`  
		Last Modified: Tue, 19 Nov 2024 00:04:53 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7ebebfd6e97d08968e51748b4aff07633cc7c18ad3c422df4495d7dd6a58d3`  
		Last Modified: Tue, 19 Nov 2024 00:04:53 GMT  
		Size: 11.3 KB (11347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6374f51e81130d8fa9a50deeed66f17d56c09c4c0109518ebc771488022f2027`  
		Last Modified: Tue, 19 Nov 2024 00:04:54 GMT  
		Size: 11.8 MB (11786424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta` - unknown; unknown

```console
$ docker pull open-liberty@sha256:db6a5952516084ef81cff4c8b304d445b3b64f29ec0fa5e7c151bd473a93d274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5763406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3d94f79d235fb6f235d453b20cf034a5631c641c948d25afb4a222bcc3de99d`

```dockerfile
```

-	Layers:
	-	`sha256:df00cc383989f23d58080029ada0d67daa0368e1213d107daeb0801aa38d64a0`  
		Last Modified: Tue, 19 Nov 2024 00:04:53 GMT  
		Size: 5.7 MB (5724684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ed5864a5d78a7d2f681065df0534c1081f60db6158879a62c854df4f6232c70`  
		Last Modified: Tue, 19 Nov 2024 00:04:52 GMT  
		Size: 38.7 KB (38722 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta` - linux; s390x

```console
$ docker pull open-liberty@sha256:69eb411c90b0870d2c3ae58e2b4d9702813fa672fbd4792abdc26f65d9efe782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.8 MB (467829575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43e62cf9bd159a8fafcefd2b09102a2265f8338e3efd2f1f12de32291b6668c`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:31 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:32 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 11 Sep 2024 16:25:32 GMT
CMD ["/bin/bash"]
# Wed, 06 Nov 2024 14:56:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Nov 2024 14:56:24 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
ENV JAVA_VERSION=jdk8u432-b06_openj9-0.48.0
# Wed, 06 Nov 2024 14:56:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='01e57b0ada3dc34b08d2f4644b64244f7a1e9a63cf885f47b9baadf663230b5d';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jre_aarch64_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='8ba759756722e415ae011bee0c4045f38e2b8e15535488944420fb8c1932d710';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jre_ppc64le_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b38ef6c7520463822affa424b4ad0e16686b86b01255b0c9912743d3f6e98a73';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jre_x64_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='5bcb556f2cd0352c14205321afdeac37615249f874ae37e84601287f5eb5be5b';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u432-b06_openj9-0.48.0/ibm-semeru-open-jre_s390x_linux_8u432b06_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 14:56:24 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 06 Nov 2024 14:56:24 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="537dbbfc03b37312c2ec282c6906828298cb74e42aca6e3e6835d44bf6923fd8c5db77e98bf6ce9ef19e1922729de53b20546149176e07ac04087df786a62fd9";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.97/bin/apache-tomcat-9.0.97.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
USER root
# Wed, 06 Nov 2024 14:56:24 GMT
ARG LIBERTY_VERSION=24.0.0.12-beta
# Wed, 06 Nov 2024 14:56:24 GMT
ARG LIBERTY_SHA=f390f288633eef7667b16301f3928462d5d39e57
# Wed, 06 Nov 2024 14:56:24 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.12-beta/openliberty-runtime-24.0.0.12-beta.zip
# Wed, 06 Nov 2024 14:56:24 GMT
ARG LIBERTY_BUILD_LABEL=cl241120241021-1102
# Wed, 06 Nov 2024 14:56:24 GMT
ARG OPENJ9_SCC=true
# Wed, 06 Nov 2024 14:56:24 GMT
ARG VERBOSE=false
# Wed, 06 Nov 2024 14:56:24 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl241120241021-1102 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=24.0.0.12-beta
# Wed, 06 Nov 2024 14:56:24 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12-beta LIBERTY_SHA=f390f288633eef7667b16301f3928462d5d39e57 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.12-beta/openliberty-runtime-24.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl241120241021-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12-beta LIBERTY_SHA=f390f288633eef7667b16301f3928462d5d39e57 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.12-beta/openliberty-runtime-24.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl241120241021-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 06 Nov 2024 14:56:24 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12-beta LIBERTY_SHA=f390f288633eef7667b16301f3928462d5d39e57 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.12-beta/openliberty-runtime-24.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl241120241021-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12-beta LIBERTY_SHA=f390f288633eef7667b16301f3928462d5d39e57 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.12-beta/openliberty-runtime-24.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl241120241021-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
# ARGS: LIBERTY_VERSION=24.0.0.12-beta LIBERTY_SHA=f390f288633eef7667b16301f3928462d5d39e57 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/24.0.0.12-beta/openliberty-runtime-24.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl241120241021-1102 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 06 Nov 2024 14:56:24 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 06 Nov 2024 14:56:24 GMT
USER 1001
# Wed, 06 Nov 2024 14:56:24 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 06 Nov 2024 14:56:24 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 06 Nov 2024 14:56:24 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d7fcbb74a18dbda1a95a881c01c2cc4d8a0d6fe38b3b4f8b5899f281f9815e`  
		Last Modified: Tue, 17 Sep 2024 01:57:02 GMT  
		Size: 12.2 MB (12203759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9808fafa51f0663378c6856bb2c3d3c29c8c1fdede39638c3b1fadddc2e64640`  
		Last Modified: Mon, 18 Nov 2024 19:34:37 GMT  
		Size: 50.3 MB (50340178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fdf4880bec1a2292221bde2ce59a88884df10168cbcb9a58d596062bc06d63`  
		Last Modified: Mon, 18 Nov 2024 19:34:36 GMT  
		Size: 4.3 MB (4337626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bcf265e90263b350665c5aa0691079b25327c5cea4378ef0631b4680625452`  
		Last Modified: Mon, 18 Nov 2024 21:45:49 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ef73241d165a186d69890eed49cc937a7768898e00d6fa2753e87b14c509e0`  
		Last Modified: Mon, 18 Nov 2024 21:45:49 GMT  
		Size: 10.0 KB (9981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6777049e2388846dcc6b43b4c381d18252be59063e123fff1b4e9387a062eceb`  
		Last Modified: Mon, 18 Nov 2024 21:45:49 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83688aa3918e2ff6b7dfad9b4d15ef00cb32495fb5ccbe471e3aee3ee21af2b`  
		Last Modified: Mon, 18 Nov 2024 21:45:49 GMT  
		Size: 33.1 KB (33113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fed37d6496c30ca033f8a915d341dbee5971022010d988486e574ae07c4d12`  
		Last Modified: Mon, 18 Nov 2024 21:45:56 GMT  
		Size: 359.6 MB (359551199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712003ef170affa6f7332915a01adc24801bb561e89d51a0ad81107f538ff2a0`  
		Last Modified: Mon, 18 Nov 2024 21:45:50 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f446d8f8d2b14f0cf25b677b5065e45aa26d313c6a52bace3d8f5d4715d1da`  
		Last Modified: Mon, 18 Nov 2024 21:45:50 GMT  
		Size: 11.3 KB (11339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaeb7e360561af0ec7286d8609858a918159150db8a57d7ccece893b82db9056`  
		Last Modified: Mon, 18 Nov 2024 21:45:51 GMT  
		Size: 13.3 MB (13338560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta` - unknown; unknown

```console
$ docker pull open-liberty@sha256:6f9d1f91640ff0437a6862fe733a0ce99b86e653ffe072c5e3db3802fd5fdfdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5759752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae87d985fd987bcc59aaf26e5bb829656a11b69d88b4b0411922797f65375ef`

```dockerfile
```

-	Layers:
	-	`sha256:7f50a703071d9608dd5c2ff448ebec226410bfb3454fac4f6e4236900eb43ac2`  
		Last Modified: Mon, 18 Nov 2024 21:45:49 GMT  
		Size: 5.7 MB (5721066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ee45eabe789bf34ea1bb00ec6bea6543daf4e408b33564f8796ed0e803319f8`  
		Last Modified: Mon, 18 Nov 2024 21:45:49 GMT  
		Size: 38.7 KB (38686 bytes)  
		MIME: application/vnd.in-toto+json
