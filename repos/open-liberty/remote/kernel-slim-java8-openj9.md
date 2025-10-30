## `open-liberty:kernel-slim-java8-openj9`

```console
$ docker pull open-liberty@sha256:59ae50df5afeb407ff99f0cf0be8dc81fb6d3916be126d58dd96a98ec663113f
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
$ docker pull open-liberty@sha256:cf001f2ec400a0244a70c207d651d68d61c0194426f8b61c97fe84bd124ce9ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.4 MB (117402351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:decee7a82af2d33aaafcb42903569a3885722dc7d7938d3afcb1aef5c776932b`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 18:52:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Oct 2025 18:52:18 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 18:52:18 GMT
ENV JAVA_VERSION=jdk8u472-b08_openj9-0.56.0
# Thu, 30 Oct 2025 18:54:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='e9f04c51ace0cc724a7b3e54e58ad1823d899c77c2a141ab28efb226c3c7bb97';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='995b091e78fe2e0fb201e3c06272d9bef018594e3205c0a981152bc3f537eda9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='5babd67d884af6251b504932e2cdce2e5a969075efa856c91087ecc6f3933fc6';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='0225084f7067a8ccf5131b7656ea5ac62d6a68fbab71dc52aac24ab02299ee7a';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Oct 2025 18:54:38 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Oct 2025 18:54:38 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Oct 2025 18:55:09 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba";     TOMCAT_VERSION="9.0.111";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 30 Oct 2025 19:13:57 GMT
USER root
# Thu, 30 Oct 2025 19:13:57 GMT
ARG LIBERTY_VERSION=25.0.0.10
# Thu, 30 Oct 2025 19:13:57 GMT
ARG LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca
# Thu, 30 Oct 2025 19:13:57 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip
# Thu, 30 Oct 2025 19:13:57 GMT
ARG LIBERTY_BUILD_LABEL=cl251020250923-1355
# Thu, 30 Oct 2025 19:13:57 GMT
ARG OPENJ9_SCC=true
# Thu, 30 Oct 2025 19:13:57 GMT
ARG VERBOSE=false
# Thu, 30 Oct 2025 19:13:57 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251020250923-1355 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.10 liberty.version=25.0.0.10 io.openliberty.version=25.0.0.10
# Thu, 30 Oct 2025 19:13:57 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Thu, 30 Oct 2025 19:13:57 GMT
COPY helpers /opt/ol/helpers # buildkit
# Thu, 30 Oct 2025 19:13:57 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Thu, 30 Oct 2025 19:13:58 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Thu, 30 Oct 2025 19:14:07 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Thu, 30 Oct 2025 19:14:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 30 Oct 2025 19:14:07 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 30 Oct 2025 19:14:07 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Thu, 30 Oct 2025 19:14:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Thu, 30 Oct 2025 19:14:10 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 30 Oct 2025 19:14:10 GMT
USER 1001
# Thu, 30 Oct 2025 19:14:10 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 30 Oct 2025 19:14:10 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 30 Oct 2025 19:14:10 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3efb4b5e4362ba249177f6f625153b69aa996b818762278e6c384fce2d0e2253`  
		Last Modified: Thu, 30 Oct 2025 18:54:39 GMT  
		Size: 12.2 MB (12171639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61fd7f63b089e1e44b0c40c9e70eb32899fc23b291118ace01aa2169f4e653b9`  
		Last Modified: Thu, 30 Oct 2025 18:55:34 GMT  
		Size: 53.7 MB (53730424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9843490e6ee3415885f2ff5be8d8783e2a39edf1fd121929e3ef9c8d3e6d4552`  
		Last Modified: Thu, 30 Oct 2025 18:55:27 GMT  
		Size: 4.3 MB (4291453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39cde7df6869cf372cb65ba80b2ef5cc7d2983f4bef27fe0ffe76a078058342`  
		Last Modified: Thu, 30 Oct 2025 19:14:26 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44001e362d90e0697f6c1c41d1530c45705275df70435c4855ac8c97cf8660df`  
		Last Modified: Thu, 30 Oct 2025 19:14:26 GMT  
		Size: 12.1 KB (12104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc097948d5751a3ca89ac2c3cfdcf7de3999e00dcf6ae1ca469b76e6c0b0ab8`  
		Last Modified: Thu, 30 Oct 2025 19:14:26 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acae2c023521283a2b4e0a81dcbadd0922d393786df9f4ade5f0ce7e3264b8b`  
		Last Modified: Thu, 30 Oct 2025 19:14:26 GMT  
		Size: 31.7 KB (31746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbc26105d9cca9aba835ab63a923b4e0f7b20a7707f0752a1a1a38ce0b33ad9`  
		Last Modified: Thu, 30 Oct 2025 19:14:28 GMT  
		Size: 14.9 MB (14868289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2440c3faa361ef854f6e15f2387823c3d95b40fabed676916b8b330cb738f8d4`  
		Last Modified: Thu, 30 Oct 2025 19:14:26 GMT  
		Size: 736.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e0b97661bdd5cac8a598df503bd48423c41133164220e907e3383c7e6b6df9`  
		Last Modified: Thu, 30 Oct 2025 19:14:26 GMT  
		Size: 13.2 KB (13199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0622620892a0603042400907ff771841076585ce619174a9898703dc89b13ca`  
		Last Modified: Thu, 30 Oct 2025 19:14:28 GMT  
		Size: 2.7 MB (2744651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:kernel-slim-java8-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:37d50fc3291d64ddd9de6d5ed9ea34e721b34899575c18e21e3b77b88b3c011b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3935747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616d7cdcd6eee7acb18cd6239e3c78a3996a38c641c58eacf0d6a9aaebcd14d6`

```dockerfile
```

-	Layers:
	-	`sha256:804b855c3756c5963ac3162dc43bf4590752d579911966e50193f190aa9a82b2`  
		Last Modified: Thu, 30 Oct 2025 20:46:38 GMT  
		Size: 3.9 MB (3895949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04cdb9559713da1e6839df419ed8155ae99aa2294bc628bf08629df59ed97d6c`  
		Last Modified: Thu, 30 Oct 2025 20:46:39 GMT  
		Size: 39.8 KB (39798 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:kernel-slim-java8-openj9` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:3e43fa51c13cae2f0037a927fb57d57bfad433ca42e79b9100484c067193cec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114771463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9627f5c3eed1b00fa34fd97dc1b3035cbe12da06e317a38e252cd2b22e16aca3`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 18:55:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Oct 2025 18:55:15 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 18:55:15 GMT
ENV JAVA_VERSION=jdk8u472-b08_openj9-0.56.0
# Thu, 30 Oct 2025 18:55:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='e9f04c51ace0cc724a7b3e54e58ad1823d899c77c2a141ab28efb226c3c7bb97';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='995b091e78fe2e0fb201e3c06272d9bef018594e3205c0a981152bc3f537eda9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='5babd67d884af6251b504932e2cdce2e5a969075efa856c91087ecc6f3933fc6';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='0225084f7067a8ccf5131b7656ea5ac62d6a68fbab71dc52aac24ab02299ee7a';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Oct 2025 18:55:18 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Oct 2025 18:55:18 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Oct 2025 18:55:50 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba";     TOMCAT_VERSION="9.0.111";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 30 Oct 2025 19:52:33 GMT
USER root
# Thu, 30 Oct 2025 19:52:33 GMT
ARG LIBERTY_VERSION=25.0.0.10
# Thu, 30 Oct 2025 19:52:33 GMT
ARG LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca
# Thu, 30 Oct 2025 19:52:33 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip
# Thu, 30 Oct 2025 19:52:33 GMT
ARG LIBERTY_BUILD_LABEL=cl251020250923-1355
# Thu, 30 Oct 2025 19:52:33 GMT
ARG OPENJ9_SCC=true
# Thu, 30 Oct 2025 19:52:33 GMT
ARG VERBOSE=false
# Thu, 30 Oct 2025 19:52:33 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251020250923-1355 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.10 liberty.version=25.0.0.10 io.openliberty.version=25.0.0.10
# Thu, 30 Oct 2025 19:52:33 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Thu, 30 Oct 2025 19:52:33 GMT
COPY helpers /opt/ol/helpers # buildkit
# Thu, 30 Oct 2025 19:52:33 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Thu, 30 Oct 2025 19:52:33 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Thu, 30 Oct 2025 19:52:44 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Thu, 30 Oct 2025 19:52:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 30 Oct 2025 19:52:44 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 30 Oct 2025 19:52:44 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Thu, 30 Oct 2025 19:52:48 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Thu, 30 Oct 2025 19:52:48 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 30 Oct 2025 19:52:48 GMT
USER 1001
# Thu, 30 Oct 2025 19:52:48 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 30 Oct 2025 19:52:48 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 30 Oct 2025 19:52:48 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d84a105da568624481b778ba63905583b4078a03a265ce2ad5df612f92d4e7`  
		Last Modified: Thu, 30 Oct 2025 18:56:10 GMT  
		Size: 12.1 MB (12129905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a5f6cd034c16728c96a933f3c7f8697c0c2bea467fb3be8a09e7e5f73b7939`  
		Last Modified: Thu, 30 Oct 2025 18:56:15 GMT  
		Size: 53.4 MB (53440936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad81da9893b9614194e5d2acd04d63bd30f02a01db3fe8a85bb27fa4bda0163`  
		Last Modified: Thu, 30 Oct 2025 18:56:09 GMT  
		Size: 4.1 MB (4141364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b6020afc9641f62216d133cd4e2aceef4dde8e283de608058ab4a3d71b9c5f`  
		Last Modified: Thu, 30 Oct 2025 19:53:20 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae17ad6bd282633849bbcb71d0ab0c554ea860d3f4710f0ad0b21546a68cb788`  
		Last Modified: Thu, 30 Oct 2025 19:53:21 GMT  
		Size: 12.1 KB (12106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f728cf131f4437436d5a13a0581d089629b5780588ec4d48010c80bd33f94140`  
		Last Modified: Thu, 30 Oct 2025 19:53:20 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb5dd1f0a88cb383ed10582c0e474173c7e266b0805ae2a0745b46d252ee0ba`  
		Last Modified: Thu, 30 Oct 2025 19:53:20 GMT  
		Size: 42.3 KB (42327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1771a36f21f970394b7a9eb2152bdc1f9a8fea5bcdf3ea4c41fe868361d31e70`  
		Last Modified: Thu, 30 Oct 2025 19:53:21 GMT  
		Size: 14.9 MB (14868572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc845189daa8040070bdc7267164c182b095d27dea724c7855bed0ee30f853b3`  
		Last Modified: Thu, 30 Oct 2025 19:53:21 GMT  
		Size: 738.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893b532938d8f3ac43ee1dd25d864deff3170822fcbfdc4d52eed0739a4cc4d2`  
		Last Modified: Thu, 30 Oct 2025 19:53:21 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74628a4f8eb44b64de678aaaaae520b05b56e33048d91353b3cfcc711d40d8b2`  
		Last Modified: Thu, 30 Oct 2025 19:53:21 GMT  
		Size: 2.7 MB (2737907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:kernel-slim-java8-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:a6a1c92df9558661ed2e4905e71f7c407dfaf3c1a65af4292edf492b8eddd143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3935719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2116989bb19ec0acc1b36df9cd5e68982ca58f6384987f2e692e66b73e4b305c`

```dockerfile
```

-	Layers:
	-	`sha256:fcaa520328f6a0c45a7f0a2b85d9745ac810a2acb0e6b10d84baae8ec1c05552`  
		Last Modified: Thu, 30 Oct 2025 20:46:44 GMT  
		Size: 3.9 MB (3895769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30b48a0f9b21b0637442b384d1ec47fbeb3926a4ca21a960d0ed58ed94650fc7`  
		Last Modified: Thu, 30 Oct 2025 20:46:45 GMT  
		Size: 40.0 KB (39950 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:kernel-slim-java8-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:9e4e7cd72bf685702a7f0c8d75bc3ea49e7e8edaa696106c1e12a085d599a16c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123750450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a12f3f75ec1f6e7d7b46509604cae3ea4f553d6ae9fd424b8cc8d449fe074f6`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 01 Oct 2025 07:06:37 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:06:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:06:42 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Wed, 01 Oct 2025 07:06:43 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 18:52:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Oct 2025 18:52:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 18:52:43 GMT
ENV JAVA_VERSION=jdk8u472-b08_openj9-0.56.0
# Thu, 30 Oct 2025 18:55:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='e9f04c51ace0cc724a7b3e54e58ad1823d899c77c2a141ab28efb226c3c7bb97';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='995b091e78fe2e0fb201e3c06272d9bef018594e3205c0a981152bc3f537eda9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='5babd67d884af6251b504932e2cdce2e5a969075efa856c91087ecc6f3933fc6';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='0225084f7067a8ccf5131b7656ea5ac62d6a68fbab71dc52aac24ab02299ee7a';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Oct 2025 18:55:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Oct 2025 18:55:58 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Oct 2025 18:56:30 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba";     TOMCAT_VERSION="9.0.111";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 30 Oct 2025 19:29:20 GMT
USER root
# Thu, 30 Oct 2025 19:29:20 GMT
ARG LIBERTY_VERSION=25.0.0.10
# Thu, 30 Oct 2025 19:29:20 GMT
ARG LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca
# Thu, 30 Oct 2025 19:29:20 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip
# Thu, 30 Oct 2025 19:29:20 GMT
ARG LIBERTY_BUILD_LABEL=cl251020250923-1355
# Thu, 30 Oct 2025 19:29:20 GMT
ARG OPENJ9_SCC=true
# Thu, 30 Oct 2025 19:29:20 GMT
ARG VERBOSE=false
# Thu, 30 Oct 2025 19:29:20 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251020250923-1355 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.10 liberty.version=25.0.0.10 io.openliberty.version=25.0.0.10
# Thu, 30 Oct 2025 19:29:20 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Thu, 30 Oct 2025 19:37:24 GMT
COPY helpers /opt/ol/helpers # buildkit
# Thu, 30 Oct 2025 19:37:25 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Thu, 30 Oct 2025 19:37:26 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Thu, 30 Oct 2025 19:37:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Thu, 30 Oct 2025 19:37:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 30 Oct 2025 19:37:38 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 30 Oct 2025 19:37:38 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Thu, 30 Oct 2025 19:37:45 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Thu, 30 Oct 2025 19:37:45 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 30 Oct 2025 19:37:45 GMT
USER 1001
# Thu, 30 Oct 2025 19:37:45 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 30 Oct 2025 19:37:45 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 30 Oct 2025 19:37:45 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d05c427cc331d7b6dd9baffe91a10981b54840825b7525c3636088e5c3447a5`  
		Last Modified: Thu, 30 Oct 2025 18:54:22 GMT  
		Size: 12.9 MB (12893771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dad38a6f242c4b5dee08d14932baf2065421a2115f9d2f873bef1841822ac0`  
		Last Modified: Thu, 30 Oct 2025 18:57:07 GMT  
		Size: 55.3 MB (55309348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a1817ff188ca2a51e323fac569cd105ca6ccf5baf2e70887d8e0b10da36506`  
		Last Modified: Thu, 30 Oct 2025 18:57:01 GMT  
		Size: 3.5 MB (3545922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d5d42e1387821ae763cb9478e0da817aa2c794c6942069de47e1eda9ad6002`  
		Last Modified: Thu, 30 Oct 2025 19:32:03 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1b47ae401650bb629fc3d99f8bf09d0d3608957958af732bb277fc9fd80e8b`  
		Last Modified: Thu, 30 Oct 2025 19:38:12 GMT  
		Size: 12.1 KB (12104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6127ad76f727c1de0717c50aa1b0a7cde9425f11128dc7cf3666a206bba4a81`  
		Last Modified: Thu, 30 Oct 2025 19:38:12 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c315d9234e11d98105e0a59ad5b1ede7084557617bfd86bfac68051db5cc960`  
		Last Modified: Thu, 30 Oct 2025 19:38:12 GMT  
		Size: 36.5 KB (36504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25dd3279cdfd3df1f9b8d4179507296280a640fbc2f5ba62f26d4d90dc161ee7`  
		Last Modified: Thu, 30 Oct 2025 19:38:14 GMT  
		Size: 14.9 MB (14868695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f32d938424bdea73e1f69ec0de06f6e97445bba749e0550cc855c4fe344522`  
		Last Modified: Thu, 30 Oct 2025 19:38:12 GMT  
		Size: 739.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124e1e56d24936f6aaeb620f5bb542ebedc9f10e67c4f5b32cd8fd4478f722e9`  
		Last Modified: Thu, 30 Oct 2025 19:38:12 GMT  
		Size: 13.2 KB (13214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9c43eb1000c5eda27d077b04acd69c5b326e0d5890810acfacf6882a55a0fa`  
		Last Modified: Thu, 30 Oct 2025 19:38:13 GMT  
		Size: 2.6 MB (2622070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:kernel-slim-java8-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:4d660581bc0cdffea9e26a4ef5b8fc4d79919b0bac867d1ccee0cfde681975a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3674ca10a5999a2df53ecdf1ba7c69c4bb0bf220ea05c1a79a47195780799049`

```dockerfile
```

-	Layers:
	-	`sha256:5889183053d8fb4ae24305c2720a8bbc728b64e2b448bbe66113729047ad5823`  
		Last Modified: Thu, 30 Oct 2025 20:46:49 GMT  
		Size: 3.9 MB (3900752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a89cb1e6355563505709ed620a6474bc91949652e806b422c3b22cae150feec7`  
		Last Modified: Thu, 30 Oct 2025 20:46:50 GMT  
		Size: 39.8 KB (39843 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:kernel-slim-java8-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:4b6eac353a030ea09717372ca041badf744f167832a1497b7de012e44ef5b7a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115848060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b3f19ceaeb782d507c405f3e2b7bdfb798ce9b0d1bedf4f5ac431e56ce1e63`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:26 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:28 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Wed, 01 Oct 2025 07:05:28 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 18:53:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Oct 2025 18:53:24 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 18:53:24 GMT
ENV JAVA_VERSION=jdk8u472-b08_openj9-0.56.0
# Thu, 30 Oct 2025 18:57:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='e9f04c51ace0cc724a7b3e54e58ad1823d899c77c2a141ab28efb226c3c7bb97';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='995b091e78fe2e0fb201e3c06272d9bef018594e3205c0a981152bc3f537eda9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='5babd67d884af6251b504932e2cdce2e5a969075efa856c91087ecc6f3933fc6';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='0225084f7067a8ccf5131b7656ea5ac62d6a68fbab71dc52aac24ab02299ee7a';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Oct 2025 18:57:34 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Oct 2025 18:57:34 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Oct 2025 18:58:07 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba";     TOMCAT_VERSION="9.0.111";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 30 Oct 2025 19:46:44 GMT
USER root
# Thu, 30 Oct 2025 19:46:44 GMT
ARG LIBERTY_VERSION=25.0.0.10
# Thu, 30 Oct 2025 19:46:44 GMT
ARG LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca
# Thu, 30 Oct 2025 19:46:44 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip
# Thu, 30 Oct 2025 19:46:44 GMT
ARG LIBERTY_BUILD_LABEL=cl251020250923-1355
# Thu, 30 Oct 2025 19:46:44 GMT
ARG OPENJ9_SCC=true
# Thu, 30 Oct 2025 19:46:44 GMT
ARG VERBOSE=false
# Thu, 30 Oct 2025 19:46:44 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251020250923-1355 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.10 liberty.version=25.0.0.10 io.openliberty.version=25.0.0.10
# Thu, 30 Oct 2025 19:46:44 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Thu, 30 Oct 2025 19:54:13 GMT
COPY helpers /opt/ol/helpers # buildkit
# Thu, 30 Oct 2025 19:54:14 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Thu, 30 Oct 2025 19:54:16 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Thu, 30 Oct 2025 19:54:29 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Thu, 30 Oct 2025 19:54:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 30 Oct 2025 19:54:30 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 30 Oct 2025 19:54:32 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Thu, 30 Oct 2025 19:54:41 GMT
# ARGS: LIBERTY_VERSION=25.0.0.10 LIBERTY_SHA=78dfbddacc7efe6b203fbe34558357002447a9ca LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.10/openliberty-kernel-25.0.0.10.zip LIBERTY_BUILD_LABEL=cl251020250923-1355 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Thu, 30 Oct 2025 19:54:41 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 30 Oct 2025 19:54:41 GMT
USER 1001
# Thu, 30 Oct 2025 19:54:41 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 30 Oct 2025 19:54:41 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 30 Oct 2025 19:54:41 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:e4a5a322dd65d010805129ca793d5d5e6b07872cbc2f41d566a84091b39c794e`  
		Last Modified: Thu, 02 Oct 2025 00:25:04 GMT  
		Size: 28.0 MB (28003413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85ec275e8f24c28d1884cb863f6a811d464cfb2b0e274ec7e8be26978e82f3c`  
		Last Modified: Thu, 30 Oct 2025 18:55:24 GMT  
		Size: 12.2 MB (12219687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e74e8fb4851467ab629f65e3d50391c452969550be2a4a823c6cdf09ffe9bb`  
		Last Modified: Thu, 30 Oct 2025 18:59:07 GMT  
		Size: 53.3 MB (53319798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159088ff6b0a160a9d8522a5af4c16db653e96839e7d10d1eedd5b451d6b6e75`  
		Last Modified: Thu, 30 Oct 2025 18:58:58 GMT  
		Size: 4.5 MB (4459583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00412d94d5a1195b6c098af1414078bc0497b5429ed544dde761b4c6ecac6404`  
		Last Modified: Thu, 30 Oct 2025 19:49:56 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3e44084258526c69d18f6d516f69e052a226e33e6ef212636f119ac03be43f`  
		Last Modified: Thu, 30 Oct 2025 19:55:20 GMT  
		Size: 12.1 KB (12105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a21ae4017e312d538aad5ee88e2d1248a9a1cd4c9a5eadd513679581760f02b`  
		Last Modified: Thu, 30 Oct 2025 19:55:24 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca86bfbb4e4b8fcf997897eeb94555fb0134c065af45f0b96f5f958e052dc56`  
		Last Modified: Thu, 30 Oct 2025 19:55:20 GMT  
		Size: 33.1 KB (33116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f693cac70d908206aa8cbafd58653ce3b5c3286efca0305813358c2acde4703`  
		Last Modified: Thu, 30 Oct 2025 19:55:21 GMT  
		Size: 14.9 MB (14868089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640724e32ce7d8f0dd47a39b56aa3bccfe3310b6137e85e0ee5d68107d05ec89`  
		Last Modified: Thu, 30 Oct 2025 19:55:20 GMT  
		Size: 739.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439bf03e9ff3a6777b6a77ab626fd03a5bb2d738a71f9171d3a0ecbde078ba39`  
		Last Modified: Thu, 30 Oct 2025 19:55:20 GMT  
		Size: 13.2 KB (13234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a545e9160e535e9adee3a07200821dda30853b71ca7c6b6a8b219922496c469`  
		Last Modified: Thu, 30 Oct 2025 19:55:21 GMT  
		Size: 2.9 MB (2917002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:kernel-slim-java8-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:8dffa23410e4f88bb6b457c7f148a30dde95c231a07edd71d7c5d35a3970decd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3936763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:349ba7f13074f6ba88d3395ebeeb4cb67e7f3b0b00207d873a15036cd32c9d1b`

```dockerfile
```

-	Layers:
	-	`sha256:46fcd71ffd63e29e5b7263e053df2f5a82b832e6470e9495810bf57829b90244`  
		Last Modified: Thu, 30 Oct 2025 20:46:56 GMT  
		Size: 3.9 MB (3896966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e52f01d936c36fa3f8d6c5641fef637ccb4442279956d299bad69df7a83a09b3`  
		Last Modified: Thu, 30 Oct 2025 20:46:56 GMT  
		Size: 39.8 KB (39797 bytes)  
		MIME: application/vnd.in-toto+json
