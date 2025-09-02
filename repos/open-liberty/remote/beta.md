## `open-liberty:beta`

```console
$ docker pull open-liberty@sha256:5dcc53756d6491afa13d4ac9b3f729def1ad2cddce0816e59af0dca3e04d632a
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
$ docker pull open-liberty@sha256:0cd4e8d68daf2564dd7cc0d32fd9be406669528abdc027304c1e9ff17fd5de83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.3 MB (480283920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d1cc9db7bf36cc309fb652ae70d06d866647da28c0c353382705a87269572ec`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 12 Aug 2025 13:28:10 GMT
ARG RELEASE
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 13:28:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 13:28:10 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Aug 2025 13:28:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 12 Aug 2025 13:28:10 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 13:28:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 Aug 2025 13:28:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
ENV JAVA_VERSION=jdk8u462-b08_openj9-0.53.0
# Tue, 12 Aug 2025 13:28:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='6ecee3b35e62c11651f6725b7d7b5eabc662166008db7b8f7b49887692a17628';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u462-b08_openj9-0.53.0/ibm-semeru-open-jre_aarch64_linux_8u462b08_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='1b072a86966d7ac9cb425849d361d6e6f1a65b64a756c982e305a3e44c45a237';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u462-b08_openj9-0.53.0/ibm-semeru-open-jre_ppc64le_linux_8u462b08_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='1e61dc30dffea82f5dec85cb18e3d8b29ffd211ee2bc2b12a5d1e9a4725ab4f9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u462-b08_openj9-0.53.0/ibm-semeru-open-jre_x64_linux_8u462b08_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='07b7aac38f2f6ea575fed24a4016a0463ffd0d3ac44de0d30801b6b37566f2a2';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u462-b08_openj9-0.53.0/ibm-semeru-open-jre_s390x_linux_8u462b08_openj9-0.53.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 13:28:10 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 12 Aug 2025 13:28:10 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="243474cd54d8589c97f2db964b13b36920500a298b190370a8c58306db786bb30101c33d9ca85eddd8014c5d7f53fec1685beeb4fb7f3037ffcc2f4124c6c6b7";     TOMCAT_VERSION="9.0.108";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
USER root
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LIBERTY_VERSION=25.0.0.9-beta
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LIBERTY_BUILD_LABEL=cl250820250727-1902
# Tue, 12 Aug 2025 13:28:10 GMT
ARG OPENJ9_SCC=true
# Tue, 12 Aug 2025 13:28:10 GMT
ARG VERBOSE=false
# Tue, 12 Aug 2025 13:28:10 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250820250727-1902 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=25.0.0.9-beta liberty.version=25.0.0.9-beta io.openliberty.version=25.0.0.9-beta
# Tue, 12 Aug 2025 13:28:10 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 12 Aug 2025 13:28:10 GMT
USER 1001
# Tue, 12 Aug 2025 13:28:10 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 12 Aug 2025 13:28:10 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 12 Aug 2025 13:28:10 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcde3d13d0251c716f205c8ae2841824ae4aaf4afbc2973d7221d3fef426680`  
		Last Modified: Mon, 01 Sep 2025 23:10:04 GMT  
		Size: 12.2 MB (12171801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878c612682dfb1752e753682ca0840b6af2683c4cddec5856424205942112d01`  
		Last Modified: Mon, 01 Sep 2025 23:10:04 GMT  
		Size: 53.7 MB (53676075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd6a8015a336653ec266dc0845072b544be6e26e397a44e136e8f7e5bd7595d`  
		Last Modified: Mon, 01 Sep 2025 23:10:06 GMT  
		Size: 4.3 MB (4278640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3c24316db9a720c0ddb905a269c4d7853d679f193c0414326ca51b7f9a8905`  
		Last Modified: Tue, 02 Sep 2025 01:50:44 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422950eee15e026f0aad8cda43704a52a8609b3e8cd83dd847aa3bbc8f88935b`  
		Last Modified: Tue, 02 Sep 2025 01:50:44 GMT  
		Size: 12.5 KB (12462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74fa9a668e98d376ab2c731124dfb7cf81ea5d0b9d27e88190c533811c49c4fe`  
		Last Modified: Tue, 02 Sep 2025 01:50:45 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a1ce23057125c8434256f8454a26f51de115d42b19edee426c020e04b9b45d`  
		Last Modified: Tue, 02 Sep 2025 01:50:45 GMT  
		Size: 31.7 KB (31745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ca08af11d223aa12807c363dca006110f6b942c43d25c55a2f617f1e778867`  
		Last Modified: Tue, 02 Sep 2025 07:59:48 GMT  
		Size: 366.8 MB (366804254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e83f5c70cd37f3f3235a3eb7113adde88bcaf3deee38125470673fd324234a33`  
		Last Modified: Tue, 02 Sep 2025 01:50:45 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a85ffb643de57b386f3f9389ea24b435d647a6799158dd1c6d8187abb2377c7`  
		Last Modified: Tue, 02 Sep 2025 01:50:46 GMT  
		Size: 13.9 KB (13860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb7f57fe0a6057a563c3da940a3d5b84663538cd001611258b492ce1c964440`  
		Last Modified: Tue, 02 Sep 2025 01:50:47 GMT  
		Size: 13.8 MB (13755803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta` - unknown; unknown

```console
$ docker pull open-liberty@sha256:628e30f666c1b4963a84ecf88f1369f26f31b4523bcbd4e8db877a02eb3b1d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5846359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427db26f4c0ec0f2a38b7029dc6a4b633d9bcb6a52d58e4f9e6c0b91d1b2cf35`

```dockerfile
```

-	Layers:
	-	`sha256:17e95d2cecdbbf41fe1ce6f6fc6bf072058bc048b39048f3ac54b5af24e8de01`  
		Last Modified: Tue, 02 Sep 2025 02:48:02 GMT  
		Size: 5.8 MB (5807445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd3828b321c4167ad857621a70c562cb9630228665244eaceca8a03f2c7fed49`  
		Last Modified: Tue, 02 Sep 2025 02:48:04 GMT  
		Size: 38.9 KB (38914 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:823187bfc4323a7c2be52752b0cdafdbb81fedcf33dbe0c115405103b4d5d549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **476.9 MB (476909216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31cb9ce64830a7a027c2be36a53fdd1c90c72dd82b829f6549d31199d36a879`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 12 Aug 2025 13:28:10 GMT
ARG RELEASE
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 13:28:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 13:28:10 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Aug 2025 13:28:10 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 12 Aug 2025 13:28:10 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 13:28:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 Aug 2025 13:28:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
ENV JAVA_VERSION=jdk8u462-b08_openj9-0.53.0
# Tue, 12 Aug 2025 13:28:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='6ecee3b35e62c11651f6725b7d7b5eabc662166008db7b8f7b49887692a17628';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u462-b08_openj9-0.53.0/ibm-semeru-open-jre_aarch64_linux_8u462b08_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='1b072a86966d7ac9cb425849d361d6e6f1a65b64a756c982e305a3e44c45a237';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u462-b08_openj9-0.53.0/ibm-semeru-open-jre_ppc64le_linux_8u462b08_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='1e61dc30dffea82f5dec85cb18e3d8b29ffd211ee2bc2b12a5d1e9a4725ab4f9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u462-b08_openj9-0.53.0/ibm-semeru-open-jre_x64_linux_8u462b08_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='07b7aac38f2f6ea575fed24a4016a0463ffd0d3ac44de0d30801b6b37566f2a2';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u462-b08_openj9-0.53.0/ibm-semeru-open-jre_s390x_linux_8u462b08_openj9-0.53.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 13:28:10 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 12 Aug 2025 13:28:10 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="243474cd54d8589c97f2db964b13b36920500a298b190370a8c58306db786bb30101c33d9ca85eddd8014c5d7f53fec1685beeb4fb7f3037ffcc2f4124c6c6b7";     TOMCAT_VERSION="9.0.108";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
USER root
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LIBERTY_VERSION=25.0.0.9-beta
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LIBERTY_BUILD_LABEL=cl250820250727-1902
# Tue, 12 Aug 2025 13:28:10 GMT
ARG OPENJ9_SCC=true
# Tue, 12 Aug 2025 13:28:10 GMT
ARG VERBOSE=false
# Tue, 12 Aug 2025 13:28:10 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250820250727-1902 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=25.0.0.9-beta liberty.version=25.0.0.9-beta io.openliberty.version=25.0.0.9-beta
# Tue, 12 Aug 2025 13:28:10 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 12 Aug 2025 13:28:10 GMT
USER 1001
# Tue, 12 Aug 2025 13:28:10 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 12 Aug 2025 13:28:10 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 12 Aug 2025 13:28:10 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ae624de3eeb0edb3e4a120905423464cf816ca0d11b0b199c055f29c2e6609`  
		Last Modified: Tue, 02 Sep 2025 01:29:48 GMT  
		Size: 12.1 MB (12130364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a0f664f250caab10003bd767dbfe9c11f1d233a6930101423a49eb69c92fd1`  
		Last Modified: Tue, 02 Sep 2025 01:31:57 GMT  
		Size: 53.4 MB (53394952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881e7e0dbc26810951c2565f5b198db2d9d39d3d332d3e244aa460c1d76782b1`  
		Last Modified: Tue, 02 Sep 2025 01:31:47 GMT  
		Size: 4.1 MB (4055782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2f0acbe69cfe6aaebdbaefb44e351a093846c4f5ab718b6aa45d6e40f0b306`  
		Last Modified: Tue, 02 Sep 2025 05:08:12 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b12e9c1f288ef7a96203cceb4bb93886c760edf1088cc0686aae4027ff99a7`  
		Last Modified: Tue, 02 Sep 2025 05:08:12 GMT  
		Size: 12.5 KB (12460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc52ad73b9d5bbc868f298bddb70124ebb491bb8f449f730a66e69c863434835`  
		Last Modified: Tue, 02 Sep 2025 05:08:12 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041a1cde949acac29340b1f4a6ce85ee0dd07eb165d99a0146d3359fbfaf5351`  
		Last Modified: Tue, 02 Sep 2025 05:08:12 GMT  
		Size: 42.3 KB (42322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b226be508eebe907c1d30282e2a499a7818c685869b7b361596cffc3adcc4383`  
		Last Modified: Tue, 02 Sep 2025 05:08:07 GMT  
		Size: 366.8 MB (366804484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55e3aaf158410b0f098a3f2500647ab3394693538e1be004c30e786d6f51bf8`  
		Last Modified: Tue, 02 Sep 2025 05:08:12 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f1bbea61bda258acede8c6fa6e8295f086e985dc82532f9a39647c3fdf3de0`  
		Last Modified: Tue, 02 Sep 2025 05:08:12 GMT  
		Size: 13.9 KB (13864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c475c10e41a22f7c058b8e1a88c0cee882a116f93cd5483e9e43d8d0da124c`  
		Last Modified: Tue, 02 Sep 2025 05:08:13 GMT  
		Size: 13.1 MB (13091177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta` - unknown; unknown

```console
$ docker pull open-liberty@sha256:070a9ae9ece21dda612f4b214d2c589cca4f78094160bd5d1c993a4ec2229e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5846282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc2ad9caa38e4b605c905aaedcb42a4be11a10381884f112d0cdd9dd1736bd6`

```dockerfile
```

-	Layers:
	-	`sha256:2e46e72629e6364c1b9e5f3aeaacaf0e3d280b539b72ad9dff53002bc5b705f5`  
		Last Modified: Tue, 02 Sep 2025 08:48:10 GMT  
		Size: 5.8 MB (5807241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d966c02019f2126c60932ff208cc3b66871f6affc8952747a543495764d4ffc`  
		Last Modified: Tue, 02 Sep 2025 08:48:10 GMT  
		Size: 39.0 KB (39041 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:2bfbd59f07ef275d6cb7b9eb0279c4f52e7da82d9594406775792ba347d8ac15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.9 MB (484872541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b27f78e9fe45a5ed0724052d697b940499c6f362844a30b9d43fecc476b7df1`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 12 Aug 2025 13:28:10 GMT
ARG RELEASE
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 13:28:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 13:28:10 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Aug 2025 13:28:10 GMT
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Tue, 12 Aug 2025 13:28:10 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 13:28:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 Aug 2025 13:28:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
ENV JAVA_VERSION=jdk8u462-b08_openj9-0.53.0
# Tue, 12 Aug 2025 13:28:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='6ecee3b35e62c11651f6725b7d7b5eabc662166008db7b8f7b49887692a17628';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u462-b08_openj9-0.53.0/ibm-semeru-open-jre_aarch64_linux_8u462b08_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='1b072a86966d7ac9cb425849d361d6e6f1a65b64a756c982e305a3e44c45a237';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u462-b08_openj9-0.53.0/ibm-semeru-open-jre_ppc64le_linux_8u462b08_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='1e61dc30dffea82f5dec85cb18e3d8b29ffd211ee2bc2b12a5d1e9a4725ab4f9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u462-b08_openj9-0.53.0/ibm-semeru-open-jre_x64_linux_8u462b08_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='07b7aac38f2f6ea575fed24a4016a0463ffd0d3ac44de0d30801b6b37566f2a2';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u462-b08_openj9-0.53.0/ibm-semeru-open-jre_s390x_linux_8u462b08_openj9-0.53.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 13:28:10 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 12 Aug 2025 13:28:10 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="243474cd54d8589c97f2db964b13b36920500a298b190370a8c58306db786bb30101c33d9ca85eddd8014c5d7f53fec1685beeb4fb7f3037ffcc2f4124c6c6b7";     TOMCAT_VERSION="9.0.108";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
USER root
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LIBERTY_VERSION=25.0.0.9-beta
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LIBERTY_BUILD_LABEL=cl250820250727-1902
# Tue, 12 Aug 2025 13:28:10 GMT
ARG OPENJ9_SCC=true
# Tue, 12 Aug 2025 13:28:10 GMT
ARG VERBOSE=false
# Tue, 12 Aug 2025 13:28:10 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250820250727-1902 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=25.0.0.9-beta liberty.version=25.0.0.9-beta io.openliberty.version=25.0.0.9-beta
# Tue, 12 Aug 2025 13:28:10 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 12 Aug 2025 13:28:10 GMT
USER 1001
# Tue, 12 Aug 2025 13:28:10 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 12 Aug 2025 13:28:10 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 12 Aug 2025 13:28:10 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd05e0384f89e87f39bbca5882dc09e12e30daf4c6b9267897a05fc765378ae`  
		Last Modified: Tue, 02 Sep 2025 00:35:06 GMT  
		Size: 12.9 MB (12894660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d3f51a2103e1fa3f1290fe8d90c7b419a5e3f2bb382dcbeda194a4bce377f2`  
		Last Modified: Tue, 02 Sep 2025 00:38:11 GMT  
		Size: 55.3 MB (55256430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba19e3b96406229dc55d0cb10b5d6eb4697af3fd909d37bddb86115642145ef9`  
		Last Modified: Tue, 02 Sep 2025 00:38:11 GMT  
		Size: 3.5 MB (3530155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c075e6855b57de86620f500678ae746e2a54e7f07ee5fc896ca3ef96a77e7e7e`  
		Last Modified: Tue, 02 Sep 2025 05:58:12 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c55b88ba1dc411c50bac9439ade88f789e52bcfa6432d72a9a3061791f64afe`  
		Last Modified: Tue, 02 Sep 2025 05:58:12 GMT  
		Size: 12.5 KB (12458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc873b5d33cd6c8eacb121fadb5b5353e2ff26205f4a6ca28d57206f52b63b0d`  
		Last Modified: Tue, 02 Sep 2025 05:58:12 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452fc8092f4bf11de76546e01365b8c766d063cece65419b5239166cf7bd75c8`  
		Last Modified: Tue, 02 Sep 2025 05:58:12 GMT  
		Size: 36.5 KB (36495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2958230161b607b6b645cc33373c6ca5cc7930bdf717748af1c97d3fe767c3`  
		Last Modified: Tue, 02 Sep 2025 05:58:01 GMT  
		Size: 366.8 MB (366804594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd0f5c44bf97d1f0c57c7c8cc92cb6dc6cb7060b1accfdc6ab178da4dd77e87`  
		Last Modified: Tue, 02 Sep 2025 05:58:12 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cad44de53465da9aad86dd20f7f2846c29db17b884e22bdcde5f78b92c4aec`  
		Last Modified: Tue, 02 Sep 2025 05:58:12 GMT  
		Size: 13.9 KB (13861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250119a45ca055bbf012a29ca6d69c12b0d0caf45618b1a5e70a229ed64b43e7`  
		Last Modified: Tue, 02 Sep 2025 05:58:13 GMT  
		Size: 11.9 MB (11878323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta` - unknown; unknown

```console
$ docker pull open-liberty@sha256:bcbcf00e0fcae38ae0865337a0836c25c295a6d4edf51abe45858e3ce06ed788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5851183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c873dff198bfaa512046049d7a63bd72206259e2b8f1e15014a380d5127bbc4`

```dockerfile
```

-	Layers:
	-	`sha256:975548ca8bcdae4738c8a84e6e83d4b4c6d4704b73c616d95113ef806331fbf1`  
		Last Modified: Tue, 02 Sep 2025 08:48:15 GMT  
		Size: 5.8 MB (5812236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c7cecd59235fb83da2b79499e17c715a71db183bc75b38f8d4fb38c6c853138`  
		Last Modified: Tue, 02 Sep 2025 08:48:16 GMT  
		Size: 38.9 KB (38947 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta` - linux; s390x

```console
$ docker pull open-liberty@sha256:885813490176fff8242bb86e19235484f5b55939654b558e1daba88a533fd19c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.3 MB (478274663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d53360947fa8e711550639ff87175933de0959e094b991a6e2715f417b1b978`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 12 Aug 2025 13:28:10 GMT
ARG RELEASE
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 13:28:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 13:28:10 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Aug 2025 13:28:10 GMT
ADD file:29917512cc6cafe60268e67a6ab4ee1e581cd8f4c2bca9a228ba5a680375b746 in / 
# Tue, 12 Aug 2025 13:28:10 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 13:28:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 Aug 2025 13:28:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
ENV JAVA_VERSION=jdk8u462-b08_openj9-0.53.0
# Tue, 12 Aug 2025 13:28:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='6ecee3b35e62c11651f6725b7d7b5eabc662166008db7b8f7b49887692a17628';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u462-b08_openj9-0.53.0/ibm-semeru-open-jre_aarch64_linux_8u462b08_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='1b072a86966d7ac9cb425849d361d6e6f1a65b64a756c982e305a3e44c45a237';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u462-b08_openj9-0.53.0/ibm-semeru-open-jre_ppc64le_linux_8u462b08_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='1e61dc30dffea82f5dec85cb18e3d8b29ffd211ee2bc2b12a5d1e9a4725ab4f9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u462-b08_openj9-0.53.0/ibm-semeru-open-jre_x64_linux_8u462b08_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='07b7aac38f2f6ea575fed24a4016a0463ffd0d3ac44de0d30801b6b37566f2a2';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u462-b08_openj9-0.53.0/ibm-semeru-open-jre_s390x_linux_8u462b08_openj9-0.53.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 13:28:10 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 12 Aug 2025 13:28:10 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="243474cd54d8589c97f2db964b13b36920500a298b190370a8c58306db786bb30101c33d9ca85eddd8014c5d7f53fec1685beeb4fb7f3037ffcc2f4124c6c6b7";     TOMCAT_VERSION="9.0.108";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
USER root
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LIBERTY_VERSION=25.0.0.9-beta
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LIBERTY_BUILD_LABEL=cl250820250727-1902
# Tue, 12 Aug 2025 13:28:10 GMT
ARG OPENJ9_SCC=true
# Tue, 12 Aug 2025 13:28:10 GMT
ARG VERBOSE=false
# Tue, 12 Aug 2025 13:28:10 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250820250727-1902 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=25.0.0.9-beta liberty.version=25.0.0.9-beta io.openliberty.version=25.0.0.9-beta
# Tue, 12 Aug 2025 13:28:10 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 12 Aug 2025 13:28:10 GMT
USER 1001
# Tue, 12 Aug 2025 13:28:10 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 12 Aug 2025 13:28:10 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 12 Aug 2025 13:28:10 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:2109104756ac117958527cffddc193d2cf33d0621953649a7d5800a93fa86665`  
		Last Modified: Mon, 01 Sep 2025 22:59:18 GMT  
		Size: 28.0 MB (28003668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69dd744c6ce11f9bcc42b570d4944d0ecf9b125f3d1c222308ced56deb59072`  
		Last Modified: Mon, 01 Sep 2025 23:24:49 GMT  
		Size: 12.2 MB (12219976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a95d2bf7f14aefe49f054f313cf2a1d0c76986163c298610b7a653a72e4e7dc`  
		Last Modified: Mon, 01 Sep 2025 23:27:56 GMT  
		Size: 53.3 MB (53267347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e875520e7e4c24908741fc84f0eba616037e81b6199d0a0e0a3fe689da072826`  
		Last Modified: Mon, 01 Sep 2025 23:27:55 GMT  
		Size: 4.4 MB (4396689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c39fb393de5b4e9fe8a91db4125053934ae904927a17355cd5de1767894c698`  
		Last Modified: Tue, 02 Sep 2025 00:40:04 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216ec142b05f5fb0bce58699fd27293712224e748a1d698fbdcdb3ec07a692de`  
		Last Modified: Tue, 02 Sep 2025 00:40:05 GMT  
		Size: 12.5 KB (12458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c769aeeacd1e1badcf7a952a3548bf37fcdfe2f85b53e937d572fff108735a0c`  
		Last Modified: Tue, 02 Sep 2025 00:40:05 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a63316579be86c9b85a4a38c0d03dee3a726d3f1835a8f2c8c53b2b9c24417c`  
		Last Modified: Tue, 02 Sep 2025 00:40:05 GMT  
		Size: 33.1 KB (33110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd183c1b94193124f91e1a71af0c2feeb542f4cbe6d6abaa5702eac0540bd91c`  
		Last Modified: Tue, 02 Sep 2025 00:39:58 GMT  
		Size: 366.8 MB (366803988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da817788dc35a914645d43e154b5572e9d5041adf0fe1070441d7e1a7361388`  
		Last Modified: Tue, 02 Sep 2025 00:40:05 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc3f7f68dff8da85972c43d57d7411e634b289595584d2612217c7299a35da4`  
		Last Modified: Tue, 02 Sep 2025 00:40:05 GMT  
		Size: 13.9 KB (13859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d43d5facebe9ec7765351a363d2495493b9274384f1cf989500340b14ca490`  
		Last Modified: Tue, 02 Sep 2025 00:40:14 GMT  
		Size: 13.5 MB (13521224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta` - unknown; unknown

```console
$ docker pull open-liberty@sha256:6cb50d5702fe89d10e46d3821c274809a3f64b115ec537a189922d9b75199d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5847376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a0919214dfe4821520e0f79ea1b412d802ca53cb2e9b1085c3f041e4fe00a7`

```dockerfile
```

-	Layers:
	-	`sha256:04d4ec360062b888203c446efb0ed1e06726b055a5482ad081a148cffc0bbe59`  
		Last Modified: Tue, 02 Sep 2025 02:48:17 GMT  
		Size: 5.8 MB (5808462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:892c2316e42065bb1943bfc296321865bb195589fd7fb1e5206322c6df55439b`  
		Last Modified: Tue, 02 Sep 2025 02:48:18 GMT  
		Size: 38.9 KB (38914 bytes)  
		MIME: application/vnd.in-toto+json
