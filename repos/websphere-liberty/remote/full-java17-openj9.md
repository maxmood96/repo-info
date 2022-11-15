## `websphere-liberty:full-java17-openj9`

```console
$ docker pull websphere-liberty@sha256:e4c6f3a7e8d8b1e9237d995ef62d10711242c590f30532d0cbbe9fd2d2ee2d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:full-java17-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:73462d1b56d6641ed7316bf5158c06a1a6c5705b49387e75ec4c99cc8fa2841a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.7 MB (452663897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afab278bd04d5e8fc632f3a9773c90ad4af991d24d20d6670405d5e206ba4f2`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 16:36:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Oct 2022 16:36:44 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Nov 2022 20:33:10 GMT
ENV JAVA_VERSION=jdk-17.0.5+8_openj9-0.35.0
# Thu, 10 Nov 2022 20:35:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8f934ce1745f52a067bdeb56b3b9e9192f51e674ff2956a1e53b33e44ea5ca42';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.5%2B8_openj9-0.35.0/ibm-semeru-open-jre_aarch64_linux_17.0.5_8_openj9-0.35.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d54972fb938f655a3665512c7181c2c5813e3bfe742650d6081e2f480388ef2f';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.5%2B8_openj9-0.35.0/ibm-semeru-open-jre_ppc64le_linux_17.0.5_8_openj9-0.35.0.tar.gz';          ;;        amd64|x86_64)          ESUM='759f9c507e0faf53b260ee9f492bab8fdeb8091bdecad904134861714e4d913b';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.5%2B8_openj9-0.35.0/ibm-semeru-open-jre_x64_linux_17.0.5_8_openj9-0.35.0.tar.gz';          ;;        s390x)          ESUM='64ffeaff0ea4915fb66d3356ef5de65e884172b031e0c268bdeb4d2aa6be1c91';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.5%2B8_openj9-0.35.0/ibm-semeru-open-jre_s390x_linux_17.0.5_8_openj9-0.35.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 10 Nov 2022 20:35:51 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Nov 2022 20:35:51 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 10 Nov 2022 20:36:26 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 10 Nov 2022 23:51:19 GMT
ARG VERBOSE=false
# Thu, 10 Nov 2022 23:51:19 GMT
ARG OPENJ9_SCC=true
# Tue, 15 Nov 2022 03:24:24 GMT
ARG EN_SHA=1ce31500fa2422ed1410137cd50d33e18cf42ad0ae0b5a3e545183ae801869e0
# Tue, 15 Nov 2022 03:24:24 GMT
ARG NON_IBM_SHA=1f032aeb46b5f5f4262f123cb2339230e2755cac039cb1bf0285cbb0f37fe7c8
# Tue, 15 Nov 2022 03:24:24 GMT
ARG NOTICES_SHA=46056efcb4c0e11e1cc9a33104c4d2ae9b42d566ec74885804914c4eb41ef2ec
# Tue, 15 Nov 2022 03:24:24 GMT
LABEL org.opencontainers.image.authors=Chris Potter, Christy Jesuraj, Melissa Lee org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=22.0.0.11 org.opencontainers.image.revision=cl221120221010-1540 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Tue, 15 Nov 2022 03:24:24 GMT
ENV LIBERTY_VERSION=22.0.0_11
# Tue, 15 Nov 2022 03:24:24 GMT
ARG LIBERTY_URL
# Tue, 15 Nov 2022 03:24:24 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 15 Nov 2022 03:24:37 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ce31500fa2422ed1410137cd50d33e18cf42ad0ae0b5a3e545183ae801869e0 NON_IBM_SHA=1f032aeb46b5f5f4262f123cb2339230e2755cac039cb1bf0285cbb0f37fe7c8 NOTICES_SHA=46056efcb4c0e11e1cc9a33104c4d2ae9b42d566ec74885804914c4eb41ef2ec OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 03:24:37 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 03:24:37 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=22.0.0.11 BuildLabel=cl221120221010-1540
# Tue, 15 Nov 2022 03:24:37 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 15 Nov 2022 03:24:38 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ce31500fa2422ed1410137cd50d33e18cf42ad0ae0b5a3e545183ae801869e0 NON_IBM_SHA=1f032aeb46b5f5f4262f123cb2339230e2755cac039cb1bf0285cbb0f37fe7c8 NOTICES_SHA=46056efcb4c0e11e1cc9a33104c4d2ae9b42d566ec74885804914c4eb41ef2ec VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Tue, 15 Nov 2022 03:24:38 GMT
COPY dir:8bf844c49178cf63745af9ec643f57d70bd92c28166fabfad188dfc250d88353 in /opt/ibm/helpers/ 
# Tue, 15 Nov 2022 03:24:38 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Tue, 15 Nov 2022 03:24:39 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ce31500fa2422ed1410137cd50d33e18cf42ad0ae0b5a3e545183ae801869e0 NON_IBM_SHA=1f032aeb46b5f5f4262f123cb2339230e2755cac039cb1bf0285cbb0f37fe7c8 NOTICES_SHA=46056efcb4c0e11e1cc9a33104c4d2ae9b42d566ec74885804914c4eb41ef2ec VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Tue, 15 Nov 2022 03:24:47 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ce31500fa2422ed1410137cd50d33e18cf42ad0ae0b5a3e545183ae801869e0 NON_IBM_SHA=1f032aeb46b5f5f4262f123cb2339230e2755cac039cb1bf0285cbb0f37fe7c8 NOTICES_SHA=46056efcb4c0e11e1cc9a33104c4d2ae9b42d566ec74885804914c4eb41ef2ec VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Tue, 15 Nov 2022 03:24:47 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 15 Nov 2022 03:24:47 GMT
USER 1001
# Tue, 15 Nov 2022 03:24:47 GMT
EXPOSE 9080 9443
# Tue, 15 Nov 2022 03:24:47 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 15 Nov 2022 03:24:47 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 15 Nov 2022 03:42:39 GMT
ARG VERBOSE=false
# Tue, 15 Nov 2022 03:42:39 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 15 Nov 2022 03:50:54 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Tue, 15 Nov 2022 03:50:56 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Tue, 15 Nov 2022 03:51:25 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f522cdfc47f379d86205a33f1211b8a8e05351eda5dc9150b5b4b26f5954341`  
		Last Modified: Tue, 25 Oct 2022 16:53:10 GMT  
		Size: 16.0 MB (16014718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29cace1a6c51112ea82ccf6b273e650589760b3c349cb8dc1876b83e6f74451`  
		Last Modified: Thu, 10 Nov 2022 20:44:35 GMT  
		Size: 48.1 MB (48096890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b121c5a34aca8e21ed0b789b533284caef0b3514a4d1d7fe0d59fefe7bdbcc`  
		Last Modified: Thu, 10 Nov 2022 20:44:29 GMT  
		Size: 4.8 MB (4757424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a887f00ef23f600ca0f536347b3d931606883ba325666e21a23784fb2e2ac98e`  
		Last Modified: Tue, 15 Nov 2022 03:52:55 GMT  
		Size: 14.3 MB (14308408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4846660d43126d868ed04441f9f788fa5623a7ec88bace2a9e4f89e5b868343f`  
		Last Modified: Tue, 15 Nov 2022 03:52:52 GMT  
		Size: 678.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffd5cb1e649532736ffec4592482c1c9ed044b5f6f82c1193f8f53fa88fcc4e`  
		Last Modified: Tue, 15 Nov 2022 03:52:52 GMT  
		Size: 9.8 KB (9754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3299d257c57e2256eacabbdb0fbae32cc00774573ddef0cfc99141aec5045305`  
		Last Modified: Tue, 15 Nov 2022 03:52:52 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f649b80746dde685670094a7c53f523207dbe8f715053a6d93d2c3b1c6680b38`  
		Last Modified: Tue, 15 Nov 2022 03:52:52 GMT  
		Size: 10.7 KB (10732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74b98fa81855c21b58c3f9d9db233e88496e7276b8d6877679a2336104be3ec`  
		Last Modified: Tue, 15 Nov 2022 03:52:52 GMT  
		Size: 2.6 MB (2594022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3986a5600cc68904277d63b7f9a319def4b1185b939d9c711f85928d4d0e617f`  
		Last Modified: Tue, 15 Nov 2022 03:54:05 GMT  
		Size: 323.6 MB (323559601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e890aeeec361d62f55be7d056ecfc8929611b55050b310166bf322999a0895`  
		Last Modified: Tue, 15 Nov 2022 03:53:48 GMT  
		Size: 943.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8a176a7aa57820d8877402c360d782c111e3569e4a0975f1e54bd3b584f728`  
		Last Modified: Tue, 15 Nov 2022 03:53:50 GMT  
		Size: 14.7 MB (14732623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full-java17-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:13a93337631b3166debc17e78a986931128bef14ee3babaf115f02ae43506fef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.4 MB (414399785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717edfa800218879f73a9127017b342722e18353b890536148fa84c50028302f`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 05 Oct 2022 10:52:08 GMT
ADD file:75224b75d955b3021df8214497d6835e1aff42b5ce83f96b779b63c4a8e15faf in / 
# Wed, 05 Oct 2022 10:52:10 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 19:23:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 05 Oct 2022 19:23:42 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 19:28:13 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1_openj9-0.33.1
# Wed, 05 Oct 2022 19:29:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0114aada7edc773346a6729c992bdd2f5ff8aedec756547f42839bb37c12e3bf';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.4.1%2B1_openj9-0.33.1/ibm-semeru-open-jre_aarch64_linux_17.0.4.1_1_openj9-0.33.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='35955d6ce7b9e262abfd2b2dff585b3be71fa7e320ea23b5d604aa45fac2d251';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.4.1%2B1_openj9-0.33.1/ibm-semeru-open-jre_ppc64le_linux_17.0.4.1_1_openj9-0.33.1.tar.gz';          ;;        amd64|x86_64)          ESUM='338ea5fe72f5a1a075c02953882a985dee437f0b60e432eacb02ba8ca15b3e0b';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.4.1%2B1_openj9-0.33.1/ibm-semeru-open-jre_x64_linux_17.0.4.1_1_openj9-0.33.1.tar.gz';          ;;        s390x)          ESUM='cf8b58da8d98f0a01d228ed3fe7177ed6ba783b8134113073977cc3ebf9eec33';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.4.1%2B1_openj9-0.33.1/ibm-semeru-open-jre_s390x_linux_17.0.4.1_1_openj9-0.33.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 05 Oct 2022 19:29:40 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 19:29:40 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 05 Oct 2022 19:30:18 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 05 Oct 2022 22:36:47 GMT
ARG VERBOSE=false
# Wed, 05 Oct 2022 22:36:48 GMT
ARG OPENJ9_SCC=true
# Wed, 05 Oct 2022 22:36:48 GMT
ARG EN_SHA=44a2cb9704f0ed8e871e9d1a8faa55563d093d0c34af3c248492dd1790a794eb
# Wed, 05 Oct 2022 22:36:49 GMT
ARG NON_IBM_SHA=9e1ddbc876eb5fd3182799b2ccf6619f23acfe6d4b0b8ee82c72e3944ad15b34
# Wed, 05 Oct 2022 22:36:49 GMT
ARG NOTICES_SHA=1f852693234e6b9fabccb4218a21a88b485300dccd76ee089fb007aaf3180725
# Wed, 05 Oct 2022 22:36:50 GMT
LABEL org.opencontainers.image.authors=Chris Potter, Christy Jesuraj, Melissa Lee org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=22.0.0.10 org.opencontainers.image.revision=cl221020220912-1100 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 05 Oct 2022 22:36:50 GMT
ENV LIBERTY_VERSION=22.0.0_10
# Wed, 05 Oct 2022 22:36:50 GMT
ARG LIBERTY_URL
# Wed, 05 Oct 2022 22:36:51 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 05 Oct 2022 22:37:25 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=44a2cb9704f0ed8e871e9d1a8faa55563d093d0c34af3c248492dd1790a794eb NON_IBM_SHA=9e1ddbc876eb5fd3182799b2ccf6619f23acfe6d4b0b8ee82c72e3944ad15b34 NOTICES_SHA=1f852693234e6b9fabccb4218a21a88b485300dccd76ee089fb007aaf3180725 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 22:37:26 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 22:37:26 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=22.0.0.10 BuildLabel=cl221020220912-1100
# Wed, 05 Oct 2022 22:37:26 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 05 Oct 2022 22:37:28 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=44a2cb9704f0ed8e871e9d1a8faa55563d093d0c34af3c248492dd1790a794eb NON_IBM_SHA=9e1ddbc876eb5fd3182799b2ccf6619f23acfe6d4b0b8ee82c72e3944ad15b34 NOTICES_SHA=1f852693234e6b9fabccb4218a21a88b485300dccd76ee089fb007aaf3180725 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 05 Oct 2022 22:37:28 GMT
COPY dir:8bf844c49178cf63745af9ec643f57d70bd92c28166fabfad188dfc250d88353 in /opt/ibm/helpers/ 
# Wed, 05 Oct 2022 22:37:29 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 05 Oct 2022 22:37:30 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=44a2cb9704f0ed8e871e9d1a8faa55563d093d0c34af3c248492dd1790a794eb NON_IBM_SHA=9e1ddbc876eb5fd3182799b2ccf6619f23acfe6d4b0b8ee82c72e3944ad15b34 NOTICES_SHA=1f852693234e6b9fabccb4218a21a88b485300dccd76ee089fb007aaf3180725 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 05 Oct 2022 22:37:42 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=44a2cb9704f0ed8e871e9d1a8faa55563d093d0c34af3c248492dd1790a794eb NON_IBM_SHA=9e1ddbc876eb5fd3182799b2ccf6619f23acfe6d4b0b8ee82c72e3944ad15b34 NOTICES_SHA=1f852693234e6b9fabccb4218a21a88b485300dccd76ee089fb007aaf3180725 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 05 Oct 2022 22:37:43 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 05 Oct 2022 22:37:43 GMT
USER 1001
# Wed, 05 Oct 2022 22:37:43 GMT
EXPOSE 9080 9443
# Wed, 05 Oct 2022 22:37:44 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 05 Oct 2022 22:37:44 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 05 Oct 2022 23:07:23 GMT
ARG VERBOSE=false
# Wed, 05 Oct 2022 23:07:24 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 05 Oct 2022 23:21:22 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Wed, 05 Oct 2022 23:21:28 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 05 Oct 2022 23:22:13 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:ecaa0fe591301d50850e37b61a6fac5429c04a3c39272da2f7b748eaed7f5c52`  
		Last Modified: Wed, 05 Oct 2022 10:54:26 GMT  
		Size: 33.3 MB (33296076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6d370b8f9860863a3dd8ff29fa9838d9d89f67331ce806ddf2fc681d5891b3`  
		Last Modified: Wed, 05 Oct 2022 19:34:51 GMT  
		Size: 17.2 MB (17186880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4bfc27d301b9fe9eb741424f55ea17d149d7ea0b2afe6e18ff0cb637156c7a3`  
		Last Modified: Wed, 05 Oct 2022 19:37:40 GMT  
		Size: 49.0 MB (48957673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecc320bbb82d63287a0129d400853125dd74c43956e7a7fe0867212b16b8178`  
		Last Modified: Wed, 05 Oct 2022 19:37:30 GMT  
		Size: 3.7 MB (3744096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c99645626fc97fb0b228dbaeb1888426a3224636493c30a8d9b1866b56c7143`  
		Last Modified: Thu, 06 Oct 2022 01:01:10 GMT  
		Size: 14.3 MB (14277768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b768edb400177cbec0c8d31dcab759ddf7974cbd3293946f768eb450cf2412`  
		Last Modified: Thu, 06 Oct 2022 01:01:05 GMT  
		Size: 679.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2906528c85638a4e0d3a480b9ed3a8545fb05b39295a3b2502acbf54e19c086`  
		Last Modified: Thu, 06 Oct 2022 01:01:05 GMT  
		Size: 9.8 KB (9752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144b25be025f9a43ae6d88974ac5cb25f12f4154473db1d5e41d4e811221f746`  
		Last Modified: Thu, 06 Oct 2022 01:01:05 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7678322670d0e3a0c531b6fc7529d8bcbdc828fd51258b3b8cbe7f0071bc6b8e`  
		Last Modified: Thu, 06 Oct 2022 01:01:05 GMT  
		Size: 10.7 KB (10746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44dfa3f4d0c537aa63ea69e03d4730f867c13385e8f68e70a1844223420998bf`  
		Last Modified: Thu, 06 Oct 2022 01:01:06 GMT  
		Size: 2.5 MB (2543380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da0242186ce115c19bcfa633519fbeba53a6c37e057ab5505667cb588478a783`  
		Last Modified: Thu, 06 Oct 2022 01:02:55 GMT  
		Size: 281.6 MB (281600709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d951911ca3c916a9b0ec1cd71284f2bd4e6bf119887bc6d497403dc0460261e`  
		Last Modified: Thu, 06 Oct 2022 01:02:30 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882089e412c29352959bde2c6ec248063bea5dfedf80c31937718271be70cdfe`  
		Last Modified: Thu, 06 Oct 2022 01:02:33 GMT  
		Size: 12.8 MB (12770807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full-java17-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:68a775f7c5d8fb14cdf298d37d67ccfee7fec0a1cc0239b0e972ead27f03f28b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.9 MB (449940590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2210171bd35576ad06049f9f57f66d6c8964a9c75d00ee81f70c56feb97d69a3`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 25 Oct 2022 01:23:11 GMT
ADD file:c657b467ecb15f1f4a49a5f04a525f38924750c8187c9ef9f0b886d0264e21f1 in / 
# Tue, 25 Oct 2022 01:23:12 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:13:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Oct 2022 08:14:15 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Nov 2022 20:51:10 GMT
ENV JAVA_VERSION=jdk-17.0.5+8_openj9-0.35.0
# Thu, 10 Nov 2022 20:53:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8f934ce1745f52a067bdeb56b3b9e9192f51e674ff2956a1e53b33e44ea5ca42';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.5%2B8_openj9-0.35.0/ibm-semeru-open-jre_aarch64_linux_17.0.5_8_openj9-0.35.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d54972fb938f655a3665512c7181c2c5813e3bfe742650d6081e2f480388ef2f';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.5%2B8_openj9-0.35.0/ibm-semeru-open-jre_ppc64le_linux_17.0.5_8_openj9-0.35.0.tar.gz';          ;;        amd64|x86_64)          ESUM='759f9c507e0faf53b260ee9f492bab8fdeb8091bdecad904134861714e4d913b';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.5%2B8_openj9-0.35.0/ibm-semeru-open-jre_x64_linux_17.0.5_8_openj9-0.35.0.tar.gz';          ;;        s390x)          ESUM='64ffeaff0ea4915fb66d3356ef5de65e884172b031e0c268bdeb4d2aa6be1c91';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.5%2B8_openj9-0.35.0/ibm-semeru-open-jre_s390x_linux_17.0.5_8_openj9-0.35.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 10 Nov 2022 20:53:22 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Nov 2022 20:53:22 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 10 Nov 2022 20:53:56 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 11 Nov 2022 00:41:26 GMT
ARG VERBOSE=false
# Fri, 11 Nov 2022 00:41:27 GMT
ARG OPENJ9_SCC=true
# Tue, 15 Nov 2022 00:55:46 GMT
ARG EN_SHA=1ce31500fa2422ed1410137cd50d33e18cf42ad0ae0b5a3e545183ae801869e0
# Tue, 15 Nov 2022 00:55:46 GMT
ARG NON_IBM_SHA=1f032aeb46b5f5f4262f123cb2339230e2755cac039cb1bf0285cbb0f37fe7c8
# Tue, 15 Nov 2022 00:55:46 GMT
ARG NOTICES_SHA=46056efcb4c0e11e1cc9a33104c4d2ae9b42d566ec74885804914c4eb41ef2ec
# Tue, 15 Nov 2022 00:55:46 GMT
LABEL org.opencontainers.image.authors=Chris Potter, Christy Jesuraj, Melissa Lee org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=22.0.0.11 org.opencontainers.image.revision=cl221120221010-1540 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Tue, 15 Nov 2022 00:55:46 GMT
ENV LIBERTY_VERSION=22.0.0_11
# Tue, 15 Nov 2022 00:55:47 GMT
ARG LIBERTY_URL
# Tue, 15 Nov 2022 00:55:47 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 15 Nov 2022 00:55:56 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ce31500fa2422ed1410137cd50d33e18cf42ad0ae0b5a3e545183ae801869e0 NON_IBM_SHA=1f032aeb46b5f5f4262f123cb2339230e2755cac039cb1bf0285cbb0f37fe7c8 NOTICES_SHA=46056efcb4c0e11e1cc9a33104c4d2ae9b42d566ec74885804914c4eb41ef2ec OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 00:55:57 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 00:55:57 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=22.0.0.11 BuildLabel=cl221120221010-1540
# Tue, 15 Nov 2022 00:55:57 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 15 Nov 2022 00:55:58 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ce31500fa2422ed1410137cd50d33e18cf42ad0ae0b5a3e545183ae801869e0 NON_IBM_SHA=1f032aeb46b5f5f4262f123cb2339230e2755cac039cb1bf0285cbb0f37fe7c8 NOTICES_SHA=46056efcb4c0e11e1cc9a33104c4d2ae9b42d566ec74885804914c4eb41ef2ec VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Tue, 15 Nov 2022 00:55:58 GMT
COPY dir:8bf844c49178cf63745af9ec643f57d70bd92c28166fabfad188dfc250d88353 in /opt/ibm/helpers/ 
# Tue, 15 Nov 2022 00:55:58 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Tue, 15 Nov 2022 00:55:59 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ce31500fa2422ed1410137cd50d33e18cf42ad0ae0b5a3e545183ae801869e0 NON_IBM_SHA=1f032aeb46b5f5f4262f123cb2339230e2755cac039cb1bf0285cbb0f37fe7c8 NOTICES_SHA=46056efcb4c0e11e1cc9a33104c4d2ae9b42d566ec74885804914c4eb41ef2ec VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Tue, 15 Nov 2022 00:56:04 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ce31500fa2422ed1410137cd50d33e18cf42ad0ae0b5a3e545183ae801869e0 NON_IBM_SHA=1f032aeb46b5f5f4262f123cb2339230e2755cac039cb1bf0285cbb0f37fe7c8 NOTICES_SHA=46056efcb4c0e11e1cc9a33104c4d2ae9b42d566ec74885804914c4eb41ef2ec VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Tue, 15 Nov 2022 00:56:04 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 15 Nov 2022 00:56:04 GMT
USER 1001
# Tue, 15 Nov 2022 00:56:04 GMT
EXPOSE 9080 9443
# Tue, 15 Nov 2022 00:56:05 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 15 Nov 2022 00:56:05 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 15 Nov 2022 01:12:35 GMT
ARG VERBOSE=false
# Tue, 15 Nov 2022 01:12:35 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 15 Nov 2022 01:19:56 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Tue, 15 Nov 2022 01:20:03 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Tue, 15 Nov 2022 01:20:33 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:a63328f08dbd14148b5ffe154c18846ead48e759779d007b78ec3fb19f5f43a5`  
		Last Modified: Tue, 25 Oct 2022 01:24:36 GMT  
		Size: 27.0 MB (27016028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013e4f2f9b7bdc2ee481845944ba279996ae945acfe957a1ebd0a7bc03f955fa`  
		Last Modified: Tue, 25 Oct 2022 08:43:33 GMT  
		Size: 15.7 MB (15709455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef2d112c3749fafe2cfa159e09120759422eb5a33227550213d13a8f5072f79`  
		Last Modified: Thu, 10 Nov 2022 21:00:00 GMT  
		Size: 47.2 MB (47171478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f117c0f0a17c61fe3ca72537d53475456ef6dbb287039c6797796fe545691752`  
		Last Modified: Thu, 10 Nov 2022 20:59:54 GMT  
		Size: 4.9 MB (4896171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82bcc44b7d32628c412674b4e9572a4bbc959fb8607d0dff86868465be3b475b`  
		Last Modified: Tue, 15 Nov 2022 01:24:14 GMT  
		Size: 14.3 MB (14308692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40deac6fd84e2e2b058aad4f3226c48351c3abe18498adaaa65ac3839f02f304`  
		Last Modified: Tue, 15 Nov 2022 01:24:12 GMT  
		Size: 680.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c664d5911fc88f74035f0384e5236446ebf621f9091c255e78d884175ca61d`  
		Last Modified: Tue, 15 Nov 2022 01:24:11 GMT  
		Size: 9.8 KB (9752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ec846ab7a5628db6872e48a1d3603b70565f62e938e179c32b8466a239f0c9`  
		Last Modified: Tue, 15 Nov 2022 01:24:11 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb90ead139d1d06df3a6ad8384d3b484b5b780a75351fe4628fe34f242276ef`  
		Last Modified: Tue, 15 Nov 2022 01:24:11 GMT  
		Size: 10.7 KB (10731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403688d91784c72257bb623f78beac3253168a3a7c74e8e2d6b5a8b6c91f7c11`  
		Last Modified: Tue, 15 Nov 2022 01:24:12 GMT  
		Size: 2.6 MB (2592368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91a6d6d4087079f0052c55704fe0c9d4760c226fe54e451d63fb4eeceb4179b`  
		Last Modified: Tue, 15 Nov 2022 01:25:19 GMT  
		Size: 323.6 MB (323559458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765bbe2f01cbf354d5fecb45469d65d1580de9a8b80ab48c558bfddd68ffc072`  
		Last Modified: Tue, 15 Nov 2022 01:25:04 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d85dd480bf6ff0837dc44e3c453509c09b55c027deef5c63dbf25c06597890d2`  
		Last Modified: Tue, 15 Nov 2022 01:25:06 GMT  
		Size: 14.7 MB (14664560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
