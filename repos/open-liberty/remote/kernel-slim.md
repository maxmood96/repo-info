## `open-liberty:kernel-slim`

```console
$ docker pull open-liberty@sha256:e518fb4e98b19d5f54aeeaf173f73e0ade3c93bfe91f3982d1f4073c800d6150
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

### `open-liberty:kernel-slim` - linux; amd64

```console
$ docker pull open-liberty@sha256:a0cad2e172f0ad7f367791efce213184f3a67da97e6ff5e6ccd546710358cb73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117789278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf8952198aa9947b90e7be40a00cdc2623ad13d988f53a83f5e2f360435368f`
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
# Mon, 01 Dec 2025 23:09:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 01 Dec 2025 23:09:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Dec 2025 23:09:14 GMT
ENV JAVA_VERSION=jdk8u472-b08_openj9-0.56.0
# Mon, 01 Dec 2025 23:09:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='e9f04c51ace0cc724a7b3e54e58ad1823d899c77c2a141ab28efb226c3c7bb97';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='995b091e78fe2e0fb201e3c06272d9bef018594e3205c0a981152bc3f537eda9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='5babd67d884af6251b504932e2cdce2e5a969075efa856c91087ecc6f3933fc6';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='0225084f7067a8ccf5131b7656ea5ac62d6a68fbab71dc52aac24ab02299ee7a';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 01 Dec 2025 23:09:17 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Dec 2025 23:09:17 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 01 Dec 2025 23:09:48 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 03 Dec 2025 21:47:23 GMT
USER root
# Wed, 03 Dec 2025 21:47:23 GMT
ARG LIBERTY_VERSION=25.0.0.12
# Wed, 03 Dec 2025 21:47:23 GMT
ARG LIBERTY_SHA=91bf2c36c89259822dcd5d7c61d59cce835c9163
# Wed, 03 Dec 2025 21:47:23 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.12/openliberty-kernel-25.0.0.12.zip
# Wed, 03 Dec 2025 21:47:23 GMT
ARG LIBERTY_BUILD_LABEL=cl251220251117-0302
# Wed, 03 Dec 2025 21:47:23 GMT
ARG OPENJ9_SCC=true
# Wed, 03 Dec 2025 21:47:23 GMT
ARG VERBOSE=false
# Wed, 03 Dec 2025 21:47:23 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251220251117-0302 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.12 liberty.version=25.0.0.12 io.openliberty.version=25.0.0.12
# Wed, 03 Dec 2025 21:47:23 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 03 Dec 2025 21:47:23 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 03 Dec 2025 21:47:23 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 03 Dec 2025 21:47:23 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=91bf2c36c89259822dcd5d7c61d59cce835c9163 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.12/openliberty-kernel-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 03 Dec 2025 21:47:31 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=91bf2c36c89259822dcd5d7c61d59cce835c9163 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.12/openliberty-kernel-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 03 Dec 2025 21:47:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 03 Dec 2025 21:47:31 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=91bf2c36c89259822dcd5d7c61d59cce835c9163 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.12/openliberty-kernel-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 03 Dec 2025 21:47:32 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=91bf2c36c89259822dcd5d7c61d59cce835c9163 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.12/openliberty-kernel-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Wed, 03 Dec 2025 21:47:34 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=91bf2c36c89259822dcd5d7c61d59cce835c9163 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.12/openliberty-kernel-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 03 Dec 2025 21:47:34 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 03 Dec 2025 21:47:34 GMT
USER 1001
# Wed, 03 Dec 2025 21:47:34 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 03 Dec 2025 21:47:34 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 03 Dec 2025 21:47:34 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98dbe6a449def6acf0185c7dd104a13d9bf9fe553f907aeae6c49c653d60593`  
		Last Modified: Mon, 01 Dec 2025 23:10:09 GMT  
		Size: 12.2 MB (12171780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b35c8a21e781fd9a8ca6dbfd1ef68934ee13f36fb3b7ce9d47dcb00f30cdcb`  
		Last Modified: Mon, 01 Dec 2025 23:10:13 GMT  
		Size: 53.7 MB (53730424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c202eabb5a0a5d81253ae53c87e64d97aa88aed4bc1f02a83c6e41eeb4745a`  
		Last Modified: Mon, 01 Dec 2025 23:10:09 GMT  
		Size: 4.3 MB (4314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb295272f96a19ec8214288140892e762c79dcd43944cfa3e4fb736a578fbcd7`  
		Last Modified: Wed, 03 Dec 2025 21:47:50 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e005be8d436c3db8d30875c451ef5ec83ae8611b50ea0aca0547a8156bcdbc`  
		Last Modified: Wed, 03 Dec 2025 21:47:50 GMT  
		Size: 11.8 KB (11823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe635f1505a6a762df086081a0ab1354d5c5e4a27d9c85ae2a1285f644e97ad7`  
		Last Modified: Wed, 03 Dec 2025 21:47:50 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d2a85969acc6c1d1640f01f10d95fe8fddf202f02d25e66f04b7fc9e06fe26`  
		Last Modified: Wed, 03 Dec 2025 21:47:50 GMT  
		Size: 31.7 KB (31747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f030543a930da433e8e83ad37cc9dc4dfbb119547cacdb434783589a5a5e0a83`  
		Last Modified: Wed, 03 Dec 2025 21:47:52 GMT  
		Size: 15.2 MB (15230489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7c2eaf5e550d807241dc0d9113a14dde2245f94ae716e31caf45526c266a16`  
		Last Modified: Wed, 03 Dec 2025 21:47:50 GMT  
		Size: 738.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca0474df9a0efb8b3e41ea87066584409eeb29f82909d1c39c0f4c154f2ffd5`  
		Last Modified: Wed, 03 Dec 2025 21:47:50 GMT  
		Size: 12.9 KB (12948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b88c682c98f8ab8e2f6dbf89de723b17814a5f90aded36968e22bb43017e8f`  
		Last Modified: Wed, 03 Dec 2025 21:47:51 GMT  
		Size: 2.7 MB (2746388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:kernel-slim` - unknown; unknown

```console
$ docker pull open-liberty@sha256:ad09585eee09eef57a8b4761511b8256e22e2fdc187bf7020d6ed4d523165e2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3935747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6edb53a09cda1b62141d4de7e14b8060a4f5b2be7a7bb5ed11061a5de99aca`

```dockerfile
```

-	Layers:
	-	`sha256:fba1539a8341cfb8074c52eb302ef15d62ec6bf7733ca069a8958b16b94233e3`  
		Last Modified: Thu, 04 Dec 2025 00:46:55 GMT  
		Size: 3.9 MB (3895949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcec99eb896c1fac4b8a3a3844dff91469f163c4649cce75bed6899221cd995a`  
		Last Modified: Thu, 04 Dec 2025 00:46:56 GMT  
		Size: 39.8 KB (39798 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:kernel-slim` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:e89b4dcaff5f701b3f537867c75e1fb8c05d80a0f68a78a3b283a3b57a98042e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115128998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346480446eb6d113937c6eef7071ee1878c72c84c0bb5b39d60a42cf5f14af63`
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
# Mon, 01 Dec 2025 21:54:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 01 Dec 2025 21:54:49 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Dec 2025 21:54:49 GMT
ENV JAVA_VERSION=jdk8u472-b08_openj9-0.56.0
# Mon, 01 Dec 2025 21:54:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='e9f04c51ace0cc724a7b3e54e58ad1823d899c77c2a141ab28efb226c3c7bb97';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='995b091e78fe2e0fb201e3c06272d9bef018594e3205c0a981152bc3f537eda9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='5babd67d884af6251b504932e2cdce2e5a969075efa856c91087ecc6f3933fc6';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='0225084f7067a8ccf5131b7656ea5ac62d6a68fbab71dc52aac24ab02299ee7a';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 01 Dec 2025 21:54:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Dec 2025 21:54:52 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 01 Dec 2025 21:55:23 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 03 Dec 2025 21:47:17 GMT
USER root
# Wed, 03 Dec 2025 21:47:17 GMT
ARG LIBERTY_VERSION=25.0.0.12
# Wed, 03 Dec 2025 21:47:17 GMT
ARG LIBERTY_SHA=91bf2c36c89259822dcd5d7c61d59cce835c9163
# Wed, 03 Dec 2025 21:47:17 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.12/openliberty-kernel-25.0.0.12.zip
# Wed, 03 Dec 2025 21:47:17 GMT
ARG LIBERTY_BUILD_LABEL=cl251220251117-0302
# Wed, 03 Dec 2025 21:47:17 GMT
ARG OPENJ9_SCC=true
# Wed, 03 Dec 2025 21:47:17 GMT
ARG VERBOSE=false
# Wed, 03 Dec 2025 21:47:17 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251220251117-0302 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.12 liberty.version=25.0.0.12 io.openliberty.version=25.0.0.12
# Wed, 03 Dec 2025 21:47:17 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 03 Dec 2025 21:47:17 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 03 Dec 2025 21:47:17 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 03 Dec 2025 21:47:17 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=91bf2c36c89259822dcd5d7c61d59cce835c9163 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.12/openliberty-kernel-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 03 Dec 2025 21:47:28 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=91bf2c36c89259822dcd5d7c61d59cce835c9163 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.12/openliberty-kernel-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 03 Dec 2025 21:47:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 03 Dec 2025 21:47:29 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=91bf2c36c89259822dcd5d7c61d59cce835c9163 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.12/openliberty-kernel-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 03 Dec 2025 21:47:29 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=91bf2c36c89259822dcd5d7c61d59cce835c9163 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.12/openliberty-kernel-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Wed, 03 Dec 2025 21:47:33 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=91bf2c36c89259822dcd5d7c61d59cce835c9163 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.12/openliberty-kernel-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 03 Dec 2025 21:47:33 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 03 Dec 2025 21:47:33 GMT
USER 1001
# Wed, 03 Dec 2025 21:47:33 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 03 Dec 2025 21:47:33 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 03 Dec 2025 21:47:33 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5c682422801bb14f8d688a7a6305da36e5e73d85b5178dcc1a35d8071f6bed`  
		Last Modified: Mon, 01 Dec 2025 21:55:44 GMT  
		Size: 12.1 MB (12130037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6f85275d523f98b42ee443d57dfc90f3e4e4e7b51af93f6c02fd8786ab05ca`  
		Last Modified: Mon, 01 Dec 2025 21:55:53 GMT  
		Size: 53.4 MB (53440936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22511a6517e63a3495bbe6b13b9c57bfd33ea690bd2c40143b776dadcb807a20`  
		Last Modified: Mon, 01 Dec 2025 21:55:43 GMT  
		Size: 4.1 MB (4126610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea3f4f4103eef14aec9c435e7fe61742b7483f7d6fc5d14398365325af6a335`  
		Last Modified: Wed, 03 Dec 2025 21:47:50 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea8791d2da878fb775089e61447ccac62f47db63d9bb66055bd4cf02b6cd527`  
		Last Modified: Wed, 03 Dec 2025 21:47:50 GMT  
		Size: 11.8 KB (11827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f1d1593eeb8938c0e4cb4dea05faf273aa5d3037d2278829aabb85679f4d46`  
		Last Modified: Wed, 03 Dec 2025 21:47:50 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228e700fcf8e64a77e3088dae1ec73889696c3f1c44bfe0e18cb83ba942ab76e`  
		Last Modified: Wed, 03 Dec 2025 21:47:50 GMT  
		Size: 42.3 KB (42323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f29a69ebbf2d8b4c81293dcb554537fed901121548b80f38979bfdbd6e9cc0a`  
		Last Modified: Wed, 03 Dec 2025 21:47:53 GMT  
		Size: 15.2 MB (15230558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8d85377ccf67b654120e8f44765a98d2194e1f30f886061db981d9c140e4ca`  
		Last Modified: Wed, 03 Dec 2025 21:47:50 GMT  
		Size: 738.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2820a2f33b04c6fbd185d0540d73fa2c2ef590831d91215309ecc82aca6a9dba`  
		Last Modified: Wed, 03 Dec 2025 21:47:50 GMT  
		Size: 12.9 KB (12921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffe5a36303b04205b3de908888ec83dbde4468551c70b8e8c5ee30ea15170f6`  
		Last Modified: Wed, 03 Dec 2025 21:47:50 GMT  
		Size: 2.7 MB (2747879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:kernel-slim` - unknown; unknown

```console
$ docker pull open-liberty@sha256:badd77e0b14d7f7a78f81f2521cc8672966c6af8f40a1a80e817123bc998ee99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3935719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c1db48235ddf831786defa9981c6b910c46d4ba35f115c60cb1aa29237884b3`

```dockerfile
```

-	Layers:
	-	`sha256:27735034647fc484f00a4d608b7754b59fbd08c3247520fb09f65cff5aceeff1`  
		Last Modified: Thu, 04 Dec 2025 00:47:01 GMT  
		Size: 3.9 MB (3895769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:540097d8ff58067dbfb71553efca9a67635a54b06a90ff47b02d2d5fca093407`  
		Last Modified: Thu, 04 Dec 2025 00:47:02 GMT  
		Size: 40.0 KB (39950 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:kernel-slim` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:04f46f0126a13dcfb0b6259aac97e3d6585b2d66f521bc22e2509d3df3ffeaf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 MB (124074230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2ddfcc5ccc62d4e01957bd29846bc7a7a66b71ba51a177bb729ec537a14119`
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
ENV JAVA_VERSION=jdk8u472-b08_openj9-0.56.0
# Mon, 01 Dec 2025 21:55:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='e9f04c51ace0cc724a7b3e54e58ad1823d899c77c2a141ab28efb226c3c7bb97';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='995b091e78fe2e0fb201e3c06272d9bef018594e3205c0a981152bc3f537eda9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='5babd67d884af6251b504932e2cdce2e5a969075efa856c91087ecc6f3933fc6';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='0225084f7067a8ccf5131b7656ea5ac62d6a68fbab71dc52aac24ab02299ee7a';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 01 Dec 2025 21:55:25 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Dec 2025 21:55:25 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 01 Dec 2025 21:55:59 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Mon, 01 Dec 2025 22:15:13 GMT
USER root
# Mon, 01 Dec 2025 22:15:13 GMT
ARG LIBERTY_VERSION=25.0.0.12
# Mon, 01 Dec 2025 22:15:13 GMT
ARG LIBERTY_SHA=91bf2c36c89259822dcd5d7c61d59cce835c9163
# Mon, 01 Dec 2025 22:15:13 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.12/openliberty-kernel-25.0.0.12.zip
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
# Mon, 01 Dec 2025 22:18:51 GMT
COPY helpers /opt/ol/helpers # buildkit
# Mon, 01 Dec 2025 22:18:52 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 03 Dec 2025 21:48:43 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=91bf2c36c89259822dcd5d7c61d59cce835c9163 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.12/openliberty-kernel-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 03 Dec 2025 21:48:54 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=91bf2c36c89259822dcd5d7c61d59cce835c9163 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.12/openliberty-kernel-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 03 Dec 2025 21:48:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 03 Dec 2025 21:48:54 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=91bf2c36c89259822dcd5d7c61d59cce835c9163 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.12/openliberty-kernel-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 03 Dec 2025 21:48:55 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=91bf2c36c89259822dcd5d7c61d59cce835c9163 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.12/openliberty-kernel-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Wed, 03 Dec 2025 21:49:03 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=91bf2c36c89259822dcd5d7c61d59cce835c9163 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.12/openliberty-kernel-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 03 Dec 2025 21:49:03 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 03 Dec 2025 21:49:03 GMT
USER 1001
# Wed, 03 Dec 2025 21:49:03 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 03 Dec 2025 21:49:03 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 03 Dec 2025 21:49:03 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Tue, 13 Jan 2026 01:30:07 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed02c429613f0e247ffa449100a48c06fced187c5ce8d553e21c41a27e3ae784`  
		Last Modified: Mon, 01 Dec 2025 21:55:07 GMT  
		Size: 12.9 MB (12893867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a25c6a5213916040c318446523626d7ebcc1fdb6e5dfabb58c732f98ab93c1`  
		Last Modified: Mon, 01 Dec 2025 21:56:43 GMT  
		Size: 55.3 MB (55309347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385a6f4ec42048f4217220ab962943ab50c7cb278f46da5909f962c54d4d049a`  
		Last Modified: Mon, 01 Dec 2025 21:56:37 GMT  
		Size: 3.5 MB (3503887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1393d327d3844f1692f0ee241eff1d93506a83d6acdbf1cf58cbbd8c187cebaa`  
		Last Modified: Mon, 01 Dec 2025 22:18:00 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360aea7a41191a1c894e25d5f735b649d10dea137c32f23f1b697e6bc502d1b2`  
		Last Modified: Mon, 01 Dec 2025 22:20:02 GMT  
		Size: 11.8 KB (11825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea4821a9f178ec5fa5473380f75f426b4214493de82b478168f355f8a89226c`  
		Last Modified: Mon, 01 Dec 2025 22:20:02 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77118e1f5c20bd708c2cfacf6bf12fad97a1532f25424f558faa2181c1a257f4`  
		Last Modified: Wed, 03 Dec 2025 21:49:31 GMT  
		Size: 36.5 KB (36498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3b84898e7df0934f0d06d1cb46ceb8837bf90b4ac1598dc6159a98eb3bbc3c`  
		Last Modified: Wed, 03 Dec 2025 21:49:35 GMT  
		Size: 15.2 MB (15230873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d021db1f34eee906cd5357b6b15985bd2b36a16d64753eade1f85f7ce02dc951`  
		Last Modified: Wed, 03 Dec 2025 21:49:31 GMT  
		Size: 741.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47e6fd8801d5e4caa526859d8e8c91133acc812e5e2f6254a8ed4f7f9825ff7`  
		Last Modified: Wed, 03 Dec 2025 21:49:31 GMT  
		Size: 12.9 KB (12942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d9c09b3a8a5c4e6d56ab7ec165e9fe88548926182e1740a356efcd91e57ba8`  
		Last Modified: Wed, 03 Dec 2025 21:49:31 GMT  
		Size: 2.6 MB (2626234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:kernel-slim` - unknown; unknown

```console
$ docker pull open-liberty@sha256:5ea37f2eee1479b2ddd543e299663a7b93ff39ba2124c5daf6078e1af35556d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03b2f7653b9ba273779b2df6945775f17bb2f79aefce04a8845fd4884f49065`

```dockerfile
```

-	Layers:
	-	`sha256:3a2e7098f472ef3e809607e42571a052cde4f306d992d62ee28e970a66fc531f`  
		Last Modified: Thu, 04 Dec 2025 00:47:07 GMT  
		Size: 3.9 MB (3900752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:107cd696b7d028029268dde2ae7884cc898f24874f9f7a9cfae876b9c9960fb4`  
		Last Modified: Thu, 04 Dec 2025 00:47:08 GMT  
		Size: 39.8 KB (39844 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:kernel-slim` - linux; s390x

```console
$ docker pull open-liberty@sha256:7c3fa03c1f3cc89202bd7811ac488b0156acba1d57e03cd5caca584079b41976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.1 MB (116077719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c1404293b1e3c23739300594fcefe0e13504c842b9a7c034cd1e32908143d0`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 09 Jan 2026 07:05:09 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:05:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:05:11 GMT
ADD file:03078bbac5343c8831dae57f317f9a6ced24a6c8b7192435e81027780f524a3a in / 
# Fri, 09 Jan 2026 07:05:11 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:11:59 GMT
ENV JAVA_VERSION=jdk8u472-b08_openj9-0.56.0
# Thu, 15 Jan 2026 22:12:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='e9f04c51ace0cc724a7b3e54e58ad1823d899c77c2a141ab28efb226c3c7bb97';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='995b091e78fe2e0fb201e3c06272d9bef018594e3205c0a981152bc3f537eda9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='5babd67d884af6251b504932e2cdce2e5a969075efa856c91087ecc6f3933fc6';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='0225084f7067a8ccf5131b7656ea5ac62d6a68fbab71dc52aac24ab02299ee7a';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 15 Jan 2026 22:12:01 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:12:01 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 15 Jan 2026 22:12:32 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 15 Jan 2026 22:53:36 GMT
USER root
# Thu, 15 Jan 2026 22:53:36 GMT
ARG LIBERTY_VERSION=25.0.0.12
# Thu, 15 Jan 2026 22:53:36 GMT
ARG LIBERTY_SHA=91bf2c36c89259822dcd5d7c61d59cce835c9163
# Thu, 15 Jan 2026 22:53:36 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.12/openliberty-kernel-25.0.0.12.zip
# Thu, 15 Jan 2026 22:53:36 GMT
ARG LIBERTY_BUILD_LABEL=cl251220251117-0302
# Thu, 15 Jan 2026 22:53:36 GMT
ARG OPENJ9_SCC=true
# Thu, 15 Jan 2026 22:53:36 GMT
ARG VERBOSE=false
# Thu, 15 Jan 2026 22:53:36 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251220251117-0302 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.12 liberty.version=25.0.0.12 io.openliberty.version=25.0.0.12
# Thu, 15 Jan 2026 22:53:36 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Thu, 15 Jan 2026 22:54:04 GMT
COPY helpers /opt/ol/helpers # buildkit
# Thu, 15 Jan 2026 22:54:04 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Thu, 15 Jan 2026 22:54:04 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=91bf2c36c89259822dcd5d7c61d59cce835c9163 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.12/openliberty-kernel-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Thu, 15 Jan 2026 22:54:09 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=91bf2c36c89259822dcd5d7c61d59cce835c9163 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.12/openliberty-kernel-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Thu, 15 Jan 2026 22:54:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 15 Jan 2026 22:54:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=91bf2c36c89259822dcd5d7c61d59cce835c9163 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.12/openliberty-kernel-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 15 Jan 2026 22:54:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=91bf2c36c89259822dcd5d7c61d59cce835c9163 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.12/openliberty-kernel-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Thu, 15 Jan 2026 22:54:14 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=91bf2c36c89259822dcd5d7c61d59cce835c9163 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.12/openliberty-kernel-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Thu, 15 Jan 2026 22:54:14 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 15 Jan 2026 22:54:14 GMT
USER 1001
# Thu, 15 Jan 2026 22:54:14 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 15 Jan 2026 22:54:14 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 15 Jan 2026 22:54:14 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:a0be7aa393c334078596b27f39dc3946551a30dd1cad58fe06cce6be05b244b2`  
		Last Modified: Thu, 15 Jan 2026 21:43:58 GMT  
		Size: 28.0 MB (28003138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1421ff1e62d1ac76e2d8a34fa67faf578cf114b64b34c9d5c7c3a05835f2924`  
		Last Modified: Thu, 15 Jan 2026 22:13:00 GMT  
		Size: 12.2 MB (12220151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8bf3a4fc2d61dc3c4745019e51665d0f9029e7459a2c4261eb3bc08b5e8b5e`  
		Last Modified: Thu, 15 Jan 2026 22:13:04 GMT  
		Size: 53.3 MB (53319766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f6f4138aa794e673234435372ef0886abee9c0e749446ca76b57e1afcada4`  
		Last Modified: Thu, 15 Jan 2026 22:12:59 GMT  
		Size: 4.4 MB (4418349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a088c3d8721ad81c18f9f955fb47ed77c86cd113b13423bf1e6d04da6a9c03c`  
		Last Modified: Thu, 15 Jan 2026 22:54:33 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff42c470ade58b502c30fee4c4a7e2f477eab7c4fedb207af4f3cc4de7f4fe50`  
		Last Modified: Thu, 15 Jan 2026 22:54:33 GMT  
		Size: 11.8 KB (11827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3035c8fb5c8c31baa678a1aef300350ff1d755b2dd1e29b83d805d59b593ac6b`  
		Last Modified: Thu, 15 Jan 2026 22:54:34 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25e9775484b1288c5998083728831c4222c9fccf9e6277cd14530cee85d800d`  
		Last Modified: Thu, 15 Jan 2026 22:54:33 GMT  
		Size: 33.1 KB (33110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf748eadbd9ce800282b0a138143ae844c692b761b9a2f0c96e92c3b229d884`  
		Last Modified: Thu, 15 Jan 2026 22:54:34 GMT  
		Size: 15.2 MB (15230027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b68dcf23ea0d9d11f4ddd82c966dc15c2d757fd8e0e038ceaea4988a0bb0dc`  
		Last Modified: Thu, 15 Jan 2026 22:54:33 GMT  
		Size: 739.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70318e9f4e1e3c17c43ed4aadacea04eb70c34172c6f89378affc4d0b747c31a`  
		Last Modified: Thu, 15 Jan 2026 22:54:33 GMT  
		Size: 12.9 KB (12928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421a64b4f131a15bda655ea45c4616c9ca34fae636e86e616ceafb124a96b04b`  
		Last Modified: Thu, 15 Jan 2026 22:54:34 GMT  
		Size: 2.8 MB (2826393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:kernel-slim` - unknown; unknown

```console
$ docker pull open-liberty@sha256:5738013731fd39a037d1cfe6db6149fd97c021fbd55a8ee6d8a855c41f533eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3935972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe37857dec8358ccfd9b030aa204ad2ed138483df6672a6ebbf2809a99fefaa`

```dockerfile
```

-	Layers:
	-	`sha256:a00be0fc0245212fb899a414e1bfbb29755a46bf85752e71155fba517dfb538d`  
		Last Modified: Fri, 16 Jan 2026 00:47:47 GMT  
		Size: 3.9 MB (3896978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fc5d73fae2fab0de5b2b8d4458f9787f5d7d515e813c03d8a164d89785a7b43`  
		Last Modified: Fri, 16 Jan 2026 00:47:47 GMT  
		Size: 39.0 KB (38994 bytes)  
		MIME: application/vnd.in-toto+json
