## `websphere-liberty:kernel-java11-openj9`

```console
$ docker pull websphere-liberty@sha256:d4d48aeace7a941c409aee5e42c4762a65acc5cbbbbb1393b9490e9fdb53048b
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
$ docker pull websphere-liberty@sha256:2265f3c9143ce29872923c43724733c3866528c358be4da69aedc3a15153f826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118910398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1824d8d9c5d1b1de534f68a1f63a791affe6db9ba8968e3886a5045c466363`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

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
# Wed, 26 Feb 2025 14:51:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 26 Feb 2025 14:51:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ENV JAVA_VERSION=jdk-11.0.26+4_openj9-0.49.0
# Wed, 26 Feb 2025 14:51:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2425d0daa7c0ef6603910c1c51ed7f3d8dbeb4dff8e1542957771ac5045fc21e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_aarch64_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d013d38e03a3455c6867b10544dc30041bf7afdb595d60ee09af43d46cdb5720';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_ppc64le_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='08586859b8a53aa9d5424a38838e8332664622049c3c33b1b0e5ea88b56ce2d9';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_x64_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='84232088178d3886d2c6dff2621f60406390bc12c36752a3305799a87cefc255';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_s390x_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 14:51:59 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 26 Feb 2025 14:51:59 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
USER root
# Wed, 26 Feb 2025 14:51:59 GMT
ARG VERBOSE=false
# Wed, 26 Feb 2025 14:51:59 GMT
ARG OPENJ9_SCC=true
# Wed, 26 Feb 2025 14:51:59 GMT
ARG LIBERTY_VERSION=25.0.0.2
# Wed, 26 Feb 2025 14:51:59 GMT
ARG LIBERTY_BUILD_LABEL=cl250220250209-1902
# Wed, 26 Feb 2025 14:51:59 GMT
ARG LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef
# Wed, 26 Feb 2025 14:51:59 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.2 org.opencontainers.image.revision=cl250220250209-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.2 com.ibm.websphere.liberty.version=25.0.0.2
# Wed, 26 Feb 2025 14:51:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 26 Feb 2025 14:51:59 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.2 BuildLabel=cl250220250209-1902
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ARG LIBERTY_URL
# Wed, 26 Feb 2025 14:51:59 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 26 Feb 2025 14:51:59 GMT
USER 1001
# Wed, 26 Feb 2025 14:51:59 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 26 Feb 2025 14:51:59 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 26 Feb 2025 14:51:59 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4c9c0b51361b1eda41c01395310e238baf9800b1345686d550a69c94746465`  
		Last Modified: Mon, 24 Mar 2025 16:59:40 GMT  
		Size: 12.2 MB (12166941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17a8db65dfbbe61341fd826f92bd8ee0208baac02a83c286274303557793d57`  
		Last Modified: Mon, 24 Mar 2025 16:59:40 GMT  
		Size: 52.4 MB (52386330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a00f4e34f78e05f58ddce14e909ffc0d07b907df8f811e608b8d3a0fbdf3f2e`  
		Last Modified: Mon, 24 Mar 2025 16:59:40 GMT  
		Size: 4.4 MB (4445687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f93ff4d3ff5bcc3ec3d8a5366fad5b4e46fac3f40a9002fddbd902c9635547`  
		Last Modified: Mon, 24 Mar 2025 17:03:05 GMT  
		Size: 31.7 KB (31748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e04c378d45c09d045a004209609428c50dde70228306130fb68ac73d379198`  
		Last Modified: Mon, 24 Mar 2025 17:03:06 GMT  
		Size: 17.5 MB (17506701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79da5f5126622e721b736294a10613e7235c8522847bf0de96619b5abfc1706a`  
		Last Modified: Mon, 24 Mar 2025 17:03:06 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81a29a1e0b30fb7cfe2da961040a1981da8c7db03556147d09d51ddb5030312`  
		Last Modified: Mon, 24 Mar 2025 17:03:06 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd273e9960552840f4d8299bb1e2274e2b4452aa47e3cdc52cb628413e7cadd2`  
		Last Modified: Mon, 24 Mar 2025 17:03:06 GMT  
		Size: 11.9 KB (11946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a1f02d25fb761745dafa761f510492b6754f97f4bb93a9c0aa9b98e95d4a37`  
		Last Modified: Mon, 24 Mar 2025 17:03:07 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68aad552f5702de9d5e68ba91e0423d6e14e908ceeb97eced180554258643597`  
		Last Modified: Mon, 24 Mar 2025 17:03:07 GMT  
		Size: 12.8 KB (12751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b5a037ee1c6b8ad8d7a6acf6dcb0893701bb45f603eed76c4b801cbc912968`  
		Last Modified: Mon, 24 Mar 2025 17:03:08 GMT  
		Size: 2.8 MB (2810110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:02a2e848019634eea5003ba2500086b03c3512bf9ddb82059765e4be5247bbc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3776540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d66af2dc1b2dde942e5449f52a38edb85c2131f0ff92e693ab8c3f9cf87e616`

```dockerfile
```

-	Layers:
	-	`sha256:99ae4f00e94f7441b7a12937b03c924f3f1f22db7ead21af95ecb24b030a154a`  
		Last Modified: Mon, 24 Mar 2025 17:03:06 GMT  
		Size: 3.7 MB (3736411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79583716fb499d4cfb3499b3b0b5706389486d00437fbdd2976405945333aee2`  
		Last Modified: Mon, 24 Mar 2025 17:03:06 GMT  
		Size: 40.1 KB (40129 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java11-openj9` - linux; arm64 variant v8

```console
$ docker pull websphere-liberty@sha256:60bf0c75b13010ca897e5a20a2b4ae91d82ba78975b8d00f5dfdd64ddd7074e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.8 MB (112775072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc5ef367f9b29bf65f8ac1a2d58dd2329d84956352b53d7b76235804c200bf4`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Wed, 26 Feb 2025 14:51:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 26 Feb 2025 14:51:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ENV JAVA_VERSION=jdk-11.0.26+4_openj9-0.49.0
# Wed, 26 Feb 2025 14:51:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2425d0daa7c0ef6603910c1c51ed7f3d8dbeb4dff8e1542957771ac5045fc21e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_aarch64_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d013d38e03a3455c6867b10544dc30041bf7afdb595d60ee09af43d46cdb5720';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_ppc64le_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='08586859b8a53aa9d5424a38838e8332664622049c3c33b1b0e5ea88b56ce2d9';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_x64_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='84232088178d3886d2c6dff2621f60406390bc12c36752a3305799a87cefc255';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_s390x_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 14:51:59 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 26 Feb 2025 14:51:59 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
USER root
# Wed, 26 Feb 2025 14:51:59 GMT
ARG VERBOSE=false
# Wed, 26 Feb 2025 14:51:59 GMT
ARG OPENJ9_SCC=true
# Wed, 26 Feb 2025 14:51:59 GMT
ARG LIBERTY_VERSION=25.0.0.2
# Wed, 26 Feb 2025 14:51:59 GMT
ARG LIBERTY_BUILD_LABEL=cl250220250209-1902
# Wed, 26 Feb 2025 14:51:59 GMT
ARG LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef
# Wed, 26 Feb 2025 14:51:59 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.2 org.opencontainers.image.revision=cl250220250209-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.2 com.ibm.websphere.liberty.version=25.0.0.2
# Wed, 26 Feb 2025 14:51:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 26 Feb 2025 14:51:59 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.2 BuildLabel=cl250220250209-1902
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ARG LIBERTY_URL
# Wed, 26 Feb 2025 14:51:59 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 26 Feb 2025 14:51:59 GMT
USER 1001
# Wed, 26 Feb 2025 14:51:59 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 26 Feb 2025 14:51:59 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 26 Feb 2025 14:51:59 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e483842b440e4fd1b12a18bab983fb09c8751e230e70f7c022dae2765ea706a5`  
		Last Modified: Mon, 24 Mar 2025 17:01:02 GMT  
		Size: 12.1 MB (12123514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f488e4d6c249fc50f450e06c50e6923a7760d0a0890f1ac781790e18f0212148`  
		Last Modified: Mon, 24 Mar 2025 17:11:19 GMT  
		Size: 48.8 MB (48787333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0490e7f6c6ae4946697c02f93de89888b284463c979419ea71797b5a456550d7`  
		Last Modified: Mon, 24 Mar 2025 17:11:18 GMT  
		Size: 4.2 MB (4182680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1db964b77caccd0a946aabd17acc10feb016e52c97c9c488ac1326c6b9a03f`  
		Last Modified: Mon, 24 Mar 2025 18:30:35 GMT  
		Size: 42.3 KB (42325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35735027c099ba3975c0ae5a2fed65cb7b9317dc47a309d2e34e7de9c40715c8`  
		Last Modified: Mon, 24 Mar 2025 18:30:36 GMT  
		Size: 17.5 MB (17506803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff319c026b6db2abe4fcc3cf506ab9338370ee7a34b553693bf997efe724af9`  
		Last Modified: Mon, 24 Mar 2025 18:30:34 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b69a953b57f592fb9d6a74e74a1caf1d539674398d6f660871e348ae3d4352`  
		Last Modified: Mon, 24 Mar 2025 18:30:34 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166bbf47e155352f21d4b027752c852aaf83e2fa22872515ce59d3f7aed3ae46`  
		Last Modified: Mon, 24 Mar 2025 18:30:35 GMT  
		Size: 11.9 KB (11946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553a43a7a278815b6e23c8a67235cc5bdcc7bbefb1c580d1f99e00b89d622f5d`  
		Last Modified: Mon, 24 Mar 2025 18:30:36 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866f0feb9a3fc91142f250e33b1b2838867b509c2bafa5c53f8a97683405975e`  
		Last Modified: Mon, 24 Mar 2025 18:30:36 GMT  
		Size: 12.8 KB (12750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84fcf8ce2c0b657cab183875773754189c3abc05e5a38eb34c8732eeffe2ab9`  
		Last Modified: Mon, 24 Mar 2025 18:30:37 GMT  
		Size: 2.7 MB (2747293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:a3b62b29b78a4ce2ede76863067cdd73211a055a37c5a5d0911438ded31c9c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3770027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c280ca2ac419343aaebf5f04274aee83a283d4f4788465bc7dfa6eac81062e2e`

```dockerfile
```

-	Layers:
	-	`sha256:aa50c89f5c4cdd9d608a50ef07455308e47088c311bacdd7a8dad4d015a10b49`  
		Last Modified: Mon, 24 Mar 2025 18:30:35 GMT  
		Size: 3.7 MB (3729757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7c967496f6d5e8412965c90cebb33ce8566bd72bcfba2832bc4bb3ae48aaa40`  
		Last Modified: Mon, 24 Mar 2025 18:30:34 GMT  
		Size: 40.3 KB (40270 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java11-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:a36339c04123fbc3d7f5eafcbe5870d4efaf6cc14a7d27e8b7b04072a8ae6dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124656222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5687bc0fedbd5b6104d0ae92f98fb0e5cdd3ad3b93ae065baeb010379a65f2f5`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

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
# Wed, 26 Feb 2025 14:51:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 26 Feb 2025 14:51:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ENV JAVA_VERSION=jdk-11.0.26+4_openj9-0.49.0
# Wed, 26 Feb 2025 14:51:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2425d0daa7c0ef6603910c1c51ed7f3d8dbeb4dff8e1542957771ac5045fc21e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_aarch64_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d013d38e03a3455c6867b10544dc30041bf7afdb595d60ee09af43d46cdb5720';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_ppc64le_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='08586859b8a53aa9d5424a38838e8332664622049c3c33b1b0e5ea88b56ce2d9';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_x64_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='84232088178d3886d2c6dff2621f60406390bc12c36752a3305799a87cefc255';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_s390x_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 14:51:59 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 26 Feb 2025 14:51:59 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
USER root
# Wed, 26 Feb 2025 14:51:59 GMT
ARG VERBOSE=false
# Wed, 26 Feb 2025 14:51:59 GMT
ARG OPENJ9_SCC=true
# Wed, 26 Feb 2025 14:51:59 GMT
ARG LIBERTY_VERSION=25.0.0.2
# Wed, 26 Feb 2025 14:51:59 GMT
ARG LIBERTY_BUILD_LABEL=cl250220250209-1902
# Wed, 26 Feb 2025 14:51:59 GMT
ARG LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef
# Wed, 26 Feb 2025 14:51:59 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.2 org.opencontainers.image.revision=cl250220250209-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.2 com.ibm.websphere.liberty.version=25.0.0.2
# Wed, 26 Feb 2025 14:51:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 26 Feb 2025 14:51:59 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.2 BuildLabel=cl250220250209-1902
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ARG LIBERTY_URL
# Wed, 26 Feb 2025 14:51:59 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 26 Feb 2025 14:51:59 GMT
USER 1001
# Wed, 26 Feb 2025 14:51:59 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 26 Feb 2025 14:51:59 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 26 Feb 2025 14:51:59 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b6a047babce01d9fd1ecd13e06fdd1fa8246e4c28a36772988cb5a72c0401af`  
		Last Modified: Mon, 24 Mar 2025 17:02:21 GMT  
		Size: 12.9 MB (12886676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a805d9a753e7b0c206566ea7b0e5e37ae7caa5afa57f098034795404a612179b`  
		Last Modified: Mon, 24 Mar 2025 17:15:52 GMT  
		Size: 53.6 MB (53621041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1caa8f7f57a39d6abf489d3b014f6bb974c02c10da375c549867c2f0e2957f8`  
		Last Modified: Mon, 24 Mar 2025 17:15:50 GMT  
		Size: 3.4 MB (3407581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882770c50208f277cf61a0637c1d7033c03bef32df5f95fc7f476917d0917e33`  
		Last Modified: Mon, 24 Mar 2025 21:27:22 GMT  
		Size: 36.5 KB (36496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09812c2adc99e3e5d1397d00705b261e13d87955895b570f1783bc9321fdf296`  
		Last Modified: Mon, 24 Mar 2025 21:27:22 GMT  
		Size: 17.5 MB (17506925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4a78ada0dc98bda609f08338bcacb7155abc7417d90523df8dedf28777d3e0`  
		Last Modified: Mon, 24 Mar 2025 21:27:21 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a0dad44a431b288cea5402ff291508eb443b40816801707dc630f495f1f8b4`  
		Last Modified: Mon, 24 Mar 2025 21:27:21 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2ba126862e57463f5b6393d49177b5e719a15c9bee65067319b0a8e8e19847`  
		Last Modified: Mon, 24 Mar 2025 21:27:23 GMT  
		Size: 11.9 KB (11949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad735f136c3b1e061699cdb1a9afc39371ac97184a6e7d1ed972f25f79efde3`  
		Last Modified: Mon, 24 Mar 2025 21:27:23 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04e7e827ecad4f6721a5ed87c8ab9dc17824e8fddebab9ca577987711a575f6`  
		Last Modified: Mon, 24 Mar 2025 21:27:23 GMT  
		Size: 12.8 KB (12755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031f36d36ae6874e80f8b672b3dcafb8ebcbab9a1073e5734b2d65abcf359b04`  
		Last Modified: Mon, 24 Mar 2025 21:27:24 GMT  
		Size: 2.7 MB (2722617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:bc8f9f4ec632f50114bcbfe4234e6a5523905b06c3c2738e6b153a735f956abf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3778596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085a695f1ee5a4cdd18e3b7f664f0dac9c458a7269bb629c90b0167db7dcaf1c`

```dockerfile
```

-	Layers:
	-	`sha256:d7252733410ec996c8b4c323183f3123a771864eff8cec7ee6c22c332fbc8a15`  
		Last Modified: Mon, 24 Mar 2025 21:27:22 GMT  
		Size: 3.7 MB (3738426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:468075106be8728d03fde88f811553087b6f61431ab48cd039ae81664468012c`  
		Last Modified: Mon, 24 Mar 2025 21:27:21 GMT  
		Size: 40.2 KB (40170 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java11-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:906776532c40bb9db8d69faff861c7c0f7b11329fb9163093cadb26c71805208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.4 MB (116420363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a2d877d2f2d64e4919eb4a2e6f4d3ef87befa29feb46db537340640d9c7e91`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:03 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:03 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:05 GMT
ADD file:39a6583c8b71c00e0ea7562cadb2b343caf5c0c274178520c7476e53faed2e3e in / 
# Sun, 26 Jan 2025 05:32:05 GMT
CMD ["/bin/bash"]
# Wed, 26 Feb 2025 14:51:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 26 Feb 2025 14:51:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ENV JAVA_VERSION=jdk-11.0.26+4_openj9-0.49.0
# Wed, 26 Feb 2025 14:51:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2425d0daa7c0ef6603910c1c51ed7f3d8dbeb4dff8e1542957771ac5045fc21e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_aarch64_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d013d38e03a3455c6867b10544dc30041bf7afdb595d60ee09af43d46cdb5720';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_ppc64le_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='08586859b8a53aa9d5424a38838e8332664622049c3c33b1b0e5ea88b56ce2d9';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_x64_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='84232088178d3886d2c6dff2621f60406390bc12c36752a3305799a87cefc255';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_s390x_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 14:51:59 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 26 Feb 2025 14:51:59 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
USER root
# Wed, 26 Feb 2025 14:51:59 GMT
ARG VERBOSE=false
# Wed, 26 Feb 2025 14:51:59 GMT
ARG OPENJ9_SCC=true
# Wed, 26 Feb 2025 14:51:59 GMT
ARG LIBERTY_VERSION=25.0.0.2
# Wed, 26 Feb 2025 14:51:59 GMT
ARG LIBERTY_BUILD_LABEL=cl250220250209-1902
# Wed, 26 Feb 2025 14:51:59 GMT
ARG LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef
# Wed, 26 Feb 2025 14:51:59 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.2 org.opencontainers.image.revision=cl250220250209-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.2 com.ibm.websphere.liberty.version=25.0.0.2
# Wed, 26 Feb 2025 14:51:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 26 Feb 2025 14:51:59 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.2 BuildLabel=cl250220250209-1902
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ARG LIBERTY_URL
# Wed, 26 Feb 2025 14:51:59 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 26 Feb 2025 14:51:59 GMT
USER 1001
# Wed, 26 Feb 2025 14:51:59 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 26 Feb 2025 14:51:59 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 26 Feb 2025 14:51:59 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:7ed94a91c4e77c2e320a028b45fcefc9419c4df2b3d6494bf92ab5d08bba4d77`  
		Last Modified: Sun, 26 Jan 2025 07:02:32 GMT  
		Size: 28.0 MB (28000931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9a504edea95fbee01cd3ff3d84972a695acb9423b1d0fea8abc1fa3cac5e26`  
		Last Modified: Tue, 04 Feb 2025 08:13:22 GMT  
		Size: 12.2 MB (12212279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690e2211e5a3922edbe2fffc31a253d298413d68da672e1bec4a1cce512e9996`  
		Last Modified: Sat, 15 Feb 2025 08:15:23 GMT  
		Size: 50.9 MB (50913952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ebbfbaf0212d70feadcf2b61a903b83322f9513be8caeb105669891b96744b`  
		Last Modified: Mon, 24 Mar 2025 17:13:44 GMT  
		Size: 4.6 MB (4566946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a906161e727f0338611301cf79d8f6d8347ebf107b7bd3b991f241be577302b`  
		Last Modified: Mon, 24 Mar 2025 18:38:18 GMT  
		Size: 33.1 KB (33113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36ffcf4c0a09f15f733ba5fc146f4ca1de3ce6f198b6e0da6f0012be740a593`  
		Last Modified: Mon, 24 Mar 2025 18:38:18 GMT  
		Size: 17.9 MB (17909677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd28e8dce30d1fbadf1f3bc9c68a26614825b40f8e7b0d834c9024863709cff`  
		Last Modified: Mon, 24 Mar 2025 18:38:18 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a41db253557c39fc3ef00e416101014503d67e7eac657a80bf96699cce99aad`  
		Last Modified: Mon, 24 Mar 2025 18:38:18 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068c2e9d191e6ad062b69f064a5bc0a8d60f4eeada7cbb2169083c516030ccce`  
		Last Modified: Mon, 24 Mar 2025 18:38:19 GMT  
		Size: 11.9 KB (11946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac845a9b45c18d3fde742cf75a4cec5919311487ad80ec8128873d6eca38e8ae`  
		Last Modified: Mon, 24 Mar 2025 18:38:18 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a65a711e7f54423c5ff2970f68c3dd43ad8149d53b858cdb594e4a7b412a39`  
		Last Modified: Mon, 24 Mar 2025 18:38:19 GMT  
		Size: 12.8 KB (12758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dfc0fb187b7904b239e7677c2500bb5472dd435bc52cff8f44db853b089d13`  
		Last Modified: Mon, 24 Mar 2025 18:38:19 GMT  
		Size: 2.8 MB (2756513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:e6fa7d939b46d0c7092ef07766a000a549ffaeaa13ea0747a0a72fb71c95af5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3773476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2950759091de065b7f6eb2c1ec0541264dbcaa856da9b8db055f82164f172cb`

```dockerfile
```

-	Layers:
	-	`sha256:19d872d42d13b64e9d263720a22b2ea98c62a96ab339d176327c70045eec85c0`  
		Last Modified: Mon, 24 Mar 2025 18:38:18 GMT  
		Size: 3.7 MB (3733346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98447b1ab0c73f5b72dc85c60bd19059bee5a9992a4d9e0fe27252f210c6c205`  
		Last Modified: Mon, 24 Mar 2025 18:38:18 GMT  
		Size: 40.1 KB (40130 bytes)  
		MIME: application/vnd.in-toto+json
