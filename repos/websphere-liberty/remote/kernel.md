## `websphere-liberty:kernel`

```console
$ docker pull websphere-liberty@sha256:2547d62b73d0b00a0eb0b8d38023d61d7a647e705747ed5940c0b3a90a2b2718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:kernel` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:c4c751a99b4a719588a54cc90de4f035a3a6c2b7d800fc4052651977df1367ac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.0 MB (185976841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840c460a7c57f9e5d723103ceba5c002279853e0db87fdce7acb56bfe3e484c9`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:44:53 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 04 May 2023 07:44:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:44:59 GMT
ENV JAVA_VERSION=8.0.8.0
# Thu, 04 May 2023 07:45:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='39cf0ebeda2461c0ee81636d745643713a37863d729784c46a48b4eded4717fb';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bef3e93e4b1025e8350492fed0f6a5a743a2d35fbacdb7820cc539d24c891a4e';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='87d22ee3d2e20faa9854044aa46bf6be5d39f8ceb9ccf91574c7518f2535dfcb';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='227ada7516542c170a920bc78a416c1dc492cba4321a23f42bd7e640ddc890e5';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 04 May 2023 07:45:58 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Thu, 04 May 2023 16:30:49 GMT
ARG VERBOSE=false
# Thu, 04 May 2023 16:30:49 GMT
ARG OPENJ9_SCC=true
# Thu, 04 May 2023 16:30:49 GMT
ARG EN_SHA=d7580938d35387110e39c3c8b3bb5c1f8dc9f0418a2f77799dbcf69a2ab63093
# Thu, 04 May 2023 16:30:49 GMT
ARG NON_IBM_SHA=0d97a3e5cf5403a9b3be514509977f4e9be4a2ac4258e692ef8e64761910f4c0
# Thu, 04 May 2023 16:30:49 GMT
ARG NOTICES_SHA=71f58dc38b4c9b60beaec4459b97b0d08228ad8e5fe5e3a0f4fd7e7c66285925
# Thu, 04 May 2023 16:30:49 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=23.0.0.4 org.opencontainers.image.revision=cl230420230418-0035 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 04 May 2023 16:30:49 GMT
ENV LIBERTY_VERSION=23.0.0_04
# Thu, 04 May 2023 16:30:50 GMT
ARG LIBERTY_URL
# Thu, 04 May 2023 16:30:50 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 04 May 2023 16:31:07 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=d7580938d35387110e39c3c8b3bb5c1f8dc9f0418a2f77799dbcf69a2ab63093 NON_IBM_SHA=0d97a3e5cf5403a9b3be514509977f4e9be4a2ac4258e692ef8e64761910f4c0 NOTICES_SHA=71f58dc38b4c9b60beaec4459b97b0d08228ad8e5fe5e3a0f4fd7e7c66285925 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 16:31:07 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Thu, 04 May 2023 16:31:07 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=23.0.0.4 BuildLabel=cl230420230418-0035
# Thu, 04 May 2023 16:31:07 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 04 May 2023 16:31:08 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=d7580938d35387110e39c3c8b3bb5c1f8dc9f0418a2f77799dbcf69a2ab63093 NON_IBM_SHA=0d97a3e5cf5403a9b3be514509977f4e9be4a2ac4258e692ef8e64761910f4c0 NOTICES_SHA=71f58dc38b4c9b60beaec4459b97b0d08228ad8e5fe5e3a0f4fd7e7c66285925 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 04 May 2023 16:31:08 GMT
COPY dir:0f3e336b1e5adb84a625050153035561e1c9802a57b7b90b5a17ebb82adba489 in /opt/ibm/helpers/ 
# Thu, 04 May 2023 16:31:08 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 04 May 2023 16:31:09 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=d7580938d35387110e39c3c8b3bb5c1f8dc9f0418a2f77799dbcf69a2ab63093 NON_IBM_SHA=0d97a3e5cf5403a9b3be514509977f4e9be4a2ac4258e692ef8e64761910f4c0 NOTICES_SHA=71f58dc38b4c9b60beaec4459b97b0d08228ad8e5fe5e3a0f4fd7e7c66285925 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 04 May 2023 16:31:16 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=d7580938d35387110e39c3c8b3bb5c1f8dc9f0418a2f77799dbcf69a2ab63093 NON_IBM_SHA=0d97a3e5cf5403a9b3be514509977f4e9be4a2ac4258e692ef8e64761910f4c0 NOTICES_SHA=71f58dc38b4c9b60beaec4459b97b0d08228ad8e5fe5e3a0f4fd7e7c66285925 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 04 May 2023 16:31:16 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Thu, 04 May 2023 16:31:16 GMT
USER 1001
# Thu, 04 May 2023 16:31:16 GMT
EXPOSE 9080 9443
# Thu, 04 May 2023 16:31:17 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 04 May 2023 16:31:17 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bee7fd4007af244555d448c1fb80ceb220cf70203647e0705bbdd49468c13e4`  
		Last Modified: Thu, 04 May 2023 07:48:21 GMT  
		Size: 1.4 MB (1446362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497fe82b0d5da8b440c5da09d2e803344e57e5bdf8e8fe81bf9b838fba8ce704`  
		Last Modified: Thu, 04 May 2023 07:48:29 GMT  
		Size: 133.9 MB (133853339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:524fe12c06d06f218122939be9ba97755a3b8327054683b80b93f44653da6f85`  
		Last Modified: Thu, 04 May 2023 17:21:41 GMT  
		Size: 14.3 MB (14346777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85703371799da1000c7d066f0304b6c94541fb8a6ba2eef6504cee8ef136ec38`  
		Last Modified: Thu, 04 May 2023 17:21:37 GMT  
		Size: 680.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc9221bcbf47dce36e7def743291ded9f70e0f482f030943616f6c331e5a8ad`  
		Last Modified: Thu, 04 May 2023 17:21:38 GMT  
		Size: 9.8 KB (9818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b10ebc0c4bce8824da6a7e981e27272505a78b444e1915e6b7c3656b6f327d`  
		Last Modified: Thu, 04 May 2023 17:21:37 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c11e3d18cd4e289d535421b7fa60f02784a3e9fefd38826fdacbd3595938da`  
		Last Modified: Thu, 04 May 2023 17:21:37 GMT  
		Size: 10.8 KB (10802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30ee90ac2a48a5ce2f4450af16c47a71aa8e1bac06c6722f506ab3fc27ae4e5`  
		Last Modified: Thu, 04 May 2023 17:21:38 GMT  
		Size: 5.9 MB (5878570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:b2061e52034b649d313b25f436bb095d878c7ba1252392bf34c66da10f6c707a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.7 MB (190687190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcc150f57ea2b6f0b5852f395e5d80d576cef43bdc8d17f71aa2dec92eb1e4db`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:17 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:18 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:21 GMT
ADD file:e75f08a67f0576b5441bb2fe454cad4b5b31a9d4efea23be791af62e1e0c712f in / 
# Tue, 25 Apr 2023 17:30:21 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 14:09:46 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 04 May 2023 14:09:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 14:09:58 GMT
ENV JAVA_VERSION=8.0.8.0
# Thu, 04 May 2023 14:12:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='39cf0ebeda2461c0ee81636d745643713a37863d729784c46a48b4eded4717fb';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bef3e93e4b1025e8350492fed0f6a5a743a2d35fbacdb7820cc539d24c891a4e';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='87d22ee3d2e20faa9854044aa46bf6be5d39f8ceb9ccf91574c7518f2535dfcb';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='227ada7516542c170a920bc78a416c1dc492cba4321a23f42bd7e640ddc890e5';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 04 May 2023 14:12:40 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Thu, 04 May 2023 20:36:44 GMT
ARG VERBOSE=false
# Thu, 04 May 2023 20:36:44 GMT
ARG OPENJ9_SCC=true
# Thu, 04 May 2023 20:36:45 GMT
ARG EN_SHA=d7580938d35387110e39c3c8b3bb5c1f8dc9f0418a2f77799dbcf69a2ab63093
# Thu, 04 May 2023 20:36:45 GMT
ARG NON_IBM_SHA=0d97a3e5cf5403a9b3be514509977f4e9be4a2ac4258e692ef8e64761910f4c0
# Thu, 04 May 2023 20:36:46 GMT
ARG NOTICES_SHA=71f58dc38b4c9b60beaec4459b97b0d08228ad8e5fe5e3a0f4fd7e7c66285925
# Thu, 04 May 2023 20:36:46 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=23.0.0.4 org.opencontainers.image.revision=cl230420230418-0035 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 04 May 2023 20:36:46 GMT
ENV LIBERTY_VERSION=23.0.0_04
# Thu, 04 May 2023 20:36:47 GMT
ARG LIBERTY_URL
# Thu, 04 May 2023 20:36:47 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 04 May 2023 20:37:46 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=d7580938d35387110e39c3c8b3bb5c1f8dc9f0418a2f77799dbcf69a2ab63093 NON_IBM_SHA=0d97a3e5cf5403a9b3be514509977f4e9be4a2ac4258e692ef8e64761910f4c0 NOTICES_SHA=71f58dc38b4c9b60beaec4459b97b0d08228ad8e5fe5e3a0f4fd7e7c66285925 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 20:37:47 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Thu, 04 May 2023 20:37:48 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=23.0.0.4 BuildLabel=cl230420230418-0035
# Thu, 04 May 2023 20:37:49 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 04 May 2023 20:37:52 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=d7580938d35387110e39c3c8b3bb5c1f8dc9f0418a2f77799dbcf69a2ab63093 NON_IBM_SHA=0d97a3e5cf5403a9b3be514509977f4e9be4a2ac4258e692ef8e64761910f4c0 NOTICES_SHA=71f58dc38b4c9b60beaec4459b97b0d08228ad8e5fe5e3a0f4fd7e7c66285925 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 04 May 2023 20:37:53 GMT
COPY dir:0f3e336b1e5adb84a625050153035561e1c9802a57b7b90b5a17ebb82adba489 in /opt/ibm/helpers/ 
# Thu, 04 May 2023 20:37:54 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 04 May 2023 20:37:56 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=d7580938d35387110e39c3c8b3bb5c1f8dc9f0418a2f77799dbcf69a2ab63093 NON_IBM_SHA=0d97a3e5cf5403a9b3be514509977f4e9be4a2ac4258e692ef8e64761910f4c0 NOTICES_SHA=71f58dc38b4c9b60beaec4459b97b0d08228ad8e5fe5e3a0f4fd7e7c66285925 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 04 May 2023 20:38:11 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=d7580938d35387110e39c3c8b3bb5c1f8dc9f0418a2f77799dbcf69a2ab63093 NON_IBM_SHA=0d97a3e5cf5403a9b3be514509977f4e9be4a2ac4258e692ef8e64761910f4c0 NOTICES_SHA=71f58dc38b4c9b60beaec4459b97b0d08228ad8e5fe5e3a0f4fd7e7c66285925 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 04 May 2023 20:38:11 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Thu, 04 May 2023 20:38:12 GMT
USER 1001
# Thu, 04 May 2023 20:38:13 GMT
EXPOSE 9080 9443
# Thu, 04 May 2023 20:38:13 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 04 May 2023 20:38:14 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:f6a63d8cd043e76933823b18cbb7057a55bb4d66d64639c81e15a4700c101582`  
		Last Modified: Wed, 03 May 2023 17:09:07 GMT  
		Size: 35.7 MB (35712706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f8e1caab24446aefe2b3b975cf39a80aad52df873c970c64a0a65cc82be5c0`  
		Last Modified: Thu, 04 May 2023 14:18:24 GMT  
		Size: 1.6 MB (1552398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908bd1b1e780377c2830ba296a4cfccc03d4b7967bc41aa767ee6ceaff2f3c81`  
		Last Modified: Thu, 04 May 2023 14:18:40 GMT  
		Size: 133.6 MB (133556002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9a74370575a86e9f95e058cc76d142c181ec03c33549d91aa8cfddd3cf2684`  
		Last Modified: Thu, 04 May 2023 22:18:19 GMT  
		Size: 14.3 MB (14347328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c2b0d60d8cb06c021333c2471482bf3b5563e5adb6e1b6e9533b825f599fb5`  
		Last Modified: Thu, 04 May 2023 22:18:15 GMT  
		Size: 686.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a1645074458f91da133ecfb817d5383f696deb45e621ee37eb6fd97f3c435d`  
		Last Modified: Thu, 04 May 2023 22:18:15 GMT  
		Size: 9.8 KB (9820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b60f8ac5608ae99431256430cb2be8d76f089d357e5d7d02ed4d4114973cadcc`  
		Last Modified: Thu, 04 May 2023 22:18:15 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c0b4d609715fb8d5995fb12809143fc9b60063cf0dd006a989ec1d798368e6`  
		Last Modified: Thu, 04 May 2023 22:18:15 GMT  
		Size: 10.8 KB (10815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f1527abf00b71338e5918e32e507ebca56d3ab76451eda62b5ed0f9e1397e9`  
		Last Modified: Thu, 04 May 2023 22:18:16 GMT  
		Size: 5.5 MB (5497161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:a794437046c5c8fae27115396e3a25e8065b0baf74dd411893497477260173bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.1 MB (181052121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e2b2ff28bdeefc1a4eee97e8a23ee5c3c3e55a99bbee91c2112fb8dff551c9`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 25 Apr 2023 17:44:52 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:44:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:44:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:44:52 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:44:54 GMT
ADD file:bbc65a9f059dc165e33f9a25ffaa40aab1a1f65164198a44394ec3065c82ae21 in / 
# Tue, 25 Apr 2023 17:44:54 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 08:44:44 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 04 May 2023 08:44:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 08:44:58 GMT
ENV JAVA_VERSION=8.0.8.0
# Thu, 04 May 2023 08:45:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='39cf0ebeda2461c0ee81636d745643713a37863d729784c46a48b4eded4717fb';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bef3e93e4b1025e8350492fed0f6a5a743a2d35fbacdb7820cc539d24c891a4e';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='87d22ee3d2e20faa9854044aa46bf6be5d39f8ceb9ccf91574c7518f2535dfcb';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='227ada7516542c170a920bc78a416c1dc492cba4321a23f42bd7e640ddc890e5';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 04 May 2023 08:45:49 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 05 May 2023 04:05:47 GMT
ARG VERBOSE=false
# Fri, 05 May 2023 04:05:47 GMT
ARG OPENJ9_SCC=true
# Fri, 05 May 2023 04:05:47 GMT
ARG EN_SHA=d7580938d35387110e39c3c8b3bb5c1f8dc9f0418a2f77799dbcf69a2ab63093
# Fri, 05 May 2023 04:05:47 GMT
ARG NON_IBM_SHA=0d97a3e5cf5403a9b3be514509977f4e9be4a2ac4258e692ef8e64761910f4c0
# Fri, 05 May 2023 04:05:48 GMT
ARG NOTICES_SHA=71f58dc38b4c9b60beaec4459b97b0d08228ad8e5fe5e3a0f4fd7e7c66285925
# Fri, 05 May 2023 04:05:48 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=23.0.0.4 org.opencontainers.image.revision=cl230420230418-0035 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 05 May 2023 04:05:48 GMT
ENV LIBERTY_VERSION=23.0.0_04
# Fri, 05 May 2023 04:05:48 GMT
ARG LIBERTY_URL
# Fri, 05 May 2023 04:05:48 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 05 May 2023 04:06:01 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=d7580938d35387110e39c3c8b3bb5c1f8dc9f0418a2f77799dbcf69a2ab63093 NON_IBM_SHA=0d97a3e5cf5403a9b3be514509977f4e9be4a2ac4258e692ef8e64761910f4c0 NOTICES_SHA=71f58dc38b4c9b60beaec4459b97b0d08228ad8e5fe5e3a0f4fd7e7c66285925 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 05 May 2023 04:06:02 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Fri, 05 May 2023 04:06:02 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=23.0.0.4 BuildLabel=cl230420230418-0035
# Fri, 05 May 2023 04:06:02 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 05 May 2023 04:06:03 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=d7580938d35387110e39c3c8b3bb5c1f8dc9f0418a2f77799dbcf69a2ab63093 NON_IBM_SHA=0d97a3e5cf5403a9b3be514509977f4e9be4a2ac4258e692ef8e64761910f4c0 NOTICES_SHA=71f58dc38b4c9b60beaec4459b97b0d08228ad8e5fe5e3a0f4fd7e7c66285925 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 05 May 2023 04:06:03 GMT
COPY dir:0f3e336b1e5adb84a625050153035561e1c9802a57b7b90b5a17ebb82adba489 in /opt/ibm/helpers/ 
# Fri, 05 May 2023 04:06:03 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 05 May 2023 04:06:04 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=d7580938d35387110e39c3c8b3bb5c1f8dc9f0418a2f77799dbcf69a2ab63093 NON_IBM_SHA=0d97a3e5cf5403a9b3be514509977f4e9be4a2ac4258e692ef8e64761910f4c0 NOTICES_SHA=71f58dc38b4c9b60beaec4459b97b0d08228ad8e5fe5e3a0f4fd7e7c66285925 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 05 May 2023 04:06:09 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=d7580938d35387110e39c3c8b3bb5c1f8dc9f0418a2f77799dbcf69a2ab63093 NON_IBM_SHA=0d97a3e5cf5403a9b3be514509977f4e9be4a2ac4258e692ef8e64761910f4c0 NOTICES_SHA=71f58dc38b4c9b60beaec4459b97b0d08228ad8e5fe5e3a0f4fd7e7c66285925 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 05 May 2023 04:06:10 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 05 May 2023 04:06:10 GMT
USER 1001
# Fri, 05 May 2023 04:06:10 GMT
EXPOSE 9080 9443
# Fri, 05 May 2023 04:06:10 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 05 May 2023 04:06:10 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:78722793f0008ff8422830a0106f21e8bc168fb9aac12cc99fb223799951759e`  
		Last Modified: Wed, 03 May 2023 22:33:36 GMT  
		Size: 28.6 MB (28647905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9459c54d841fa6f6b374fa6fe3230943f4104eb1c43155f1255ff1c9e735443`  
		Last Modified: Thu, 04 May 2023 08:48:50 GMT  
		Size: 1.5 MB (1452439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f1a3330c7bf0b93483213fd37e7f563f9c48a90f30d9ec27d5b01cf032a5af`  
		Last Modified: Thu, 04 May 2023 08:48:59 GMT  
		Size: 130.7 MB (130656050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e42819a5bf6984ce1077238ebd6bc30809f897453abc18e32697d9d0b844e8`  
		Last Modified: Fri, 05 May 2023 05:09:14 GMT  
		Size: 14.3 MB (14347101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e43ec2862967467907e500ac0101063e6351859c3fff3b123b15005a7c668f`  
		Last Modified: Fri, 05 May 2023 05:09:11 GMT  
		Size: 677.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0193225f7d167292d774d4392bd72e99bfdb5fe7e3a045c71d756a0d55757f46`  
		Last Modified: Fri, 05 May 2023 05:09:11 GMT  
		Size: 9.8 KB (9815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54433df610647d6cdb4a26028f03de0720188ea121befa2e4bb5c42152accd97`  
		Last Modified: Fri, 05 May 2023 05:09:11 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cfa3a66d7ca4186047eaeec69700da17028135d5fcd4717cdbe0d5848c8dfca`  
		Last Modified: Fri, 05 May 2023 05:09:11 GMT  
		Size: 10.8 KB (10805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e9736bd80cdb51a7beae40e05a4ef3d3eb3b70d8c82ad433ef7a3c3f427424`  
		Last Modified: Fri, 05 May 2023 05:09:12 GMT  
		Size: 5.9 MB (5927056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
