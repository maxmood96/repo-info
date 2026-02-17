## `websphere-liberty:kernel-java17-openj9`

```console
$ docker pull websphere-liberty@sha256:9e857e1550b89f788e1cd8e76171da86c72c6624184181cd425cd527a5985a7f
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

### `websphere-liberty:kernel-java17-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:5779e7a4d1e2b8be5a8cd66c371743cd657894afa0034fd6462dff26a6f4ff33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132282410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fe56ca769a795d4f1d14730c3b151c5b5cd87aabcca0106a9c78ad50d85fa3b`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 20:07:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Feb 2026 20:07:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:07:32 GMT
ENV JAVA_VERSION=jdk-17.0.18+8_openj9-0.57.0
# Mon, 09 Feb 2026 20:07:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a01d4aec9c66e9f8cefd63564ee5be9d31df01b5bab8007ba7ed0410fa97a490';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.18%2B8_openj9-0.57.0/ibm-semeru-open-jre_aarch64_linux_17.0.18_8_openj9-0.57.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e62c6f38315bbabcfedc1c69ab4cf2f0619314cddeaffb517b593aae7141fd3d';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.18%2B8_openj9-0.57.0/ibm-semeru-open-jre_ppc64le_linux_17.0.18_8_openj9-0.57.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b6c43cc8b824d69338e15ea220f2ca5b94a04ae657c95ad4372560b4ba0163e7';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.18%2B8_openj9-0.57.0/ibm-semeru-open-jre_x64_linux_17.0.18_8_openj9-0.57.0.tar.gz';          ;;        s390x)          ESUM='fb4714fd7096537e366abcd2d817d3fbbf21f81458766cec9340302755a15107';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.18%2B8_openj9-0.57.0/ibm-semeru-open-jre_s390x_linux_17.0.18_8_openj9-0.57.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 09 Feb 2026 20:07:35 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 20:07:35 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 09 Feb 2026 20:08:38 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Mon, 09 Feb 2026 21:15:36 GMT
USER root
# Mon, 09 Feb 2026 21:15:36 GMT
ARG VERBOSE=false
# Mon, 09 Feb 2026 21:15:36 GMT
ARG OPENJ9_SCC=true
# Mon, 09 Feb 2026 21:15:36 GMT
ARG LIBERTY_VERSION=26.0.0.1
# Mon, 09 Feb 2026 21:15:36 GMT
ARG LIBERTY_BUILD_LABEL=cl260120260112-1902
# Mon, 09 Feb 2026 21:15:36 GMT
ARG LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8
# Mon, 09 Feb 2026 21:15:36 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.1 org.opencontainers.image.revision=cl260120260112-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.1 com.ibm.websphere.liberty.version=26.0.0.1
# Mon, 09 Feb 2026 21:15:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Mon, 09 Feb 2026 21:15:36 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.1 BuildLabel=cl260120260112-1902
# Mon, 09 Feb 2026 21:15:36 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Mon, 09 Feb 2026 21:15:36 GMT
ARG LIBERTY_URL
# Mon, 09 Feb 2026 21:15:36 GMT
ARG DOWNLOAD_OPTIONS=
# Mon, 09 Feb 2026 21:15:49 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 21:15:49 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Mon, 09 Feb 2026 21:15:49 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Mon, 09 Feb 2026 21:15:49 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Mon, 09 Feb 2026 21:15:49 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Mon, 09 Feb 2026 21:15:49 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Mon, 09 Feb 2026 21:15:49 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Mon, 09 Feb 2026 21:15:53 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Mon, 09 Feb 2026 21:15:53 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Mon, 09 Feb 2026 21:15:53 GMT
USER 1001
# Mon, 09 Feb 2026 21:15:53 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Mon, 09 Feb 2026 21:15:53 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Mon, 09 Feb 2026 21:15:53 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d5f7f9fd0f29884535e2497a1739ba6938d209f2d5c71af23f0100080d64d4`  
		Last Modified: Mon, 09 Feb 2026 20:08:51 GMT  
		Size: 21.3 MB (21297007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47fe24dd1332c96492402c5c5169bd58708ee94c0537c3fd7e3e247b075615d3`  
		Last Modified: Mon, 09 Feb 2026 20:08:52 GMT  
		Size: 55.4 MB (55427113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392be8e4b8dfc32f20238863314ab3f6bbd2082c364d1ea0a4ff660fab85aff1`  
		Last Modified: Mon, 09 Feb 2026 20:08:50 GMT  
		Size: 5.0 MB (4979226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d4da51fcce96d19d923b691ef796d7c7971637f675896df0376db082cc17fa`  
		Last Modified: Mon, 09 Feb 2026 21:16:01 GMT  
		Size: 31.7 KB (31749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a330c44a7488e0e494b24bbbc4c42917b6ff4c3d1eb6ce5500337cc683d1ba7`  
		Last Modified: Mon, 09 Feb 2026 21:16:02 GMT  
		Size: 18.0 MB (18043377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e1db1b2bc2ae37de40005269e9149ffaf8aa9ee86fb4e3d2729ea244ad0b60`  
		Last Modified: Mon, 09 Feb 2026 21:16:01 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bec499ab26a6496c77d74c5f7a8fb5c33beae2ceb232d04ea0a98ed6e812d0c`  
		Last Modified: Mon, 09 Feb 2026 21:16:01 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a51b3fe6ad0c2cb2ca39df1a63511a735c7d48b2b3e5fdad7a17d05c504e6b3`  
		Last Modified: Mon, 09 Feb 2026 21:16:02 GMT  
		Size: 14.1 KB (14117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8d0b7e6881b6e340420bd023a7d292d1fa49b01720c878712d2cc704d27a6f`  
		Last Modified: Mon, 09 Feb 2026 21:16:02 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747f3c324244c704b6a0ac42d8bd68b9e39c13339e06164b10e142a8fbfe2483`  
		Last Modified: Mon, 09 Feb 2026 21:16:02 GMT  
		Size: 15.0 KB (14979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7507c7d3027237542414bd200707569c08cb9b2693585013c88d06aa9d929668`  
		Last Modified: Mon, 09 Feb 2026 21:16:03 GMT  
		Size: 2.7 MB (2746586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:c4df71e39a3c5dfa1e9548393b79bae1bf49ed8343e8a5e98602ac2a90ca9bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3357279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc51d9bb7a58c861d772cb1081fc7519578ab04f537e8b95011797d480490470`

```dockerfile
```

-	Layers:
	-	`sha256:93d6a853c92eff116bbe1f27b412362d499778cfe171860a39dfe88e1046197f`  
		Last Modified: Mon, 09 Feb 2026 21:16:01 GMT  
		Size: 3.3 MB (3316454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcd8a1a6fc21941780544f14a6335ae431f425f060c3bac407b5927c8047efbc`  
		Last Modified: Mon, 09 Feb 2026 21:16:01 GMT  
		Size: 40.8 KB (40825 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java17-openj9` - linux; arm64 variant v8

```console
$ docker pull websphere-liberty@sha256:295b0d2acd84338bd4d08ea00423fe2bdfe5034511b5ee79882cf50d63aaa332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129131540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a12ffcf61d0da84a99606f475c17c0c8be70a2be1cb4bc3029504249d0b1b6`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 20:07:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Feb 2026 20:07:56 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:07:56 GMT
ENV JAVA_VERSION=jdk-17.0.18+8_openj9-0.57.0
# Mon, 09 Feb 2026 20:07:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a01d4aec9c66e9f8cefd63564ee5be9d31df01b5bab8007ba7ed0410fa97a490';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.18%2B8_openj9-0.57.0/ibm-semeru-open-jre_aarch64_linux_17.0.18_8_openj9-0.57.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e62c6f38315bbabcfedc1c69ab4cf2f0619314cddeaffb517b593aae7141fd3d';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.18%2B8_openj9-0.57.0/ibm-semeru-open-jre_ppc64le_linux_17.0.18_8_openj9-0.57.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b6c43cc8b824d69338e15ea220f2ca5b94a04ae657c95ad4372560b4ba0163e7';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.18%2B8_openj9-0.57.0/ibm-semeru-open-jre_x64_linux_17.0.18_8_openj9-0.57.0.tar.gz';          ;;        s390x)          ESUM='fb4714fd7096537e366abcd2d817d3fbbf21f81458766cec9340302755a15107';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.18%2B8_openj9-0.57.0/ibm-semeru-open-jre_s390x_linux_17.0.18_8_openj9-0.57.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 09 Feb 2026 20:07:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 20:07:58 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 09 Feb 2026 20:09:01 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Mon, 09 Feb 2026 21:15:13 GMT
USER root
# Mon, 09 Feb 2026 21:15:13 GMT
ARG VERBOSE=false
# Mon, 09 Feb 2026 21:15:13 GMT
ARG OPENJ9_SCC=true
# Mon, 09 Feb 2026 21:15:13 GMT
ARG LIBERTY_VERSION=26.0.0.1
# Mon, 09 Feb 2026 21:15:13 GMT
ARG LIBERTY_BUILD_LABEL=cl260120260112-1902
# Mon, 09 Feb 2026 21:15:13 GMT
ARG LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8
# Mon, 09 Feb 2026 21:15:13 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.1 org.opencontainers.image.revision=cl260120260112-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.1 com.ibm.websphere.liberty.version=26.0.0.1
# Mon, 09 Feb 2026 21:15:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Mon, 09 Feb 2026 21:15:13 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.1 BuildLabel=cl260120260112-1902
# Mon, 09 Feb 2026 21:15:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Mon, 09 Feb 2026 21:15:13 GMT
ARG LIBERTY_URL
# Mon, 09 Feb 2026 21:15:13 GMT
ARG DOWNLOAD_OPTIONS=
# Mon, 09 Feb 2026 21:15:24 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 21:15:24 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Mon, 09 Feb 2026 21:15:24 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Mon, 09 Feb 2026 21:15:24 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Mon, 09 Feb 2026 21:15:24 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Mon, 09 Feb 2026 21:15:24 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Mon, 09 Feb 2026 21:15:24 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Mon, 09 Feb 2026 21:15:28 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Mon, 09 Feb 2026 21:15:28 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Mon, 09 Feb 2026 21:15:28 GMT
USER 1001
# Mon, 09 Feb 2026 21:15:28 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Mon, 09 Feb 2026 21:15:28 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Mon, 09 Feb 2026 21:15:28 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533076f5780fba4211c7ce5b61de50010f832dec993c48cf589679b31fcc082d`  
		Last Modified: Mon, 09 Feb 2026 20:09:15 GMT  
		Size: 20.9 MB (20913380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283ee5e47da3f706a370483cf99726e9fa179af754084c4b198d73805ad8dfa8`  
		Last Modified: Mon, 09 Feb 2026 20:09:15 GMT  
		Size: 53.7 MB (53700518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a9abe22e2c226e298f71c6a583a8dfc28e5bb57b57e0ff75b5857bd15a6309`  
		Last Modified: Mon, 09 Feb 2026 20:09:14 GMT  
		Size: 4.7 MB (4716840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b928a7edd8bbc7fb22c9e89626758bb1d4f42a8bb59d3117ab4f7ee6c10731`  
		Last Modified: Mon, 09 Feb 2026 21:15:37 GMT  
		Size: 42.3 KB (42321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbe349192263f0295c1e780b98528cb9d32bd18976aeb19cc133d4c036eeefc`  
		Last Modified: Mon, 09 Feb 2026 21:15:37 GMT  
		Size: 18.0 MB (18043425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad8e0e8cc223fe231bddeb55a94e6f6974cee66dc42160b898231d4fff098b7`  
		Last Modified: Mon, 09 Feb 2026 21:15:37 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56de88c76461c4319edac036608f6cfd56772d29ef3eb625bff46c21207d6c58`  
		Last Modified: Mon, 09 Feb 2026 21:15:37 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8fda1450af86257f86805ded47eaf24125f2fe0929f331d4b30ea889f44490`  
		Last Modified: Mon, 09 Feb 2026 21:15:38 GMT  
		Size: 14.1 KB (14116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d1637c900f8b42d5665e632770bdf932f7b29db548de31e643ab3c57e19dff`  
		Last Modified: Mon, 09 Feb 2026 21:15:38 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9139c826ed380686335cdc351d24657700bc955c05e92cf02c8332d22779345`  
		Last Modified: Mon, 09 Feb 2026 21:15:38 GMT  
		Size: 15.0 KB (14977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb14541201c4dd95be3d5078a95b04b65b477e7e8e06a84bda7d548abf5efb0`  
		Last Modified: Mon, 09 Feb 2026 21:15:39 GMT  
		Size: 2.8 MB (2819892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:07459d6d6949da8a99401cc4566efc52736141b021cbf8c72db221c33876f0b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3355962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c794059659e5131b178c6913d2e3a7dcc567500dd103a928c009764f64c3bb`

```dockerfile
```

-	Layers:
	-	`sha256:479afbe811ac0497ba9c5c15dd8501e40534cfab408b3648469dfa992686d68b`  
		Last Modified: Mon, 09 Feb 2026 21:15:37 GMT  
		Size: 3.3 MB (3314996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34e6fcd6e33bb431f5abb60287a0a1e917549d51b614b01b413d15ffc64be64a`  
		Last Modified: Mon, 09 Feb 2026 21:15:36 GMT  
		Size: 41.0 KB (40966 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java17-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:bca46906cb502e029461183ffb32b259fc30a284c1b1f3d0fda0ef5b2d1ce5e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139596187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4964b9771147ae70eb88da371f291fe9635031df8ca9f1382b3ee9c72ed46176`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 20:34:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Feb 2026 20:34:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:34:09 GMT
ENV JAVA_VERSION=jdk-17.0.18+8_openj9-0.57.0
# Mon, 09 Feb 2026 22:50:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a01d4aec9c66e9f8cefd63564ee5be9d31df01b5bab8007ba7ed0410fa97a490';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.18%2B8_openj9-0.57.0/ibm-semeru-open-jre_aarch64_linux_17.0.18_8_openj9-0.57.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e62c6f38315bbabcfedc1c69ab4cf2f0619314cddeaffb517b593aae7141fd3d';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.18%2B8_openj9-0.57.0/ibm-semeru-open-jre_ppc64le_linux_17.0.18_8_openj9-0.57.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b6c43cc8b824d69338e15ea220f2ca5b94a04ae657c95ad4372560b4ba0163e7';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.18%2B8_openj9-0.57.0/ibm-semeru-open-jre_x64_linux_17.0.18_8_openj9-0.57.0.tar.gz';          ;;        s390x)          ESUM='fb4714fd7096537e366abcd2d817d3fbbf21f81458766cec9340302755a15107';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.18%2B8_openj9-0.57.0/ibm-semeru-open-jre_s390x_linux_17.0.18_8_openj9-0.57.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 09 Feb 2026 22:50:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 22:50:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 09 Feb 2026 22:51:40 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Mon, 09 Feb 2026 23:13:44 GMT
USER root
# Mon, 09 Feb 2026 23:13:44 GMT
ARG VERBOSE=false
# Mon, 09 Feb 2026 23:13:44 GMT
ARG OPENJ9_SCC=true
# Mon, 09 Feb 2026 23:13:44 GMT
ARG LIBERTY_VERSION=26.0.0.1
# Mon, 09 Feb 2026 23:13:44 GMT
ARG LIBERTY_BUILD_LABEL=cl260120260112-1902
# Mon, 09 Feb 2026 23:13:44 GMT
ARG LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8
# Mon, 09 Feb 2026 23:13:44 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.1 org.opencontainers.image.revision=cl260120260112-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.1 com.ibm.websphere.liberty.version=26.0.0.1
# Mon, 09 Feb 2026 23:13:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Mon, 09 Feb 2026 23:13:44 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.1 BuildLabel=cl260120260112-1902
# Mon, 09 Feb 2026 23:13:44 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Mon, 09 Feb 2026 23:13:44 GMT
ARG LIBERTY_URL
# Mon, 09 Feb 2026 23:13:44 GMT
ARG DOWNLOAD_OPTIONS=
# Mon, 09 Feb 2026 23:13:57 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 23:13:57 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Mon, 09 Feb 2026 23:13:58 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Mon, 09 Feb 2026 23:13:58 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Mon, 09 Feb 2026 23:13:59 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Mon, 09 Feb 2026 23:13:59 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Mon, 09 Feb 2026 23:14:00 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Mon, 09 Feb 2026 23:14:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Mon, 09 Feb 2026 23:14:11 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Mon, 09 Feb 2026 23:14:11 GMT
USER 1001
# Mon, 09 Feb 2026 23:14:11 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Mon, 09 Feb 2026 23:14:11 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Mon, 09 Feb 2026 23:14:11 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca127b638f72ed7f9e1f454f0122c3723c277c84c84220dabb2fe7b41220d548`  
		Last Modified: Mon, 09 Feb 2026 20:36:03 GMT  
		Size: 23.3 MB (23280007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b286d86079789cbd7b2077cb2bd38a53df0843cdd80499b9d59386baf9f1af44`  
		Last Modified: Mon, 09 Feb 2026 22:52:18 GMT  
		Size: 57.3 MB (57292163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fb4addc715fb68e273e6f2e4af211123f8708007bdfb83f183c436cf380c05`  
		Last Modified: Mon, 09 Feb 2026 22:52:16 GMT  
		Size: 3.9 MB (3878256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052a3d81cb82930ddb9f4ee39d746b7611822a0dd17f4d956ae2eef2078515ea`  
		Last Modified: Mon, 09 Feb 2026 23:14:34 GMT  
		Size: 36.5 KB (36498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280f7ca7aeff617851fdb9d539a57278e093ad418054ffd60cfc4dfb1a6d2e45`  
		Last Modified: Mon, 09 Feb 2026 23:14:35 GMT  
		Size: 18.0 MB (18043756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4133ace60f04cfad344efdf79a4060b78af8c65029b1d1266ce7f91fabd5155f`  
		Last Modified: Mon, 09 Feb 2026 23:14:34 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95151a9b5c29054d154e79e37d4ec1a0b16e8c42e36301d86298ebf64b059cfb`  
		Last Modified: Mon, 09 Feb 2026 23:14:34 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f915ff3527b02ddd52657f758af148ce9c7609cbb656ee1e784d32a7fdea618`  
		Last Modified: Mon, 09 Feb 2026 23:14:35 GMT  
		Size: 14.1 KB (14118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ab33ff241bf2d0f4950b6a9c08be385cd8df2f594b2148b336141f9463a59f`  
		Last Modified: Mon, 09 Feb 2026 23:14:35 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210476f1aaa4967cd29bdeaac001ba5851d4e40d802301960eadb0b77a286619`  
		Last Modified: Mon, 09 Feb 2026 23:14:35 GMT  
		Size: 15.0 KB (14988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d621749bae6ad3a82327d87895c5acd840b09c5e7be2b9de9380f444cd15b5`  
		Last Modified: Mon, 09 Feb 2026 23:14:36 GMT  
		Size: 2.7 MB (2727996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:aef0f9138bb625eff7d6ef8e50ee1ad8171f4696908797f56c3fa73105acb4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3361948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b6bd860a47af53c4f9cfd0d7af609ec5ac04a02bceca65f49bca89dd30833a`

```dockerfile
```

-	Layers:
	-	`sha256:85ecf1ed2d5652fee620778263d09444686e67c6d52869ad9376d03ca1968cab`  
		Last Modified: Mon, 09 Feb 2026 23:14:34 GMT  
		Size: 3.3 MB (3321082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:596373c9f59ab613c3e0afca22f8c8ee3dfaf1575ee8e5c3df2d3042891ed2bf`  
		Last Modified: Mon, 09 Feb 2026 23:14:34 GMT  
		Size: 40.9 KB (40866 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java17-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:8fe09c1475ef9a2fb8f8ecc63553ad77ae8307e3baa3e70061f54ee11cdcbb12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123477132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d950c6af691f71e9de7fa37083291509277ef1a14cf8958bf37adb32bb1caa0`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:51 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:51 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:52 GMT
ADD file:be1799101a7a15f881e3aebea1e86fa6a156760dc7688b1affe179e948814a3b in / 
# Tue, 10 Feb 2026 16:50:52 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:17:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:17:22 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:17:22 GMT
ENV JAVA_VERSION=jdk-17.0.18+8_openj9-0.57.0
# Tue, 17 Feb 2026 20:40:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a01d4aec9c66e9f8cefd63564ee5be9d31df01b5bab8007ba7ed0410fa97a490';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.18%2B8_openj9-0.57.0/ibm-semeru-open-jre_aarch64_linux_17.0.18_8_openj9-0.57.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e62c6f38315bbabcfedc1c69ab4cf2f0619314cddeaffb517b593aae7141fd3d';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.18%2B8_openj9-0.57.0/ibm-semeru-open-jre_ppc64le_linux_17.0.18_8_openj9-0.57.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b6c43cc8b824d69338e15ea220f2ca5b94a04ae657c95ad4372560b4ba0163e7';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.18%2B8_openj9-0.57.0/ibm-semeru-open-jre_x64_linux_17.0.18_8_openj9-0.57.0.tar.gz';          ;;        s390x)          ESUM='fb4714fd7096537e366abcd2d817d3fbbf21f81458766cec9340302755a15107';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.18%2B8_openj9-0.57.0/ibm-semeru-open-jre_s390x_linux_17.0.18_8_openj9-0.57.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Feb 2026 20:40:07 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:40:07 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Feb 2026 20:41:18 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 17 Feb 2026 21:53:44 GMT
USER root
# Tue, 17 Feb 2026 21:53:44 GMT
ARG VERBOSE=false
# Tue, 17 Feb 2026 21:53:44 GMT
ARG OPENJ9_SCC=true
# Tue, 17 Feb 2026 21:53:44 GMT
ARG LIBERTY_VERSION=26.0.0.1
# Tue, 17 Feb 2026 21:53:44 GMT
ARG LIBERTY_BUILD_LABEL=cl260120260112-1902
# Tue, 17 Feb 2026 21:53:44 GMT
ARG LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8
# Tue, 17 Feb 2026 21:53:44 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.1 org.opencontainers.image.revision=cl260120260112-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.1 com.ibm.websphere.liberty.version=26.0.0.1
# Tue, 17 Feb 2026 21:53:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Tue, 17 Feb 2026 21:53:44 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.1 BuildLabel=cl260120260112-1902
# Tue, 17 Feb 2026 21:53:44 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 17 Feb 2026 21:53:44 GMT
ARG LIBERTY_URL
# Tue, 17 Feb 2026 21:53:44 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 17 Feb 2026 21:54:01 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:54:01 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 17 Feb 2026 21:54:02 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 17 Feb 2026 21:54:04 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 17 Feb 2026 21:54:04 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 17 Feb 2026 21:54:05 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 17 Feb 2026 21:54:07 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Tue, 17 Feb 2026 21:54:14 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 17 Feb 2026 21:54:14 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 17 Feb 2026 21:54:14 GMT
USER 1001
# Tue, 17 Feb 2026 21:54:14 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 17 Feb 2026 21:54:14 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 17 Feb 2026 21:54:14 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:8b6ba492713239cba0554ce53d24405e1285684fa64bcfb05df4af8037ba5836`  
		Last Modified: Tue, 10 Feb 2026 17:42:12 GMT  
		Size: 29.9 MB (29909784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2ce3b2a70015000a5b0ceaa4885f1aceec67cb23d3ef542311e0f5506c39b0`  
		Last Modified: Tue, 17 Feb 2026 20:19:02 GMT  
		Size: 13.1 MB (13118433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a126ffcb9b8a68f40af722d4890772c7757035bb9b385f2b9267477328e0ca4d`  
		Last Modified: Tue, 17 Feb 2026 20:41:48 GMT  
		Size: 54.3 MB (54312562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbb2daf00932057db75fddac5172011fc3a3c91e2ec551d3d5421f11059b3db`  
		Last Modified: Tue, 17 Feb 2026 20:41:47 GMT  
		Size: 5.1 MB (5127220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225e45987abd75ba56625236c579f4f6db78dbed0dba66d354a2a0fcf174342a`  
		Last Modified: Tue, 17 Feb 2026 21:54:30 GMT  
		Size: 33.1 KB (33111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7cb3e9fd080cc703f188a5d94d6db678e1e15f57d18f8023c14dc4ce1f197b`  
		Last Modified: Tue, 17 Feb 2026 21:54:31 GMT  
		Size: 18.0 MB (18042869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6333ae6ab977b41d8718b51a7fc6e480dd9be8bc5268136c738ac76f83b737`  
		Last Modified: Tue, 17 Feb 2026 21:54:30 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09496c3874c62e92bf507cad6a6968f14b8d34c88a483ad794fa153296fe79e`  
		Last Modified: Tue, 17 Feb 2026 21:54:30 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48091bf38829812e6b7623eb6ba49df3e422f36ee187fc57b86325eb9e7706a3`  
		Last Modified: Tue, 17 Feb 2026 21:54:31 GMT  
		Size: 14.1 KB (14118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49067b6f2b1e544e89649467865f24dfcdcb80476d73dfe824700e19a2f9e9c0`  
		Last Modified: Tue, 17 Feb 2026 21:54:31 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046fb4ff207d03f04e5a9df43807c214f3c72ad522a8caa99eb4aca3537cbbd0`  
		Last Modified: Tue, 17 Feb 2026 21:54:31 GMT  
		Size: 15.0 KB (14996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ac00f1cd8f57d94ce95bc07fb4eb80ddd99a3eb9f450ec4e9e9dbdb65a1625`  
		Last Modified: Tue, 17 Feb 2026 21:54:32 GMT  
		Size: 2.9 MB (2901790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:c03061783d2ad3b057ebee35d6a347f6995b7080348718d1cdb11ea77e355d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3358277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e5df3e5517e5d4e8b569e3e7dbf51651c5b9ac03b2ca8da43dfd4967b487bf8`

```dockerfile
```

-	Layers:
	-	`sha256:7aea64f620ddae19b73426e243bc450844a27c82cce518f6a3e4884bba911644`  
		Last Modified: Tue, 17 Feb 2026 21:54:31 GMT  
		Size: 3.3 MB (3317451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df4040d57fc443c804465051933ebaac72c459894b8b41336ad774d77a8418b7`  
		Last Modified: Tue, 17 Feb 2026 21:54:30 GMT  
		Size: 40.8 KB (40826 bytes)  
		MIME: application/vnd.in-toto+json
