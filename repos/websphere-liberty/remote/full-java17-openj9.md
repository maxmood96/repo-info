## `websphere-liberty:full-java17-openj9`

```console
$ docker pull websphere-liberty@sha256:e8c24a8bac16bbbbb56f23e8fc9a764588cd5737ef40e1bff2a78203884b8e14
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

### `websphere-liberty:full-java17-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:890ac20dc0941ecf9a96330be44f242d648ef2509ae8c7b6eb7ac3cec155174b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.0 MB (491976411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0cd52ead339ff5d9d0fa9ae9640ae2ce01208ea0dd8d2ff1855883b2f7ab01`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

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
# Thu, 19 Sep 2024 17:39:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Sep 2024 17:39:31 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_VERSION=jdk-17.0.12+7_openj9-0.46.1
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cb2bfe44358158dcaa903e1f9aeb3e895adc1d5ace1f764e0dc1b1aeb4ffb77e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_aarch64_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='29f969c56c1e82587e0fcb1c0253dec413538c9599eaec9fcdb3983d181aad96';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_ppc64le_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='f218a8e1596197a3e89e9eff3ef4dc3e56ff41d7e293261e02cbc589a418998e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_x64_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='1490c54b365dc1c4bfea47412433df79ebfd2c3f85c9f7b1c88ce2d7ae7dee75';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_s390x_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.95/bin/apache-tomcat-9.0.95.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
USER root
# Tue, 08 Oct 2024 20:01:46 GMT
ARG VERBOSE=false
# Tue, 08 Oct 2024 20:01:46 GMT
ARG OPENJ9_SCC=true
# Tue, 08 Oct 2024 20:01:46 GMT
ARG LIBERTY_VERSION=24.0.0.10
# Tue, 08 Oct 2024 20:01:46 GMT
ARG LIBERTY_BUILD_LABEL=cl241020240923-1638
# Tue, 08 Oct 2024 20:01:46 GMT
ARG LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf
# Tue, 08 Oct 2024 20:01:46 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.10 org.opencontainers.image.revision=cl241020240923-1638 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Tue, 08 Oct 2024 20:01:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Tue, 08 Oct 2024 20:01:46 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.10 BuildLabel=cl241020240923-1638
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
ARG LIBERTY_URL
# Tue, 08 Oct 2024 20:01:46 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 08 Oct 2024 20:01:46 GMT
USER 1001
# Tue, 08 Oct 2024 20:01:46 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 08 Oct 2024 20:01:46 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 08 Oct 2024 20:01:46 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 08 Oct 2024 20:01:46 GMT
ARG VERBOSE=false
# Tue, 08 Oct 2024 20:01:46 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2164747e1ff2ca7eac681bf32f49a500610ebae6a7ec62604a1f098051d7b765`  
		Last Modified: Thu, 19 Sep 2024 20:01:39 GMT  
		Size: 12.2 MB (12156493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb949f759267157c8c5b6da2affd1e2fbb45890cb425c73a09ff662b46558b1e`  
		Last Modified: Thu, 19 Sep 2024 20:01:39 GMT  
		Size: 51.5 MB (51534126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a965409154c3ffae601b19ee5aaead25c0246b90b6f423b74baa889aaf1ef80d`  
		Last Modified: Thu, 19 Sep 2024 20:01:39 GMT  
		Size: 4.9 MB (4898019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c8f4581818eb7de718e49a828c3e47c4c9e0ff3309f3b26d29cc81777eba65`  
		Last Modified: Wed, 09 Oct 2024 00:04:46 GMT  
		Size: 31.8 KB (31750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3b2fcf66352d6ff3e2d56cf300beb9aed5b6d69fe04c19c0768c2dd5f5ae32`  
		Last Modified: Wed, 09 Oct 2024 00:04:47 GMT  
		Size: 17.4 MB (17431564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d90f66012a06d511f86f24e96516ad22a9690d4a0bdd289db0ae306abb6deb`  
		Last Modified: Wed, 09 Oct 2024 00:04:46 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32af4e18afafe598d837536bb4b8f5d6a877c2e0088a6341436beb8c8e781ae`  
		Last Modified: Wed, 09 Oct 2024 00:04:46 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4522d1660cc421d0e54afb7e406bef60620bb40e42083799fa7100e396d37e06`  
		Last Modified: Wed, 09 Oct 2024 00:04:47 GMT  
		Size: 11.8 KB (11830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a66fb9672c82f11edd8239a9ab87af1fdd58e57406698a2ea1acf6d61881ed`  
		Last Modified: Wed, 09 Oct 2024 00:04:47 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e91c32fd40349f208808955ce4c70f2035f470a80f7d60022f7abdc803b0cb`  
		Last Modified: Wed, 09 Oct 2024 00:04:47 GMT  
		Size: 12.6 KB (12631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6be04f2c6a04b110552bd87c5278a526047abaf109b1523541ed625fead829`  
		Last Modified: Wed, 09 Oct 2024 00:04:48 GMT  
		Size: 2.8 MB (2834470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f459c20abb806d1edb60b8f7605944f5ef2d85153e85cb6f71185734adf905`  
		Last Modified: Wed, 09 Oct 2024 01:07:26 GMT  
		Size: 357.4 MB (357435391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca88029d581dea003abe60463f5094028e7f93ecb92fa2f944dc40608762e0`  
		Last Modified: Wed, 09 Oct 2024 01:07:17 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a70445ec7bde8752d0b5a854536bf86affa3a72d27a5ba303444f886cc2a7e`  
		Last Modified: Wed, 09 Oct 2024 01:07:18 GMT  
		Size: 16.1 MB (16091266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:2307a272f73fe6c5b25c8645c8195493ae6b8c4a7c3f7ac004c17e6e51cae6bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5660992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4b90ba832f69b65003dc46f26279a3f86e147c8dd5343065fd5161eee80d8c`

```dockerfile
```

-	Layers:
	-	`sha256:af34ad638899674df49ef9d2c0c4baa111c7bcd6a2c68f1b229ccf5e68f967ee`  
		Last Modified: Wed, 09 Oct 2024 01:07:17 GMT  
		Size: 5.6 MB (5641413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c008074af45629ce460d66078773598901540447520e8d74b9b02b3046349d7c`  
		Last Modified: Wed, 09 Oct 2024 01:07:17 GMT  
		Size: 19.6 KB (19579 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java17-openj9` - linux; arm64 variant v8

```console
$ docker pull websphere-liberty@sha256:c48e4100dbb33477eab1ed664f1784179044236e087cb5dda9d08b886b790845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.8 MB (484809096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7a3ef1e7acfa62ba727e1e007e06347072490c45561ce15cb2d5a01b4a59e46`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

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
# Thu, 19 Sep 2024 17:39:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Sep 2024 17:39:31 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_VERSION=jdk-17.0.12+7_openj9-0.46.1
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cb2bfe44358158dcaa903e1f9aeb3e895adc1d5ace1f764e0dc1b1aeb4ffb77e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_aarch64_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='29f969c56c1e82587e0fcb1c0253dec413538c9599eaec9fcdb3983d181aad96';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_ppc64le_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='f218a8e1596197a3e89e9eff3ef4dc3e56ff41d7e293261e02cbc589a418998e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_x64_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='1490c54b365dc1c4bfea47412433df79ebfd2c3f85c9f7b1c88ce2d7ae7dee75';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_s390x_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.95/bin/apache-tomcat-9.0.95.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
USER root
# Tue, 08 Oct 2024 20:01:46 GMT
ARG VERBOSE=false
# Tue, 08 Oct 2024 20:01:46 GMT
ARG OPENJ9_SCC=true
# Tue, 08 Oct 2024 20:01:46 GMT
ARG LIBERTY_VERSION=24.0.0.10
# Tue, 08 Oct 2024 20:01:46 GMT
ARG LIBERTY_BUILD_LABEL=cl241020240923-1638
# Tue, 08 Oct 2024 20:01:46 GMT
ARG LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf
# Tue, 08 Oct 2024 20:01:46 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.10 org.opencontainers.image.revision=cl241020240923-1638 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Tue, 08 Oct 2024 20:01:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Tue, 08 Oct 2024 20:01:46 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.10 BuildLabel=cl241020240923-1638
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
ARG LIBERTY_URL
# Tue, 08 Oct 2024 20:01:46 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 08 Oct 2024 20:01:46 GMT
USER 1001
# Tue, 08 Oct 2024 20:01:46 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 08 Oct 2024 20:01:46 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 08 Oct 2024 20:01:46 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 08 Oct 2024 20:01:46 GMT
ARG VERBOSE=false
# Tue, 08 Oct 2024 20:01:46 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3831940244be8baa42f9d6629360ed0326dedeb7d18134cfa77184874d97bf6f`  
		Last Modified: Tue, 17 Sep 2024 02:06:03 GMT  
		Size: 12.1 MB (12114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20642fa5f40650d3b2d9c9ff8d86ea87930c0b986bfbbd31aa92bf919ad6154d`  
		Last Modified: Tue, 17 Sep 2024 02:11:45 GMT  
		Size: 47.9 MB (47916904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc107faa922311b6d5ade0aa99f19705957ab2a4030ddfc64d3951188f41172`  
		Last Modified: Thu, 19 Sep 2024 20:11:28 GMT  
		Size: 4.7 MB (4663030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d666bacec61e57936283765bc0084c2cb47d932893715523cf8b6e0c735c6049`  
		Last Modified: Wed, 09 Oct 2024 00:29:48 GMT  
		Size: 42.3 KB (42326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5c56e37c63fb8708fa41e321651c6a6a70a69607a32fb3f1d1b9c29effbe51`  
		Last Modified: Wed, 09 Oct 2024 00:29:48 GMT  
		Size: 17.4 MB (17431904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af78619809019354e8a44bb2eaa68629ffedf1d2c697e35034ed07fa9b1d8b03`  
		Last Modified: Wed, 09 Oct 2024 00:29:47 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d7b9cd2a52c7d850958e0a5cb44a85527f665866aee7c70976d7122657c2f2`  
		Last Modified: Wed, 09 Oct 2024 00:29:47 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98dda09837cd0b4ff0dabc005cda062c8b126f9b1172fed948ab6f7ee4548462`  
		Last Modified: Wed, 09 Oct 2024 00:29:48 GMT  
		Size: 11.8 KB (11826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcaeb9a35b85274931c157e9157de5915138c8a064c13fd50faddc9b5abd1547`  
		Last Modified: Wed, 09 Oct 2024 00:29:48 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c6b5d8044a39840cceb438cd633e8484428493fad1bc26db632e2f32d0c58c`  
		Last Modified: Wed, 09 Oct 2024 00:29:49 GMT  
		Size: 12.6 KB (12634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450a2d3dfb6542c3094d689606e994840ee9610f7a1bb33c5296fdf56997972b`  
		Last Modified: Wed, 09 Oct 2024 00:29:50 GMT  
		Size: 2.7 MB (2737490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0d38b380b821ace83948aa3321c1bb8f2b9cc62465e0481d14ff8923532b08`  
		Last Modified: Wed, 09 Oct 2024 01:22:29 GMT  
		Size: 357.4 MB (357435918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9363ca10333879d79fafb1332cb82195abd609fcc647c53622dc4711743db5d3`  
		Last Modified: Wed, 09 Oct 2024 01:22:21 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0b33d4e297601a8378440a9002d898cb2022e108b69bf097f4aa8c15000e32`  
		Last Modified: Wed, 09 Oct 2024 01:22:22 GMT  
		Size: 15.1 MB (15081239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:dfaaafb029a27b6e4041752032798a056b32ffc7a86315817ee006ff24b1e2c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5654397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dfa94ffd08625cc2666295faf35ea10a4b7b71fc55c98f974b3c391e5abbc66`

```dockerfile
```

-	Layers:
	-	`sha256:ea13d89d87ac4ecb2eb3264356e072696c10761099f12ab54d99a4639a88a890`  
		Last Modified: Wed, 09 Oct 2024 01:22:21 GMT  
		Size: 5.6 MB (5634735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:059fd6b65ca9f68f00b6e7de5f1dc526ddf78fb6a113c55cdfd7b2ba832090ed`  
		Last Modified: Wed, 09 Oct 2024 01:22:20 GMT  
		Size: 19.7 KB (19662 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java17-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:fd93373c54004462527c9a661d86c599fb9f32c82efbf9b7f0ebc4f79263e511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.5 MB (495453048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e5aa341a3efdbc7fd97cbb6508d2a5c03968280687d997367f36b7484127c7`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

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
# Thu, 19 Sep 2024 17:39:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Sep 2024 17:39:31 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_VERSION=jdk-17.0.12+7_openj9-0.46.1
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cb2bfe44358158dcaa903e1f9aeb3e895adc1d5ace1f764e0dc1b1aeb4ffb77e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_aarch64_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='29f969c56c1e82587e0fcb1c0253dec413538c9599eaec9fcdb3983d181aad96';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_ppc64le_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='f218a8e1596197a3e89e9eff3ef4dc3e56ff41d7e293261e02cbc589a418998e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_x64_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='1490c54b365dc1c4bfea47412433df79ebfd2c3f85c9f7b1c88ce2d7ae7dee75';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_s390x_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.95/bin/apache-tomcat-9.0.95.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
USER root
# Tue, 08 Oct 2024 20:01:46 GMT
ARG VERBOSE=false
# Tue, 08 Oct 2024 20:01:46 GMT
ARG OPENJ9_SCC=true
# Tue, 08 Oct 2024 20:01:46 GMT
ARG LIBERTY_VERSION=24.0.0.10
# Tue, 08 Oct 2024 20:01:46 GMT
ARG LIBERTY_BUILD_LABEL=cl241020240923-1638
# Tue, 08 Oct 2024 20:01:46 GMT
ARG LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf
# Tue, 08 Oct 2024 20:01:46 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.10 org.opencontainers.image.revision=cl241020240923-1638 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Tue, 08 Oct 2024 20:01:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Tue, 08 Oct 2024 20:01:46 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.10 BuildLabel=cl241020240923-1638
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
ARG LIBERTY_URL
# Tue, 08 Oct 2024 20:01:46 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 08 Oct 2024 20:01:46 GMT
USER 1001
# Tue, 08 Oct 2024 20:01:46 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 08 Oct 2024 20:01:46 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 08 Oct 2024 20:01:46 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 08 Oct 2024 20:01:46 GMT
ARG VERBOSE=false
# Tue, 08 Oct 2024 20:01:46 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
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
	-	`sha256:3e956f85db15bc3def81b35a583203cdacb3b7c13fc265dacab2f17dd60df77d`  
		Last Modified: Tue, 17 Sep 2024 01:23:56 GMT  
		Size: 53.1 MB (53116177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac51ff44c02229b95f1ef5c650d3318da0b21b6208e7f83628d3926229ff6b9`  
		Last Modified: Thu, 19 Sep 2024 20:15:51 GMT  
		Size: 3.8 MB (3782496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188f621976a1165e0aa191d641278b06e431a1e29ab3d52cb69da54c5aa5e774`  
		Last Modified: Wed, 09 Oct 2024 00:40:46 GMT  
		Size: 36.5 KB (36499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57126a2f2fca6603b081a3361b37db2fa3a4562ea061d693676dd75b0e6aee93`  
		Last Modified: Wed, 09 Oct 2024 00:40:47 GMT  
		Size: 17.4 MB (17432154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3259ed12e5e0caf60809e4789f82e44a964949c4185b198d8f78c90b3e1b08`  
		Last Modified: Wed, 09 Oct 2024 00:40:46 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea89b2dfd46421af755b2a4030b01ac103fd6e0d8c7f2e6b1e02a828828b0d58`  
		Last Modified: Wed, 09 Oct 2024 00:40:46 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bba28303551d0c8476369a829fa2a66a8b93cc2cf0f8324c76afb282844108a`  
		Last Modified: Wed, 09 Oct 2024 00:40:47 GMT  
		Size: 11.8 KB (11829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d0a0edee966dc16ca18bede454d69d4de1ec0c93bede60188740b04da4ec1f`  
		Last Modified: Wed, 09 Oct 2024 00:40:47 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8e68db369e9e47a0cd905ac1c00b38effa6cd5f2588f979de445260f465521`  
		Last Modified: Wed, 09 Oct 2024 00:40:47 GMT  
		Size: 12.6 KB (12648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd867ada65116b9e79fae91d9f7eebb59dc5a2b76898b044654ca102ba573eb`  
		Last Modified: Wed, 09 Oct 2024 00:40:48 GMT  
		Size: 2.7 MB (2666926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437cd7278fffbcd9b7bbde01f8a29db35a5e175aa951e3d762f7b391cd6148f3`  
		Last Modified: Wed, 09 Oct 2024 01:53:49 GMT  
		Size: 357.4 MB (357436181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc484236f6321b621ebb75935ce6034386a21dab21192cbfe93d1dd8c913669`  
		Last Modified: Wed, 09 Oct 2024 01:53:30 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04328e4372c7042f416efcec5e1efec6ea141c8b1f97e72bed690f35e975041d`  
		Last Modified: Wed, 09 Oct 2024 01:53:33 GMT  
		Size: 13.6 MB (13618564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:f7b62f15f43855c8e6a8950dcd5fb6cfae23337d38268ad84cd459303c5a6386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5665502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e535ca25629a25f10f74e9da6e9f835ac47fe8a4b839d5e61ee91efbc8df2832`

```dockerfile
```

-	Layers:
	-	`sha256:43dc58a53a60adc25e34f035738cffb541ba65babc2e6a3ed8021d68f49c2235`  
		Last Modified: Wed, 09 Oct 2024 01:53:29 GMT  
		Size: 5.6 MB (5645895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adee3942cfda83f55e10dd98397dc58919d2e42e94c3a1e0dc08f3916b3e64cd`  
		Last Modified: Wed, 09 Oct 2024 01:53:29 GMT  
		Size: 19.6 KB (19607 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java17-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:3ccece2f868bf2189c2b3cac4699810a07dc244d1400f75e39899ed25f9cdb37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.5 MB (489485891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb1fbd220c677ceffae1b5dedcfd2effbf4be308eef43ec25a4522119940fba`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

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
# Thu, 19 Sep 2024 17:39:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Sep 2024 17:39:31 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_VERSION=jdk-17.0.12+7_openj9-0.46.1
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cb2bfe44358158dcaa903e1f9aeb3e895adc1d5ace1f764e0dc1b1aeb4ffb77e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_aarch64_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='29f969c56c1e82587e0fcb1c0253dec413538c9599eaec9fcdb3983d181aad96';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_ppc64le_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='f218a8e1596197a3e89e9eff3ef4dc3e56ff41d7e293261e02cbc589a418998e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_x64_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='1490c54b365dc1c4bfea47412433df79ebfd2c3f85c9f7b1c88ce2d7ae7dee75';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_s390x_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.95/bin/apache-tomcat-9.0.95.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
USER root
# Tue, 08 Oct 2024 20:01:46 GMT
ARG VERBOSE=false
# Tue, 08 Oct 2024 20:01:46 GMT
ARG OPENJ9_SCC=true
# Tue, 08 Oct 2024 20:01:46 GMT
ARG LIBERTY_VERSION=24.0.0.10
# Tue, 08 Oct 2024 20:01:46 GMT
ARG LIBERTY_BUILD_LABEL=cl241020240923-1638
# Tue, 08 Oct 2024 20:01:46 GMT
ARG LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf
# Tue, 08 Oct 2024 20:01:46 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.10 org.opencontainers.image.revision=cl241020240923-1638 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Tue, 08 Oct 2024 20:01:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Tue, 08 Oct 2024 20:01:46 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.10 BuildLabel=cl241020240923-1638
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
ARG LIBERTY_URL
# Tue, 08 Oct 2024 20:01:46 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 08 Oct 2024 20:01:46 GMT
USER 1001
# Tue, 08 Oct 2024 20:01:46 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 08 Oct 2024 20:01:46 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 08 Oct 2024 20:01:46 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 08 Oct 2024 20:01:46 GMT
ARG VERBOSE=false
# Tue, 08 Oct 2024 20:01:46 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
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
	-	`sha256:bf306d6b55fcd4409a3d7914177a321a344e69fa7c2a2b6fcbfa5871e82a7fab`  
		Last Modified: Tue, 17 Sep 2024 02:04:33 GMT  
		Size: 50.5 MB (50470509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b37cc8f8b8f9d1c5741bfa4a1e93d8c6659c980ab4c801503926c834f02cb30`  
		Last Modified: Thu, 19 Sep 2024 20:15:44 GMT  
		Size: 5.0 MB (5033582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853abeb5b541742e78b7be413a78e4802def5284a6f3dcb4920e8685047852af`  
		Last Modified: Wed, 09 Oct 2024 00:33:05 GMT  
		Size: 33.1 KB (33112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4526a29d36f2bb680df827bf112b7cded74abc94e164033e2757b352409ddea3`  
		Last Modified: Wed, 09 Oct 2024 00:33:05 GMT  
		Size: 17.4 MB (17431814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc252f4c017e925575e5bd467f56702c2ef6c3f885c4abda24d3ca158e44f6d2`  
		Last Modified: Wed, 09 Oct 2024 00:33:05 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bbdfab7bed30d961b29832bf1fde0c3a2a160325efe4bca542d44166b071b4e`  
		Last Modified: Wed, 09 Oct 2024 00:33:05 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add8cbb971e95beab90f363b74e0ecc22cb67b508b84422acefab93137cd548`  
		Last Modified: Wed, 09 Oct 2024 00:33:05 GMT  
		Size: 11.8 KB (11830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943624c7baabcd7c36ba0e44a5e2fec79704558f2da61f9dcff91dedf5064a5b`  
		Last Modified: Wed, 09 Oct 2024 00:33:06 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4ef0446b0709de9fc873d3847f19ed88825d825fbf61a06bb7d51391532c51`  
		Last Modified: Wed, 09 Oct 2024 00:33:06 GMT  
		Size: 12.6 KB (12632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccaa329205c5e01245f4d4f0038af4ef786e59030f5eca92028d881ce5b4dc5a`  
		Last Modified: Wed, 09 Oct 2024 00:33:06 GMT  
		Size: 2.8 MB (2820927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08044e4a6a2b71b6201f9c4ffaf102ba995a372f9dac8c1a3b85cdd2ea9d0eb7`  
		Last Modified: Wed, 09 Oct 2024 01:36:06 GMT  
		Size: 357.4 MB (357435397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4e25b0b5b913f06172ce66a1dee4776f224848e0d5ca5fc75c24c613c6bd6e`  
		Last Modified: Wed, 09 Oct 2024 01:36:00 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6bdc1ea793cd303ecf2cebe70865a7747b1140e5119aecb0c09d17631731be9`  
		Last Modified: Wed, 09 Oct 2024 01:36:02 GMT  
		Size: 16.0 MB (16027663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:d63e383ebd7b2c740252094f4e7d148b1edb38bfcf32eb8ce5617f18a8fda243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5662128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8103eba9a9485b9bbf37c52e4780ee40d84f1603ef41d11ae256a274a019be31`

```dockerfile
```

-	Layers:
	-	`sha256:e27faadd657f55f2c7ebf0fc0766d0ecc54082dd67337decc8cc1edd93620a6b`  
		Last Modified: Wed, 09 Oct 2024 01:36:00 GMT  
		Size: 5.6 MB (5642549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e09c2eabac9fd3b64f146565417a43b320ed84c01678fc8a7826838ebba92450`  
		Last Modified: Wed, 09 Oct 2024 01:36:00 GMT  
		Size: 19.6 KB (19579 bytes)  
		MIME: application/vnd.in-toto+json
