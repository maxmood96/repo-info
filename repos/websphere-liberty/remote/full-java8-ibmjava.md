## `websphere-liberty:full-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:08dff9ae051292c3041de8f24cf930f4b51881ab9d636fa7e2c5f1af54f93bde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:full-java8-ibmjava` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:1843cfc1f817949ba924ccb1dacfda582cf3ab1aaa979f69ce07c1c73f82bc01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.2 MB (547238528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558f13f59152f87fe8a6e62cc2a92e25995cf3d15f597853e9140ba67941992c`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 05:19:55 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 03 Oct 2023 05:20:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 05:20:01 GMT
ENV JAVA_VERSION=8.0.8.11
# Tue, 03 Oct 2023 05:21:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='eef1360ed6a3a4054c212807dd85bf4d78098dd0670455ea6a9443fb74b15c65';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b8df030cbb96ce68cedc69ec255d496084307d5fbb2041d9dd15a58d7a3d7f12';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='69bcd643a5b1fdddcd920d8cefb60566d8e06027b4b3e600715464ecfd60662d';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='182fd5bd6f73b968a8eb221aec907b8a04a58021214bc41f9fe37417d22f712e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 03 Oct 2023 05:21:06 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 03 Oct 2023 10:30:26 GMT
USER root
# Tue, 03 Oct 2023 10:30:26 GMT
ARG VERBOSE=false
# Tue, 03 Oct 2023 10:30:26 GMT
ARG OPENJ9_SCC=true
# Tue, 03 Oct 2023 10:30:26 GMT
ARG LIBERTY_VERSION=23.0.0.9
# Tue, 03 Oct 2023 10:30:26 GMT
ARG LIBERTY_BUILD_LABEL=cl230920230904-1158
# Tue, 03 Oct 2023 10:30:26 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=23.0.0.9 org.opencontainers.image.revision=cl230920230904-1158 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Tue, 03 Oct 2023 10:30:26 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Tue, 03 Oct 2023 10:30:27 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=23.0.0.9 BuildLabel=cl230920230904-1158
# Tue, 03 Oct 2023 10:30:34 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230920230904-1158 LIBERTY_VERSION=23.0.0.9 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*;
# Tue, 03 Oct 2023 10:30:34 GMT
ARG LIBERTY_URL
# Tue, 03 Oct 2023 10:30:34 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 03 Oct 2023 10:30:46 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl230920230904-1158 LIBERTY_VERSION=23.0.0.9 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 10:30:46 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 03 Oct 2023 10:30:47 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl230920230904-1158 LIBERTY_VERSION=23.0.0.9 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env
# Tue, 03 Oct 2023 10:30:47 GMT
COPY file:7278f8f20139aab77b5c9fa76ad85e8a92836053c3ecfb9f5925f1a19788ef47 in /opt/ibm/NOTICES 
# Tue, 03 Oct 2023 10:30:48 GMT
COPY dir:4b5f5eed522fc9e4e2492b23f4706c27fe3a6f8cdaf689c3914c172a013d14dd in /opt/ibm/helpers/ 
# Tue, 03 Oct 2023 10:30:48 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Tue, 03 Oct 2023 10:30:48 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl230920230904-1158 LIBERTY_VERSION=23.0.0.9 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Tue, 03 Oct 2023 10:30:55 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl230920230904-1158 LIBERTY_VERSION=23.0.0.9 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Tue, 03 Oct 2023 10:30:55 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Tue, 03 Oct 2023 10:30:55 GMT
USER 1001
# Tue, 03 Oct 2023 10:30:55 GMT
EXPOSE 9080 9443
# Tue, 03 Oct 2023 10:30:55 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 03 Oct 2023 10:30:55 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 03 Oct 2023 10:31:49 GMT
ARG VERBOSE=false
# Tue, 03 Oct 2023 10:31:49 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 03 Oct 2023 10:40:43 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw;
# Tue, 03 Oct 2023 10:40:44 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Tue, 03 Oct 2023 10:41:18 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84e200272255a6616d7743262d3941ca6f0bbf7b449faad76984c248df2bf7f`  
		Last Modified: Tue, 03 Oct 2023 05:23:40 GMT  
		Size: 1.5 MB (1469189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4270374fd1193596c5073e693cb85c1b5936334847757e5b727ffefb60dc1472`  
		Last Modified: Tue, 03 Oct 2023 05:23:51 GMT  
		Size: 134.2 MB (134198566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a3b9956db2cd1d02b13fe4640aaf9c54c321784e25cdae7705a43e2a8fdf5e`  
		Last Modified: Tue, 03 Oct 2023 11:10:33 GMT  
		Size: 266.1 KB (266085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1974bb5d2ed44cc29674cc4e7ec5206b65b2aba27eff457a488995d95aa179f1`  
		Last Modified: Tue, 03 Oct 2023 11:10:35 GMT  
		Size: 17.0 MB (17016653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66461e57d60c8a492fe29962748d5e248fe111c17598d42f5dd918859813dc22`  
		Last Modified: Tue, 03 Oct 2023 11:10:33 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7710533f537979a041e3c9e1f8861431b2ad869953e968b8543f151bb645cbae`  
		Last Modified: Tue, 03 Oct 2023 11:10:31 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c59f31e2e3a8db92ce4130015741f243b4e58b75e7851a1b0c315dd8a57f34d`  
		Last Modified: Tue, 03 Oct 2023 11:10:31 GMT  
		Size: 11.3 KB (11251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bedae499e7eb95fbc5d3b2a64071132ade1aaf8a72204703b14681e2181538a1`  
		Last Modified: Tue, 03 Oct 2023 11:10:31 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59a1f59504ce6728adfa88080d33ad32cb9b0a82a19773a61ee5c869029650d`  
		Last Modified: Tue, 03 Oct 2023 11:10:31 GMT  
		Size: 12.2 KB (12179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eeda2e2159c41cf18b01f9d896471490eadec96aa572af4ec96f529257a5859`  
		Last Modified: Tue, 03 Oct 2023 11:10:32 GMT  
		Size: 5.5 MB (5520489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748ab958e5acedfb5542de8ee257716d5eeaa5ec06cca655d948fffaf0670875`  
		Last Modified: Tue, 03 Oct 2023 11:11:26 GMT  
		Size: 342.9 MB (342941536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f848939f3afd206e7d1e17c59ddb61d60b90c92e0877baecc1ddd1f7bfc6596b`  
		Last Modified: Tue, 03 Oct 2023 11:11:08 GMT  
		Size: 947.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a16281df0114487e6eb6bdebe07e2e7667d0fad3a8d6f1cba111043242bb3a`  
		Last Modified: Tue, 03 Oct 2023 11:11:10 GMT  
		Size: 15.4 MB (15358354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:5189767e59066ed7149205947519787d99297a8cb40dd1dfd687216a051c2370
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.6 MB (549559353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be6fa2f7744f4139a01b7fbc5cceea569b73f2fa116818f230d1fcbfee8e504`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 05 Oct 2023 07:34:18 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:34:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:34:22 GMT
ADD file:595ff761b2778bdc6bb59cbe8ce51c4a247e0f279ccd59a17b5be6cdeac0b4d2 in / 
# Thu, 05 Oct 2023 07:34:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 08:13:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 13 Oct 2023 08:13:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 08:13:27 GMT
ENV JAVA_VERSION=8.0.8.11
# Fri, 13 Oct 2023 08:14:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='eef1360ed6a3a4054c212807dd85bf4d78098dd0670455ea6a9443fb74b15c65';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b8df030cbb96ce68cedc69ec255d496084307d5fbb2041d9dd15a58d7a3d7f12';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='69bcd643a5b1fdddcd920d8cefb60566d8e06027b4b3e600715464ecfd60662d';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='182fd5bd6f73b968a8eb221aec907b8a04a58021214bc41f9fe37417d22f712e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 13 Oct 2023 08:14:49 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 13 Oct 2023 09:21:59 GMT
USER root
# Fri, 13 Oct 2023 09:21:59 GMT
ARG VERBOSE=false
# Fri, 13 Oct 2023 09:22:00 GMT
ARG OPENJ9_SCC=true
# Fri, 13 Oct 2023 09:22:00 GMT
ARG LIBERTY_VERSION=23.0.0.9
# Fri, 13 Oct 2023 09:22:01 GMT
ARG LIBERTY_BUILD_LABEL=cl230920230904-1158
# Fri, 13 Oct 2023 09:22:01 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=23.0.0.9 org.opencontainers.image.revision=cl230920230904-1158 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 13 Oct 2023 09:22:01 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Fri, 13 Oct 2023 09:22:02 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=23.0.0.9 BuildLabel=cl230920230904-1158
# Fri, 13 Oct 2023 09:22:20 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230920230904-1158 LIBERTY_VERSION=23.0.0.9 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*;
# Fri, 13 Oct 2023 09:22:20 GMT
ARG LIBERTY_URL
# Fri, 13 Oct 2023 09:22:21 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 13 Oct 2023 09:22:37 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl230920230904-1158 LIBERTY_VERSION=23.0.0.9 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 09:22:38 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 13 Oct 2023 09:22:41 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl230920230904-1158 LIBERTY_VERSION=23.0.0.9 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env
# Fri, 13 Oct 2023 09:22:41 GMT
COPY file:7278f8f20139aab77b5c9fa76ad85e8a92836053c3ecfb9f5925f1a19788ef47 in /opt/ibm/NOTICES 
# Fri, 13 Oct 2023 09:22:42 GMT
COPY dir:4b5f5eed522fc9e4e2492b23f4706c27fe3a6f8cdaf689c3914c172a013d14dd in /opt/ibm/helpers/ 
# Fri, 13 Oct 2023 09:22:42 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 13 Oct 2023 09:22:44 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl230920230904-1158 LIBERTY_VERSION=23.0.0.9 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 13 Oct 2023 09:22:56 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl230920230904-1158 LIBERTY_VERSION=23.0.0.9 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 13 Oct 2023 09:22:59 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 13 Oct 2023 09:23:01 GMT
USER 1001
# Fri, 13 Oct 2023 09:23:01 GMT
EXPOSE 9080 9443
# Fri, 13 Oct 2023 09:23:02 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 13 Oct 2023 09:23:02 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 13 Oct 2023 09:24:40 GMT
ARG VERBOSE=false
# Fri, 13 Oct 2023 09:24:40 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 13 Oct 2023 09:34:57 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw;
# Fri, 13 Oct 2023 09:35:04 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 13 Oct 2023 09:35:44 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:589c4cce1daa100afadbdbeda96025d02f85c117e0e60b70801af41b4e618668`  
		Last Modified: Fri, 13 Oct 2023 06:13:20 GMT  
		Size: 35.7 MB (35682793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904b226304be2a431a19eec30131080b3479f2caad182fbba54f9e23036ee614`  
		Last Modified: Fri, 13 Oct 2023 08:17:57 GMT  
		Size: 1.6 MB (1576632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b66dc3ced6dc65a771df7966ced60e7e5e41efe2173564204b05a317fe2a51`  
		Last Modified: Fri, 13 Oct 2023 08:18:09 GMT  
		Size: 133.9 MB (133871667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b3dd924fc01ab3e7b6d297e4b70c86c27993ef4ba7affb9a04a88d172ae175`  
		Last Modified: Fri, 13 Oct 2023 10:34:45 GMT  
		Size: 270.4 KB (270416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a814394cf3a7692d226820f9af371231cd4615d1d1a462b3e0cf5b62c79f6b`  
		Last Modified: Fri, 13 Oct 2023 10:34:46 GMT  
		Size: 17.0 MB (17017173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51aa282fa7587838b2e15ce368cb25e4ad133503db1036cb890de3640b9536a7`  
		Last Modified: Fri, 13 Oct 2023 10:34:44 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1533658d9b1ba34e69c8d3337f33d999a635b5bc4d08f9ebed6bcb26762348e9`  
		Last Modified: Fri, 13 Oct 2023 10:34:42 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ace629efa8f3db50684e7eaa314617ea74132ae6e95a9860c64145588fc67d`  
		Last Modified: Fri, 13 Oct 2023 10:34:42 GMT  
		Size: 11.3 KB (11257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542b6c2d7de03cb4995d05ee1bc6ecf17f0c0139d71ac8b7abf902521d7b6feb`  
		Last Modified: Fri, 13 Oct 2023 10:34:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6a1f3a57a4ff2c71149977135bb2030f7159b08753d2c2bb626a6681e2af81`  
		Last Modified: Fri, 13 Oct 2023 10:34:42 GMT  
		Size: 12.2 KB (12182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1b9d8d5fa2709e02227a653ebbbcf34a09ebd29f12a9d34651259132466917`  
		Last Modified: Fri, 13 Oct 2023 10:34:43 GMT  
		Size: 5.1 MB (5081919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18fc449f1f8b6d8b967a4536e8d8c9a2a7ca0c614421a85647e1e78527a71aa2`  
		Last Modified: Fri, 13 Oct 2023 10:35:39 GMT  
		Size: 342.9 MB (342942962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4803349355ec44be5963736fe4302d1f17dd1f587c76b852a17b8ec2663a3f35`  
		Last Modified: Fri, 13 Oct 2023 10:35:19 GMT  
		Size: 950.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a57a36c350667d904ed983001f9914e3c6a06f01edf1383683a1f398b442bee`  
		Last Modified: Fri, 13 Oct 2023 10:35:21 GMT  
		Size: 13.1 MB (13088991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:dbbb4dbb0eac690aad3d426fdd222569e53045c455c9ff3336ddb5bdb51bd92b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.0 MB (542013762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0264069bf47a9b17bb1bfcb9e210abc238d49594e5f949444d1ccef5e31828`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 05 Oct 2023 07:29:34 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:29:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:29:34 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:29:36 GMT
ADD file:d165475f8f027ab758a463da57c8c29f5d302f0a87a475ac68fdfae30005c7ac in / 
# Thu, 05 Oct 2023 07:29:36 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 10:19:06 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 13 Oct 2023 10:19:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 10:19:15 GMT
ENV JAVA_VERSION=8.0.8.11
# Fri, 13 Oct 2023 10:20:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='eef1360ed6a3a4054c212807dd85bf4d78098dd0670455ea6a9443fb74b15c65';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b8df030cbb96ce68cedc69ec255d496084307d5fbb2041d9dd15a58d7a3d7f12';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='69bcd643a5b1fdddcd920d8cefb60566d8e06027b4b3e600715464ecfd60662d';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='182fd5bd6f73b968a8eb221aec907b8a04a58021214bc41f9fe37417d22f712e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 13 Oct 2023 10:20:22 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 13 Oct 2023 12:10:49 GMT
USER root
# Fri, 13 Oct 2023 12:10:49 GMT
ARG VERBOSE=false
# Fri, 13 Oct 2023 12:10:49 GMT
ARG OPENJ9_SCC=true
# Fri, 13 Oct 2023 12:10:49 GMT
ARG LIBERTY_VERSION=23.0.0.9
# Fri, 13 Oct 2023 12:10:49 GMT
ARG LIBERTY_BUILD_LABEL=cl230920230904-1158
# Fri, 13 Oct 2023 12:10:49 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=23.0.0.9 org.opencontainers.image.revision=cl230920230904-1158 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 13 Oct 2023 12:10:50 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Fri, 13 Oct 2023 12:10:50 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=23.0.0.9 BuildLabel=cl230920230904-1158
# Fri, 13 Oct 2023 12:10:56 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230920230904-1158 LIBERTY_VERSION=23.0.0.9 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*;
# Fri, 13 Oct 2023 12:10:56 GMT
ARG LIBERTY_URL
# Fri, 13 Oct 2023 12:10:56 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 13 Oct 2023 12:11:05 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl230920230904-1158 LIBERTY_VERSION=23.0.0.9 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 12:11:06 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 13 Oct 2023 12:11:08 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl230920230904-1158 LIBERTY_VERSION=23.0.0.9 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env
# Fri, 13 Oct 2023 12:11:08 GMT
COPY file:7278f8f20139aab77b5c9fa76ad85e8a92836053c3ecfb9f5925f1a19788ef47 in /opt/ibm/NOTICES 
# Fri, 13 Oct 2023 12:11:08 GMT
COPY dir:4b5f5eed522fc9e4e2492b23f4706c27fe3a6f8cdaf689c3914c172a013d14dd in /opt/ibm/helpers/ 
# Fri, 13 Oct 2023 12:11:08 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 13 Oct 2023 12:11:09 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl230920230904-1158 LIBERTY_VERSION=23.0.0.9 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 13 Oct 2023 12:11:14 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl230920230904-1158 LIBERTY_VERSION=23.0.0.9 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 13 Oct 2023 12:11:15 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 13 Oct 2023 12:11:15 GMT
USER 1001
# Fri, 13 Oct 2023 12:11:15 GMT
EXPOSE 9080 9443
# Fri, 13 Oct 2023 12:11:15 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 13 Oct 2023 12:11:15 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 13 Oct 2023 12:12:12 GMT
ARG VERBOSE=false
# Fri, 13 Oct 2023 12:12:13 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 13 Oct 2023 12:21:23 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw;
# Fri, 13 Oct 2023 12:21:33 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 13 Oct 2023 12:22:04 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:818e4e246beb9ab026d2b95bf051fe9610b92dbc0a35b45d09b0cf237b6f3c2e`  
		Last Modified: Fri, 13 Oct 2023 10:16:45 GMT  
		Size: 28.7 MB (28650497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c855df473e374cd3b2cd0795d423dd3af83fe5f371b4696552798894466ecf2e`  
		Last Modified: Fri, 13 Oct 2023 10:23:06 GMT  
		Size: 1.5 MB (1477153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c492c7aab07b58a0cf2430436e2c24488591a66cdfec307d045da70be22993`  
		Last Modified: Fri, 13 Oct 2023 10:23:15 GMT  
		Size: 130.7 MB (130726437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c8396e763c2b866bc0b0c6b9dc4a229e49e6a48c8a2fedfc32736197abb7cf`  
		Last Modified: Fri, 13 Oct 2023 13:10:19 GMT  
		Size: 267.4 KB (267422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e108a131dd40ddb396701949e8760ca32420562f05969507bdaae09a667018e1`  
		Last Modified: Fri, 13 Oct 2023 13:10:20 GMT  
		Size: 17.0 MB (17016870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa9f0e6e084f4338250cb6b689a7958c8a0dfdb2c59bf8631521a882faa80ad`  
		Last Modified: Fri, 13 Oct 2023 13:10:18 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe2a30859d98e46540c0c508632b04a02e0eb1ff0fd1cb137de208ec2bc8668`  
		Last Modified: Fri, 13 Oct 2023 13:10:17 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54afd89ed7b370ea21c101db4f3756558748f43a141e4d9100a5f922f192f492`  
		Last Modified: Fri, 13 Oct 2023 13:10:17 GMT  
		Size: 11.3 KB (11251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b78ff17ed12d901fe1c00191c4218da13f56908e1f96de4bbec924f67994d22`  
		Last Modified: Fri, 13 Oct 2023 13:10:17 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1bab0e784931e8e25f108b9c6069e1b6f863ea53c5590d9dea2ac1a93c13b2e`  
		Last Modified: Fri, 13 Oct 2023 13:10:17 GMT  
		Size: 12.2 KB (12180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686e79b183a28e5c644125283fb20f96f42c123d05d71be0a2c1f88d2addfc56`  
		Last Modified: Fri, 13 Oct 2023 13:10:17 GMT  
		Size: 5.5 MB (5517912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be7120d88c99c24d8c8be4aefb97f5edc528e3cb78168b820b58692fd5e65e95`  
		Last Modified: Fri, 13 Oct 2023 13:11:02 GMT  
		Size: 342.9 MB (342942695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9be98e42499d91c267872dfa8b2eae3eb47a0d4c6840fbaf7028ae87f037d4`  
		Last Modified: Fri, 13 Oct 2023 13:10:41 GMT  
		Size: 947.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12cf16f8de0312945ba67dc999f8319e97d0b2f0853a454d1fa94a729412f326`  
		Last Modified: Fri, 13 Oct 2023 13:10:43 GMT  
		Size: 15.4 MB (15387989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
