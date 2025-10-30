## `websphere-liberty:kernel-java11-openj9`

```console
$ docker pull websphere-liberty@sha256:f4ad3b752864b0c1a2bfd7057583fb58f5e48a751704d0e4fd22961f198aa60c
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

### `websphere-liberty:kernel-java11-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:c302f2ad2367b9f6e31c48fab11ebe8d6252c8ab0d788eba49bfbb9a41debce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.1 MB (122065843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9b1f33ede20d9d209e34de2e34435ee196ef66ca8f6aa8cd9abec748753fa8`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

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
# Thu, 30 Oct 2025 18:57:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Oct 2025 18:57:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 18:57:14 GMT
ENV JAVA_VERSION=jdk-11.0.29+7_openj9-0.56.0
# Thu, 30 Oct 2025 18:57:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9fd5b1e5f18c80d945570cd86db46f737fdecbdcd8978d502c4a601f704c6676';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='16289eb013673a686abfef6631570e5b08c6171a1f7cf79fd495759d53393c38';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='474acb3b9c1ba608efe0c3aa0321a271cfbe2044e89d73e7129b0b013eb484df';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='42c7324f112975abc6a36c1cacad8f7515924cc60c21ac45e5985e7908d2c931';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Oct 2025 18:57:17 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Oct 2025 18:57:17 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Oct 2025 18:57:48 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba";     TOMCAT_VERSION="9.0.111";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 30 Oct 2025 19:16:47 GMT
USER root
# Thu, 30 Oct 2025 19:16:47 GMT
ARG VERBOSE=false
# Thu, 30 Oct 2025 19:16:47 GMT
ARG OPENJ9_SCC=true
# Thu, 30 Oct 2025 19:16:47 GMT
ARG LIBERTY_VERSION=25.0.0.10
# Thu, 30 Oct 2025 19:16:47 GMT
ARG LIBERTY_BUILD_LABEL=cl251020250923-1355
# Thu, 30 Oct 2025 19:16:47 GMT
ARG LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa
# Thu, 30 Oct 2025 19:16:47 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.10 org.opencontainers.image.revision=cl251020250923-1355 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.10 com.ibm.websphere.liberty.version=25.0.0.10
# Thu, 30 Oct 2025 19:16:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Thu, 30 Oct 2025 19:16:47 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.10 BuildLabel=cl251020250923-1355
# Thu, 30 Oct 2025 19:16:47 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Thu, 30 Oct 2025 19:16:47 GMT
ARG LIBERTY_URL
# Thu, 30 Oct 2025 19:16:47 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 30 Oct 2025 19:17:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 19:17:13 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 30 Oct 2025 19:17:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 30 Oct 2025 19:17:13 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Thu, 30 Oct 2025 19:17:13 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Thu, 30 Oct 2025 19:17:13 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Thu, 30 Oct 2025 19:17:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Thu, 30 Oct 2025 19:17:17 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Thu, 30 Oct 2025 19:17:17 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 30 Oct 2025 19:17:17 GMT
USER 1001
# Thu, 30 Oct 2025 19:17:17 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 30 Oct 2025 19:17:17 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 30 Oct 2025 19:17:17 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974be5de89f7216537fde0b3a5e08956e0e9824621147c8726917b833c20facf`  
		Last Modified: Thu, 30 Oct 2025 18:58:10 GMT  
		Size: 12.2 MB (12171646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29696f404a7dca35a5c964284fe247d031701f6d03e253a2f6c1ee48960ed82`  
		Last Modified: Thu, 30 Oct 2025 18:58:17 GMT  
		Size: 55.4 MB (55434640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20933a95bdc2c483315b6f60683445356b8222c959b12d8d7dc3883f9482fdab`  
		Last Modified: Thu, 30 Oct 2025 18:58:08 GMT  
		Size: 4.4 MB (4411847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83f94ad6f2f3f21af8a9463e3623b1546e06412ca0228fe2c69ee26b5a01af5`  
		Last Modified: Thu, 30 Oct 2025 19:17:33 GMT  
		Size: 31.7 KB (31747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2249e2c1cc39db19c52ae315c9fb76389fc27fad52d25e62352991c9973940`  
		Last Modified: Thu, 30 Oct 2025 19:17:36 GMT  
		Size: 17.7 MB (17668809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21be9a580028f7c854b097086155052c4e1dca04072b2d1a884cd788ff110a5a`  
		Last Modified: Thu, 30 Oct 2025 19:17:33 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e282aa277a077eda7549f6801ac8e7e666990588dd849b56f7e986f6bbae61c`  
		Last Modified: Thu, 30 Oct 2025 19:17:33 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8e61d74247cf4d0106d8ca81ac289eed155280f626a31782e25b509e861f9f`  
		Last Modified: Thu, 30 Oct 2025 19:17:33 GMT  
		Size: 14.4 KB (14387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3563858c2eb4962998a823aa03e8eccc3302ffa2f575b4f5629aacf4b685dd`  
		Last Modified: Thu, 30 Oct 2025 19:17:33 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283674b7e48661889b4543d9c5fd21193654d06b1dd7016182f0faca31c53ec1`  
		Last Modified: Thu, 30 Oct 2025 19:17:33 GMT  
		Size: 15.2 KB (15248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c880f1959347bf8d734d197e7ad107423ee658e6ea88476169b7f1637ab9a87d`  
		Last Modified: Thu, 30 Oct 2025 19:17:34 GMT  
		Size: 2.8 MB (2778456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:95958f04037382bad3ba8afed7a949e3df702fade8ee7d5236305b551d77b182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3929073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86458b7b2512ceaf5d8b95b5176fe58d67e664f045322939763b2db01ad1d909`

```dockerfile
```

-	Layers:
	-	`sha256:85a1ff73f326bf256a33ec691e553ca1d051e81f8101e2a02a2ad8b43ac542c0`  
		Last Modified: Thu, 30 Oct 2025 21:20:56 GMT  
		Size: 3.9 MB (3888248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24ec22a4f05c3b8b0e8381444bd7d1122540442ea82064863511e925f84019d5`  
		Last Modified: Thu, 30 Oct 2025 21:20:57 GMT  
		Size: 40.8 KB (40825 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java11-openj9` - linux; arm64 variant v8

```console
$ docker pull websphere-liberty@sha256:fcf034ac0b55beb43e7159c7c94a340dc6617dccc7d5b8e2c6dac5d307a89658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.0 MB (118004670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a315bc5f37d3d9ce0169986448ce9e0de4f053c95ee029eca8ae1559140631f2`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

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
# Thu, 30 Oct 2025 18:55:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Oct 2025 18:55:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 18:55:10 GMT
ENV JAVA_VERSION=jdk-11.0.29+7_openj9-0.56.0
# Thu, 30 Oct 2025 18:55:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9fd5b1e5f18c80d945570cd86db46f737fdecbdcd8978d502c4a601f704c6676';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='16289eb013673a686abfef6631570e5b08c6171a1f7cf79fd495759d53393c38';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='474acb3b9c1ba608efe0c3aa0321a271cfbe2044e89d73e7129b0b013eb484df';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='42c7324f112975abc6a36c1cacad8f7515924cc60c21ac45e5985e7908d2c931';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Oct 2025 18:55:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Oct 2025 18:55:13 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Oct 2025 18:55:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba";     TOMCAT_VERSION="9.0.111";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 30 Oct 2025 20:03:56 GMT
USER root
# Thu, 30 Oct 2025 20:03:56 GMT
ARG VERBOSE=false
# Thu, 30 Oct 2025 20:03:56 GMT
ARG OPENJ9_SCC=true
# Thu, 30 Oct 2025 20:03:56 GMT
ARG LIBERTY_VERSION=25.0.0.10
# Thu, 30 Oct 2025 20:03:56 GMT
ARG LIBERTY_BUILD_LABEL=cl251020250923-1355
# Thu, 30 Oct 2025 20:03:56 GMT
ARG LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa
# Thu, 30 Oct 2025 20:03:56 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.10 org.opencontainers.image.revision=cl251020250923-1355 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.10 com.ibm.websphere.liberty.version=25.0.0.10
# Thu, 30 Oct 2025 20:03:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Thu, 30 Oct 2025 20:03:56 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.10 BuildLabel=cl251020250923-1355
# Thu, 30 Oct 2025 20:03:56 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Thu, 30 Oct 2025 20:03:56 GMT
ARG LIBERTY_URL
# Thu, 30 Oct 2025 20:03:56 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 30 Oct 2025 20:04:07 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 20:04:07 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 30 Oct 2025 20:04:07 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 30 Oct 2025 20:04:07 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Thu, 30 Oct 2025 20:04:08 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Thu, 30 Oct 2025 20:04:08 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Thu, 30 Oct 2025 20:04:08 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Thu, 30 Oct 2025 20:04:12 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Thu, 30 Oct 2025 20:04:12 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 30 Oct 2025 20:04:12 GMT
USER 1001
# Thu, 30 Oct 2025 20:04:12 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 30 Oct 2025 20:04:12 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 30 Oct 2025 20:04:12 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040f67fa4eec83079a9633f2a50173b1e0cc6661a6a0c66fe958356446d2f619`  
		Last Modified: Thu, 30 Oct 2025 18:56:06 GMT  
		Size: 12.1 MB (12129845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8d3614cb3b275944d132487f6a1f8496c160f1fb54db750ce208ff92079b28`  
		Last Modified: Thu, 30 Oct 2025 18:56:09 GMT  
		Size: 53.7 MB (53713602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39424a13d5cea5d6c2f00edc7a0068e27c337906865d2ad07030dec7a373a5d3`  
		Last Modified: Thu, 30 Oct 2025 18:56:06 GMT  
		Size: 4.2 MB (4215277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2da6bd568951704ca7ff005af34337b96dd185e1aa160e502d13dd0f89e0b5`  
		Last Modified: Thu, 30 Oct 2025 20:04:29 GMT  
		Size: 42.3 KB (42326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdf313d2f34f6c505684965a7dcc500565a07b7935d40504ab3637c877d4f3d`  
		Last Modified: Thu, 30 Oct 2025 20:04:29 GMT  
		Size: 17.7 MB (17668830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd84a4d8fb38e442fda1f0da78814c28d0d206c1f5cd1f8f11eacbbcfd26fd0d`  
		Last Modified: Thu, 30 Oct 2025 20:04:28 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7e7bae288ec79d6364b85e465520bf04ed90388d70c460de074fba0a0c751d`  
		Last Modified: Thu, 30 Oct 2025 20:04:29 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e31a3eff7011dac3816f8c9121be6232d10de0cc1c911104c512fa0bc4c74fb`  
		Last Modified: Thu, 30 Oct 2025 20:04:29 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3825f4e6eb502c4ab26e529a015c9d403ddf951d2339496acd735aaf938edcbe`  
		Last Modified: Thu, 30 Oct 2025 20:04:28 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec9f31169603218a5050172f3979836dde4399e635894d5b4e5fd86b8210088`  
		Last Modified: Thu, 30 Oct 2025 20:04:29 GMT  
		Size: 15.3 KB (15264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77b06c5bff9710f73b2df28a44ac52b456b9fed4cc4f325e335c0390f770883`  
		Last Modified: Thu, 30 Oct 2025 20:04:29 GMT  
		Size: 2.8 MB (2819783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:e05000ee671e2d478c5e907f74b93661cd977b2df6002edbf86abcfea57f2f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3927584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ded5f775c65aafff894ce16b8227b8caabfb41364c6c6a6b2b9c35c4a5751ca`

```dockerfile
```

-	Layers:
	-	`sha256:ce03213e5a82aa76c4d0ce2405524782b4dd0f90fec1caaae28e4e91eda5df99`  
		Last Modified: Thu, 30 Oct 2025 21:23:34 GMT  
		Size: 3.9 MB (3886620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c043ee10b14e1e7f987b5be2e8baaeba00ad719c8f9e1169325e9649b39ecb9`  
		Last Modified: Thu, 30 Oct 2025 21:23:35 GMT  
		Size: 41.0 KB (40964 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java11-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:dd0e2bd1303bd4ba607d49b20036d515c113fc46a8604de2c264261ec9f2ab67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128576382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dcb78a69b4217a8fa992fc2129ed20b430a03419e1ca41e978b84aded747471`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

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
ENV JAVA_VERSION=jdk-11.0.29+7_openj9-0.56.0
# Thu, 30 Oct 2025 19:02:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9fd5b1e5f18c80d945570cd86db46f737fdecbdcd8978d502c4a601f704c6676';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='16289eb013673a686abfef6631570e5b08c6171a1f7cf79fd495759d53393c38';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='474acb3b9c1ba608efe0c3aa0321a271cfbe2044e89d73e7129b0b013eb484df';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='42c7324f112975abc6a36c1cacad8f7515924cc60c21ac45e5985e7908d2c931';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Oct 2025 19:02:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Oct 2025 19:02:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Oct 2025 19:02:39 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba";     TOMCAT_VERSION="9.0.111";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 30 Oct 2025 20:09:19 GMT
USER root
# Thu, 30 Oct 2025 20:09:19 GMT
ARG VERBOSE=false
# Thu, 30 Oct 2025 20:09:19 GMT
ARG OPENJ9_SCC=true
# Thu, 30 Oct 2025 20:09:19 GMT
ARG LIBERTY_VERSION=25.0.0.10
# Thu, 30 Oct 2025 20:09:19 GMT
ARG LIBERTY_BUILD_LABEL=cl251020250923-1355
# Thu, 30 Oct 2025 20:09:19 GMT
ARG LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa
# Thu, 30 Oct 2025 20:09:19 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.10 org.opencontainers.image.revision=cl251020250923-1355 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.10 com.ibm.websphere.liberty.version=25.0.0.10
# Thu, 30 Oct 2025 20:09:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Thu, 30 Oct 2025 20:09:19 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.10 BuildLabel=cl251020250923-1355
# Thu, 30 Oct 2025 20:09:19 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Thu, 30 Oct 2025 20:09:19 GMT
ARG LIBERTY_URL
# Thu, 30 Oct 2025 20:09:19 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 30 Oct 2025 20:09:49 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 20:09:49 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 30 Oct 2025 20:09:50 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 30 Oct 2025 20:09:50 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Thu, 30 Oct 2025 20:09:51 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Thu, 30 Oct 2025 20:09:52 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Thu, 30 Oct 2025 20:09:53 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Thu, 30 Oct 2025 20:10:02 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Thu, 30 Oct 2025 20:10:02 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 30 Oct 2025 20:10:02 GMT
USER 1001
# Thu, 30 Oct 2025 20:10:02 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 30 Oct 2025 20:10:02 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 30 Oct 2025 20:10:02 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
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
	-	`sha256:a84d91243995e4da3caeea42a02c003c34e01fba10c017640845d5bc43efa1f4`  
		Last Modified: Thu, 30 Oct 2025 21:16:41 GMT  
		Size: 57.3 MB (57283294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afafd816ee78735ecf393921e856df65b71512fb406db56048f2910a0348614f`  
		Last Modified: Thu, 30 Oct 2025 19:50:34 GMT  
		Size: 3.5 MB (3489405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4155a96a25905358730fe0cb380d8aec6c3dc9ae8a979d93f2c03a7b589a0b`  
		Last Modified: Thu, 30 Oct 2025 20:10:27 GMT  
		Size: 36.5 KB (36499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa992e835ee8989342c793fb36ebc30e5bd607087e5474c590634158e6a9867`  
		Last Modified: Thu, 30 Oct 2025 20:10:29 GMT  
		Size: 17.7 MB (17668870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89d80d43d61e9079687192f6740e869ee39b30bf52e75038b48ce2703e79889`  
		Last Modified: Thu, 30 Oct 2025 20:10:27 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9faab77f63531420040304489c0afdc38b072fdeee99ebf1cd2647fffecd08`  
		Last Modified: Thu, 30 Oct 2025 20:10:27 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8eeb515491ae821f3454d42bbe0bba516d3aebf60e48d5054c3e2cea4eeeb0`  
		Last Modified: Thu, 30 Oct 2025 20:10:27 GMT  
		Size: 14.4 KB (14387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd38126ecd5ce149b7a4ba49dc2f9aa4aabb32bd64f3a95b8c0eee1398ee28eb`  
		Last Modified: Thu, 30 Oct 2025 20:10:27 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a748e419f9f988c5d45515a9cfa83f8d44879a533a880d7d69e00751fc5af26a`  
		Last Modified: Thu, 30 Oct 2025 20:10:27 GMT  
		Size: 15.3 KB (15271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63def942231c338368a837546eabbdac0bf12643275fff433528681e26d38afb`  
		Last Modified: Thu, 30 Oct 2025 20:10:28 GMT  
		Size: 2.7 MB (2725849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:ed34dc03c9f8f43f8ac3ded3b7a762efbd5184739b8b17e276acb3a2a1d4604e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3933739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6078a936e75e9aa85e836da0c0ffb02552c569fba82dbd4824de5397f500b9f7`

```dockerfile
```

-	Layers:
	-	`sha256:01cdc04081b8557874fdf0424328fc2757793bc0b360ad07f3f64874df8c660a`  
		Last Modified: Thu, 30 Oct 2025 21:23:40 GMT  
		Size: 3.9 MB (3892875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74c9ee05e9e12ba850d17b23f10a0bac9d0ed22ff714690ad78a081a241c9808`  
		Last Modified: Thu, 30 Oct 2025 21:23:41 GMT  
		Size: 40.9 KB (40864 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java11-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:047e090c19ff076908a04a51e61b12413b24516579ee93b29cb9ae482243272c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.9 MB (119877473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5660893e23d21f7b5374a5d3a1df787397db512d97e3a8cde308c80fb74fb497`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

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
ENV JAVA_VERSION=jdk-11.0.29+7_openj9-0.56.0
# Thu, 30 Oct 2025 19:05:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9fd5b1e5f18c80d945570cd86db46f737fdecbdcd8978d502c4a601f704c6676';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='16289eb013673a686abfef6631570e5b08c6171a1f7cf79fd495759d53393c38';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='474acb3b9c1ba608efe0c3aa0321a271cfbe2044e89d73e7129b0b013eb484df';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='42c7324f112975abc6a36c1cacad8f7515924cc60c21ac45e5985e7908d2c931';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Oct 2025 19:05:04 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Oct 2025 19:05:04 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Oct 2025 19:05:39 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba";     TOMCAT_VERSION="9.0.111";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 30 Oct 2025 20:21:24 GMT
USER root
# Thu, 30 Oct 2025 20:21:24 GMT
ARG VERBOSE=false
# Thu, 30 Oct 2025 20:21:24 GMT
ARG OPENJ9_SCC=true
# Thu, 30 Oct 2025 20:21:24 GMT
ARG LIBERTY_VERSION=25.0.0.10
# Thu, 30 Oct 2025 20:21:24 GMT
ARG LIBERTY_BUILD_LABEL=cl251020250923-1355
# Thu, 30 Oct 2025 20:21:24 GMT
ARG LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa
# Thu, 30 Oct 2025 20:21:24 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.10 org.opencontainers.image.revision=cl251020250923-1355 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.10 com.ibm.websphere.liberty.version=25.0.0.10
# Thu, 30 Oct 2025 20:21:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Thu, 30 Oct 2025 20:21:24 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.10 BuildLabel=cl251020250923-1355
# Thu, 30 Oct 2025 20:21:24 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Thu, 30 Oct 2025 20:21:24 GMT
ARG LIBERTY_URL
# Thu, 30 Oct 2025 20:21:24 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 30 Oct 2025 20:21:31 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 20:21:31 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 30 Oct 2025 20:21:31 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 30 Oct 2025 20:21:31 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Thu, 30 Oct 2025 20:21:32 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Thu, 30 Oct 2025 20:21:33 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Thu, 30 Oct 2025 20:21:33 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Thu, 30 Oct 2025 20:21:43 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Thu, 30 Oct 2025 20:21:43 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 30 Oct 2025 20:21:43 GMT
USER 1001
# Thu, 30 Oct 2025 20:21:43 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 30 Oct 2025 20:21:43 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 30 Oct 2025 20:21:43 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
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
	-	`sha256:baf143b346acde13c74277f365d5da4888bb48d1c60bfa2e141fad8feab58c1e`  
		Last Modified: Thu, 30 Oct 2025 19:06:36 GMT  
		Size: 54.4 MB (54423360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd2b6ac9e379c7c1f18f3aeb5c880f8b300627339b391506ddad56a56aba178`  
		Last Modified: Thu, 30 Oct 2025 19:06:27 GMT  
		Size: 4.6 MB (4625483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e04bbc8aa263e4533d4ff3c397904810b1a5ebd0b2a82df447ad9277e5bd61`  
		Last Modified: Thu, 30 Oct 2025 20:22:06 GMT  
		Size: 33.1 KB (33112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d53fb691317c2de22fd51694ceee65de61b4f4063ef6dc94f1faecdfef5ba1a`  
		Last Modified: Thu, 30 Oct 2025 20:22:08 GMT  
		Size: 17.7 MB (17668573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661c93f70fbe41d4217a0a39357a2602319b99ebf22de2b3112d86b025b5f28b`  
		Last Modified: Thu, 30 Oct 2025 20:22:06 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52ff04f51df03b846c5c51957c6352d80f6eafcea84849c23a54fd39ae533d6`  
		Last Modified: Thu, 30 Oct 2025 20:22:06 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ce4308c7390eb075450d12a7c7bc3fe46bef93cf4ed3acab3cf2c27a2a1142`  
		Last Modified: Thu, 30 Oct 2025 20:22:06 GMT  
		Size: 14.4 KB (14389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a8f6374cd9c71fd9be70ef475e6dd8beb966178047c7b6ca46485b3cb402b0`  
		Last Modified: Thu, 30 Oct 2025 20:22:06 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ce341f450ec5fcae0089e90f4bdbd1e2f575b107a2c7a375df69a56660aa01`  
		Last Modified: Thu, 30 Oct 2025 20:22:06 GMT  
		Size: 15.3 KB (15264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e3a7e61577f280861b5c18b9065cfae102f175b5c876722e1ce23d692a964b`  
		Last Modified: Thu, 30 Oct 2025 20:22:06 GMT  
		Size: 2.9 MB (2871946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:ede5bf935ef03bcc69a588ad071af2b11dc3bfa2605a696ead7878d92623bf6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:403209698cf07df089b3154052e8a96c823d47a16be5c6f72f1e7190b3af0f4f`

```dockerfile
```

-	Layers:
	-	`sha256:b0f2e124fda2c64ddf9993f11f8039531ea4f0f82dca73aa64e4e4761da697ab`  
		Last Modified: Thu, 30 Oct 2025 21:23:46 GMT  
		Size: 3.9 MB (3889265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:282e0307465ffee9f9d084672d8fa42d7f0abe22e37ada1f7a18a16e98a3b616`  
		Last Modified: Thu, 30 Oct 2025 21:23:47 GMT  
		Size: 40.8 KB (40825 bytes)  
		MIME: application/vnd.in-toto+json
