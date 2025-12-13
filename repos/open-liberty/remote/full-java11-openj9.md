## `open-liberty:full-java11-openj9`

```console
$ docker pull open-liberty@sha256:36e312ae579288b463ab2921bd56ab0e60ba71d4dd01782615d1072635f79b16
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

### `open-liberty:full-java11-openj9` - linux; amd64

```console
$ docker pull open-liberty@sha256:09a1bd19deca3a426cc316b7d3f8d9d6252fa2f5f2c1aa88d4c5ccffcac1f473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.1 MB (461131336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a382c199dfa140741e616d26bbde6b9731bb3625e0189de6c3b60c01e34f61d0`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:10:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 01 Dec 2025 23:10:01 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Dec 2025 23:10:01 GMT
ENV JAVA_VERSION=jdk-11.0.29+7_openj9-0.56.0
# Mon, 01 Dec 2025 23:10:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9fd5b1e5f18c80d945570cd86db46f737fdecbdcd8978d502c4a601f704c6676';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='16289eb013673a686abfef6631570e5b08c6171a1f7cf79fd495759d53393c38';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='474acb3b9c1ba608efe0c3aa0321a271cfbe2044e89d73e7129b0b013eb484df';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='42c7324f112975abc6a36c1cacad8f7515924cc60c21ac45e5985e7908d2c931';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 01 Dec 2025 23:10:04 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Dec 2025 23:10:04 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 01 Dec 2025 23:10:36 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 03 Dec 2025 21:47:33 GMT
USER root
# Wed, 03 Dec 2025 21:47:33 GMT
ARG LIBERTY_VERSION=25.0.0.12
# Wed, 03 Dec 2025 21:47:33 GMT
ARG LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3
# Wed, 03 Dec 2025 21:47:33 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip
# Wed, 03 Dec 2025 21:47:33 GMT
ARG LIBERTY_BUILD_LABEL=cl251220251117-0302
# Wed, 03 Dec 2025 21:47:33 GMT
ARG OPENJ9_SCC=true
# Wed, 03 Dec 2025 21:47:33 GMT
ARG VERBOSE=false
# Wed, 03 Dec 2025 21:47:33 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251220251117-0302 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.12 liberty.version=25.0.0.12 io.openliberty.version=25.0.0.12
# Wed, 03 Dec 2025 21:47:33 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 03 Dec 2025 21:47:33 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 03 Dec 2025 21:47:33 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 03 Dec 2025 21:47:34 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 03 Dec 2025 21:47:52 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 03 Dec 2025 21:47:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 03 Dec 2025 21:47:52 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 03 Dec 2025 21:47:52 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Wed, 03 Dec 2025 21:48:11 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 03 Dec 2025 21:48:11 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 03 Dec 2025 21:48:11 GMT
USER 1001
# Wed, 03 Dec 2025 21:48:11 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 03 Dec 2025 21:48:11 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 03 Dec 2025 21:48:11 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b188f6006db07bd00eff78992b755ce608a5eecba224eb4feffe4cbc7dbe1f7`  
		Last Modified: Mon, 01 Dec 2025 23:11:00 GMT  
		Size: 12.2 MB (12171796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f1557af6a49327d510ee4f0e4c03c1ff87d137621f3a50fbb34ecd45e58ae7`  
		Last Modified: Mon, 01 Dec 2025 23:11:10 GMT  
		Size: 55.4 MB (55434639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c55fb663654ce7df6bb1f3d54c6205d9f3abbaa1e71a90f79e6963bcc48271`  
		Last Modified: Mon, 01 Dec 2025 23:10:58 GMT  
		Size: 4.4 MB (4392710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5cd839456a7f8c85bd5a92be8284fff64cc23bfb1da499600bb53c223b62bf`  
		Last Modified: Wed, 03 Dec 2025 21:48:49 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8255cdbf49585d828df94a30c6bb62698339d7f9d69b339be6c8d42743b1a8b7`  
		Last Modified: Wed, 03 Dec 2025 21:48:49 GMT  
		Size: 12.3 KB (12287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d029af3b2ff157a95ce84f34a1eeb335dc0d2cf3fe3f12baae95b0c187cce7a`  
		Last Modified: Wed, 03 Dec 2025 21:48:49 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fdf82b694da97f85624957a9394ae403acd01596bc3db05b44347c150ed3e6d`  
		Last Modified: Wed, 03 Dec 2025 21:48:49 GMT  
		Size: 31.7 KB (31748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830ed8a02b9c789b581bce81291da0eaa355119e18426b4ede14d33a216af31d`  
		Last Modified: Thu, 04 Dec 2025 01:15:42 GMT  
		Size: 345.9 MB (345928124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76be023dace075215c4d64a17aa78d08976d3ab4230e8b98d6efde5f086c825`  
		Last Modified: Wed, 03 Dec 2025 21:48:49 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bdae3cc63986df5e023590ee5421c070251fb17ece7341dff5fe348739f105`  
		Last Modified: Wed, 03 Dec 2025 21:48:49 GMT  
		Size: 13.7 KB (13726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32cf46fa4acc470f6e6e9557a4966a5867e4cc54013ee9ce207f03c997f0fdfe`  
		Last Modified: Wed, 03 Dec 2025 21:48:51 GMT  
		Size: 13.6 MB (13607162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:e23da846f884c60fd40401e6b77a616d15a05f0d7c163f9c79ee4b5529225254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5756180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b53413c95779ef8f02d83ef12bd10353eb0d3062f1b72e64265dacde97afda56`

```dockerfile
```

-	Layers:
	-	`sha256:1ea10d66bcbbe2aeffa55f71095fd33278a66d7d31e445747af57843407263d4`  
		Last Modified: Thu, 04 Dec 2025 00:48:30 GMT  
		Size: 5.7 MB (5716816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de9e799ab26037caa2b39e32e7f6164c0181d14f38c54f299e7c615971ca1660`  
		Last Modified: Thu, 04 Dec 2025 00:48:33 GMT  
		Size: 39.4 KB (39364 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java11-openj9` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:a2cbc8622e993d35df3d66b6e1b5d172485fb5fef15ccaf9a03f75b01e0638a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **456.8 MB (456789467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71168e48080d97d08ecfb4e8b1cbc73f4fd11552c8478afe1a64010b5a24aae9`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 21:53:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 01 Dec 2025 21:53:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Dec 2025 21:53:34 GMT
ENV JAVA_VERSION=jdk-11.0.29+7_openj9-0.56.0
# Mon, 01 Dec 2025 21:54:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9fd5b1e5f18c80d945570cd86db46f737fdecbdcd8978d502c4a601f704c6676';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='16289eb013673a686abfef6631570e5b08c6171a1f7cf79fd495759d53393c38';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='474acb3b9c1ba608efe0c3aa0321a271cfbe2044e89d73e7129b0b013eb484df';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='42c7324f112975abc6a36c1cacad8f7515924cc60c21ac45e5985e7908d2c931';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 01 Dec 2025 21:54:42 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Dec 2025 21:54:42 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 01 Dec 2025 21:55:13 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 03 Dec 2025 21:46:53 GMT
USER root
# Wed, 03 Dec 2025 21:46:53 GMT
ARG LIBERTY_VERSION=25.0.0.12
# Wed, 03 Dec 2025 21:46:53 GMT
ARG LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3
# Wed, 03 Dec 2025 21:46:53 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip
# Wed, 03 Dec 2025 21:46:53 GMT
ARG LIBERTY_BUILD_LABEL=cl251220251117-0302
# Wed, 03 Dec 2025 21:46:53 GMT
ARG OPENJ9_SCC=true
# Wed, 03 Dec 2025 21:46:53 GMT
ARG VERBOSE=false
# Wed, 03 Dec 2025 21:46:53 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251220251117-0302 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.12 liberty.version=25.0.0.12 io.openliberty.version=25.0.0.12
# Wed, 03 Dec 2025 21:46:53 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 03 Dec 2025 21:46:53 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 03 Dec 2025 21:46:53 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 03 Dec 2025 21:46:53 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 03 Dec 2025 21:47:13 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 03 Dec 2025 21:47:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 03 Dec 2025 21:47:13 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 03 Dec 2025 21:47:13 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Wed, 03 Dec 2025 21:47:35 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 03 Dec 2025 21:47:35 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 03 Dec 2025 21:47:35 GMT
USER 1001
# Wed, 03 Dec 2025 21:47:35 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 03 Dec 2025 21:47:35 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 03 Dec 2025 21:47:35 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe5c25ace4281cda0a6beee2f596c784279f3a2b466d176ba28026d25852efd`  
		Last Modified: Mon, 01 Dec 2025 21:54:57 GMT  
		Size: 12.1 MB (12129891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402e0557a5db00b5b60ff7e347babbfdd7696ef12e5e16eecd068bc841a89646`  
		Last Modified: Mon, 01 Dec 2025 21:55:46 GMT  
		Size: 53.7 MB (53713602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7386bf36af963403218ba8a8bb42e4ab32a270b6c8e6e6f1a5efe9ce234bbfa`  
		Last Modified: Mon, 01 Dec 2025 21:55:39 GMT  
		Size: 4.3 MB (4264010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e8d38ab145a86b21a880854c10d69aa1858a5b220179389c00662077c3efba`  
		Last Modified: Wed, 03 Dec 2025 21:48:15 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415ed8af5f9a8c1a78fe01548c775b39ac3e7a3ddfcf0645fb93daca24ad2636`  
		Last Modified: Wed, 03 Dec 2025 21:48:15 GMT  
		Size: 12.3 KB (12283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1f6c61aefdef02892262a9815b96c80ce0934c33665ca19284cd349f1eb82c`  
		Last Modified: Wed, 03 Dec 2025 21:48:15 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e55ea93d5d55e2822b303f779dad2e2cb7c5b706041b121da7bb6fb2c72d636`  
		Last Modified: Wed, 03 Dec 2025 21:48:16 GMT  
		Size: 42.3 KB (42322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebed6e390539e8d0e68fafb9266f37651f52cf868be070ef564e5164bf5da10b`  
		Last Modified: Thu, 04 Dec 2025 01:16:40 GMT  
		Size: 345.9 MB (345928293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf7eb85d1e4ec0c7c5e741fbd6e4e584d87f86c6ae03cb0f0964fc4994c64ae`  
		Last Modified: Wed, 03 Dec 2025 21:48:16 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb3c607da4ce47c5f353950cf2147a2c2ce6dbc88e2fd1a3964c86d05cdb2af`  
		Last Modified: Wed, 03 Dec 2025 21:48:16 GMT  
		Size: 13.7 KB (13718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d79621e2995dc9f4a9cc310c900396682c1b3ab60edc51a6eeb2ceab5efec50`  
		Last Modified: Wed, 03 Dec 2025 21:48:17 GMT  
		Size: 13.3 MB (13299125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:76448119dd0e31fcb4437949cd5cdd381ce4bef938f5e3a1610c3f36258ed6bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5754668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:086957a74070e0a07d0b69bc09973068f4e126746262a3a335220d40e4fb746b`

```dockerfile
```

-	Layers:
	-	`sha256:964067e0baeca4a03184321913862dd2fe7635b0012f783522b4a98c975a6699`  
		Last Modified: Thu, 04 Dec 2025 00:48:38 GMT  
		Size: 5.7 MB (5715176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9175360b64dead7286a243607132a8b92a263f2916bba44f57131af7012e2db`  
		Last Modified: Thu, 04 Dec 2025 00:48:39 GMT  
		Size: 39.5 KB (39492 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java11-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:935b5a9373513e6740ab1b45c839dfcfe780ef4702ef495cd6137f414138b58f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.2 MB (466157180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d74262d8751877401c4ba1c7a4030fc2bf798b4e12e25a312c2e8598163f7c2a`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 21:53:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 01 Dec 2025 21:53:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Dec 2025 21:53:33 GMT
ENV JAVA_VERSION=jdk-11.0.29+7_openj9-0.56.0
# Mon, 01 Dec 2025 21:59:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9fd5b1e5f18c80d945570cd86db46f737fdecbdcd8978d502c4a601f704c6676';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='16289eb013673a686abfef6631570e5b08c6171a1f7cf79fd495759d53393c38';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='474acb3b9c1ba608efe0c3aa0321a271cfbe2044e89d73e7129b0b013eb484df';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='42c7324f112975abc6a36c1cacad8f7515924cc60c21ac45e5985e7908d2c931';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 01 Dec 2025 21:59:29 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Dec 2025 21:59:29 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 01 Dec 2025 22:00:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Mon, 01 Dec 2025 22:15:13 GMT
USER root
# Mon, 01 Dec 2025 22:15:13 GMT
ARG LIBERTY_VERSION=25.0.0.12
# Mon, 01 Dec 2025 22:15:13 GMT
ARG LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3
# Mon, 01 Dec 2025 22:15:13 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip
# Mon, 01 Dec 2025 22:15:13 GMT
ARG LIBERTY_BUILD_LABEL=cl251220251117-0302
# Mon, 01 Dec 2025 22:15:13 GMT
ARG OPENJ9_SCC=true
# Mon, 01 Dec 2025 22:15:13 GMT
ARG VERBOSE=false
# Mon, 01 Dec 2025 22:15:13 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251220251117-0302 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.12 liberty.version=25.0.0.12 io.openliberty.version=25.0.0.12
# Mon, 01 Dec 2025 22:15:13 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Mon, 01 Dec 2025 22:15:14 GMT
COPY helpers /opt/ol/helpers # buildkit
# Mon, 01 Dec 2025 22:15:14 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 03 Dec 2025 21:52:11 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 03 Dec 2025 21:52:45 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 03 Dec 2025 21:52:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 03 Dec 2025 21:52:46 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 03 Dec 2025 21:52:48 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Wed, 03 Dec 2025 21:53:26 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 03 Dec 2025 21:53:26 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 03 Dec 2025 21:53:26 GMT
USER 1001
# Wed, 03 Dec 2025 21:53:26 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 03 Dec 2025 21:53:26 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 03 Dec 2025 21:53:26 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Thu, 13 Nov 2025 23:02:18 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed02c429613f0e247ffa449100a48c06fced187c5ce8d553e21c41a27e3ae784`  
		Last Modified: Mon, 01 Dec 2025 21:55:07 GMT  
		Size: 12.9 MB (12893867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37be6f838c1885e59c4695d4bd908e38e217defee79992e2c0c2b47e2ae483f6`  
		Last Modified: Mon, 01 Dec 2025 22:00:58 GMT  
		Size: 57.3 MB (57283319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19908eadfd213736cb484c33ffb1437e524e4182db21025aa46d929620f52b87`  
		Last Modified: Mon, 01 Dec 2025 22:00:48 GMT  
		Size: 3.5 MB (3478787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1393d327d3844f1692f0ee241eff1d93506a83d6acdbf1cf58cbbd8c187cebaa`  
		Last Modified: Mon, 01 Dec 2025 22:18:00 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9705b707179de7438755d38fcf17f995b3a1cf1ec7013b6ce8ea527c6de92262`  
		Last Modified: Mon, 01 Dec 2025 22:18:06 GMT  
		Size: 12.3 KB (12285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a7f7b23a19f2f4573272f72922a1c047ca446a1d1fd3f7013ba540ebc4d88c`  
		Last Modified: Mon, 01 Dec 2025 22:18:00 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4240fd848dafd8d7a9b2a1a9e356241ecf9f1055dd8409ec07767d39759cad44`  
		Last Modified: Wed, 03 Dec 2025 21:54:48 GMT  
		Size: 36.5 KB (36498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2f4c998cb928e2091c0ed157411760a4546de344bf659e6124afd42efd0ce6`  
		Last Modified: Wed, 03 Dec 2025 22:39:01 GMT  
		Size: 345.9 MB (345928554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed647eb846d17df775fe33d034854363554c400a0659862112a7192e19bff0da`  
		Last Modified: Wed, 03 Dec 2025 21:54:48 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf34d5fdf70e14978334f7d4f5cecefe7b6c75dee86462ea06aa9f53f6ea3ed`  
		Last Modified: Wed, 03 Dec 2025 21:54:49 GMT  
		Size: 13.8 KB (13760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357e26bb35d9802f1065808f6ecb90ff1fe8ca85f57998d9fee986596b33e2ad`  
		Last Modified: Wed, 03 Dec 2025 21:54:50 GMT  
		Size: 12.1 MB (12061037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:6d2fb3899878f46c40e6fa59f248e8055f14ff979224a5c124388df8b52744f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5760835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b31f3273195e6324bbab565d53d9820f816fe0ba2b5eaaeec6dee488985ef374`

```dockerfile
```

-	Layers:
	-	`sha256:c28993fb0f084ae6b40dcd1ac8e5192abe18f4ee52c20a95f9be0471e605eea8`  
		Last Modified: Thu, 04 Dec 2025 00:48:44 GMT  
		Size: 5.7 MB (5721437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ee8e16b8d5303ffef869cc549a8654b1b99ad790bd2be732f1dda87645c19b0`  
		Last Modified: Thu, 04 Dec 2025 00:48:45 GMT  
		Size: 39.4 KB (39398 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java11-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:fa9b2115a0f63bed778eae76a7fb31acf1b8e6ac57d97f261aa993ab2febc5b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.6 MB (459630332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b85ae5975b94f978cb217523028bd3efa67c608130c9260b83f92132f1d3fea1`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:42 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:44 GMT
ADD file:3d940f8d55eafd405ad4e9fa11689b18e385411a264e560df2a7b1b1fd1c45ea in / 
# Mon, 13 Oct 2025 17:23:44 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 21:53:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 01 Dec 2025 21:53:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Dec 2025 21:53:32 GMT
ENV JAVA_VERSION=jdk-11.0.29+7_openj9-0.56.0
# Mon, 01 Dec 2025 21:55:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9fd5b1e5f18c80d945570cd86db46f737fdecbdcd8978d502c4a601f704c6676';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='16289eb013673a686abfef6631570e5b08c6171a1f7cf79fd495759d53393c38';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='474acb3b9c1ba608efe0c3aa0321a271cfbe2044e89d73e7129b0b013eb484df';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='42c7324f112975abc6a36c1cacad8f7515924cc60c21ac45e5985e7908d2c931';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 01 Dec 2025 21:55:36 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Dec 2025 21:55:36 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 01 Dec 2025 21:56:11 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Mon, 01 Dec 2025 22:11:07 GMT
USER root
# Mon, 01 Dec 2025 22:11:07 GMT
ARG LIBERTY_VERSION=25.0.0.12
# Mon, 01 Dec 2025 22:11:07 GMT
ARG LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3
# Mon, 01 Dec 2025 22:11:07 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip
# Mon, 01 Dec 2025 22:11:07 GMT
ARG LIBERTY_BUILD_LABEL=cl251220251117-0302
# Mon, 01 Dec 2025 22:11:07 GMT
ARG OPENJ9_SCC=true
# Mon, 01 Dec 2025 22:11:07 GMT
ARG VERBOSE=false
# Mon, 01 Dec 2025 22:11:07 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251220251117-0302 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.12 liberty.version=25.0.0.12 io.openliberty.version=25.0.0.12
# Mon, 01 Dec 2025 22:11:07 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Mon, 01 Dec 2025 22:11:07 GMT
COPY helpers /opt/ol/helpers # buildkit
# Mon, 01 Dec 2025 22:11:07 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 03 Dec 2025 21:48:33 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 03 Dec 2025 21:49:03 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 03 Dec 2025 21:49:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 03 Dec 2025 21:49:05 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 03 Dec 2025 21:49:07 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Wed, 03 Dec 2025 21:49:57 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 03 Dec 2025 21:49:57 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 03 Dec 2025 21:49:57 GMT
USER 1001
# Wed, 03 Dec 2025 21:49:57 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 03 Dec 2025 21:49:57 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 03 Dec 2025 21:49:57 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:d15824160d0d57e05338a0838871eb3f72224cf5de518ea6af54ba25e7e9c4da`  
		Last Modified: Thu, 13 Nov 2025 23:02:52 GMT  
		Size: 28.0 MB (28003285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b729344b6db60e029cbcc5ef912d5e5debcd7c143dafbbe8c4f8b0b91566586f`  
		Last Modified: Mon, 01 Dec 2025 21:55:05 GMT  
		Size: 12.2 MB (12219897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42d5a423a4f18d1f72410a67936ebbce038aea374d6b26269ed658d21d8f3e0`  
		Last Modified: Mon, 01 Dec 2025 21:56:56 GMT  
		Size: 54.4 MB (54423367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ede27f75c2972e60b04231060706a31e061bf6d324be517f4cfb9e297be56d`  
		Last Modified: Mon, 01 Dec 2025 21:56:50 GMT  
		Size: 4.7 MB (4703664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270a49987bdca4b91dc15defb1126bdbf2d47f98373afeff19980675911cb3b7`  
		Last Modified: Mon, 01 Dec 2025 22:13:36 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc1f487e15fba3e4dbaf84a7da2ccb30197eaf0be99fd8689d9a7976b68ccb2`  
		Last Modified: Mon, 01 Dec 2025 22:13:36 GMT  
		Size: 12.3 KB (12283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3052d087d03d3694ba8f84d43848932a9ab23a6a925dbf7908e83a223d0bf10`  
		Last Modified: Mon, 01 Dec 2025 22:13:36 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abce58ca101c16f39e8c35cd5805c569d9946976b568fc09f7b685549cdc538c`  
		Last Modified: Wed, 03 Dec 2025 21:51:12 GMT  
		Size: 33.1 KB (33110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4b61143593f9b5f23485dd984910f91c235c545ac6fa3fe549c40c8c207199`  
		Last Modified: Thu, 04 Dec 2025 01:17:20 GMT  
		Size: 345.9 MB (345927871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237d3133a9be63e7889106c7fdd1c27bf8216cd42cc75434a6cd936de5c6e964`  
		Last Modified: Wed, 03 Dec 2025 21:51:12 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0157b6f596e8c375a09c6400afffe6478b9045c01b2332b29347b5a77f12b135`  
		Last Modified: Wed, 03 Dec 2025 21:51:12 GMT  
		Size: 13.8 KB (13759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56d5fc154b9a3a77ac8966bf4e0aca44d3c0e02e810b17a2aa899516947f747`  
		Last Modified: Wed, 03 Dec 2025 21:51:13 GMT  
		Size: 14.3 MB (14290745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:c01d373ca7ba42fcfd6f37abce2201c9a85d68e63e16577805e589e164e9413a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5757197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4358ec5e5c2d3a3a689c23703f14979435afd1d166a6c2d3121b782b0f21a6`

```dockerfile
```

-	Layers:
	-	`sha256:a79316267fa0993712a55987d4fac4e3316747429c3af3ea202253e73b032095`  
		Last Modified: Thu, 04 Dec 2025 00:48:49 GMT  
		Size: 5.7 MB (5717833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23721ad4210e2e33a10bce2d763d6e2731607a355d922b641bffe879a055dce6`  
		Last Modified: Thu, 04 Dec 2025 00:48:50 GMT  
		Size: 39.4 KB (39364 bytes)  
		MIME: application/vnd.in-toto+json
