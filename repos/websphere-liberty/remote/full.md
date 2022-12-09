## `websphere-liberty:full`

```console
$ docker pull websphere-liberty@sha256:c106a73a5ed948b8ea0e946d5896763222ff05fe07a0bcc8d021c8a82a348893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:full` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:6b212287330a0c0779b906108fb8b67d447a781f9a2a5069e1da0bc00675230c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **519.9 MB (519859598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b248c96e87d7aeed28f12e0a524ebdd1d2c53892d2c0d28f0e9483597c8dab7`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:11 GMT
ADD file:3c88cea17de40599dc8b8da90adc8439635066835e930f9573ec6cc856c5c096 in / 
# Fri, 09 Dec 2022 01:20:12 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 04:21:18 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 09 Dec 2022 04:21:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 04:21:25 GMT
ENV JAVA_VERSION=8.0.7.20
# Fri, 09 Dec 2022 04:22:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 09 Dec 2022 04:22:24 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 09 Dec 2022 10:32:19 GMT
ARG VERBOSE=false
# Fri, 09 Dec 2022 10:32:19 GMT
ARG OPENJ9_SCC=true
# Fri, 09 Dec 2022 10:32:19 GMT
ARG EN_SHA=1e17d4aaf1fa467f73b9b8b81c1cb0ef2839ef5e9772cad5821e0322fb3f455a
# Fri, 09 Dec 2022 10:32:19 GMT
ARG NON_IBM_SHA=bb36c29ffe57a4cb5805d5cdcaa2594229e8caded88ec178aea3561fac30b06a
# Fri, 09 Dec 2022 10:32:19 GMT
ARG NOTICES_SHA=3f1afde6d12d56d4c96bb3005aa9f80c78089b9b358e952974fe1fad9f4cf3a4
# Fri, 09 Dec 2022 10:32:19 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=22.0.0.12 org.opencontainers.image.revision=cl221220221107-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 09 Dec 2022 10:32:19 GMT
ENV LIBERTY_VERSION=22.0.0_12
# Fri, 09 Dec 2022 10:32:19 GMT
ARG LIBERTY_URL
# Fri, 09 Dec 2022 10:32:19 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 09 Dec 2022 10:32:38 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1e17d4aaf1fa467f73b9b8b81c1cb0ef2839ef5e9772cad5821e0322fb3f455a NON_IBM_SHA=bb36c29ffe57a4cb5805d5cdcaa2594229e8caded88ec178aea3561fac30b06a NOTICES_SHA=3f1afde6d12d56d4c96bb3005aa9f80c78089b9b358e952974fe1fad9f4cf3a4 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 10:32:38 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 10:32:38 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=22.0.0.12 BuildLabel=cl221220221107-1900
# Fri, 09 Dec 2022 10:32:38 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 09 Dec 2022 10:32:40 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1e17d4aaf1fa467f73b9b8b81c1cb0ef2839ef5e9772cad5821e0322fb3f455a NON_IBM_SHA=bb36c29ffe57a4cb5805d5cdcaa2594229e8caded88ec178aea3561fac30b06a NOTICES_SHA=3f1afde6d12d56d4c96bb3005aa9f80c78089b9b358e952974fe1fad9f4cf3a4 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 09 Dec 2022 10:32:40 GMT
COPY dir:8bf844c49178cf63745af9ec643f57d70bd92c28166fabfad188dfc250d88353 in /opt/ibm/helpers/ 
# Fri, 09 Dec 2022 10:32:40 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 09 Dec 2022 10:32:41 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1e17d4aaf1fa467f73b9b8b81c1cb0ef2839ef5e9772cad5821e0322fb3f455a NON_IBM_SHA=bb36c29ffe57a4cb5805d5cdcaa2594229e8caded88ec178aea3561fac30b06a NOTICES_SHA=3f1afde6d12d56d4c96bb3005aa9f80c78089b9b358e952974fe1fad9f4cf3a4 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 09 Dec 2022 10:32:50 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1e17d4aaf1fa467f73b9b8b81c1cb0ef2839ef5e9772cad5821e0322fb3f455a NON_IBM_SHA=bb36c29ffe57a4cb5805d5cdcaa2594229e8caded88ec178aea3561fac30b06a NOTICES_SHA=3f1afde6d12d56d4c96bb3005aa9f80c78089b9b358e952974fe1fad9f4cf3a4 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 09 Dec 2022 10:32:50 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 09 Dec 2022 10:32:50 GMT
USER 1001
# Fri, 09 Dec 2022 10:32:50 GMT
EXPOSE 9080 9443
# Fri, 09 Dec 2022 10:32:50 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 09 Dec 2022 10:32:50 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 09 Dec 2022 10:33:49 GMT
ARG VERBOSE=false
# Fri, 09 Dec 2022 10:33:49 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 09 Dec 2022 10:42:28 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Fri, 09 Dec 2022 10:42:30 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 09 Dec 2022 10:43:00 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:fb668870d8a72b5d72a3b6d98ee626e00f9f7c29c6f4f7d3a63673d747dbffe7`  
		Last Modified: Fri, 09 Dec 2022 01:21:25 GMT  
		Size: 26.7 MB (26711459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acae8945e830b26864e6f4dcccac1c0f41145f5792c80fa11241789b45ce0c0`  
		Last Modified: Fri, 09 Dec 2022 04:24:50 GMT  
		Size: 2.9 MB (2949577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb0aaff24d2e9d944fe20d8d7b841c223905eed0cad23da4932cdc722436b29`  
		Last Modified: Fri, 09 Dec 2022 04:24:59 GMT  
		Size: 129.3 MB (129322664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c6789e5af14a95b78121e6f52ff57b9e4dbf07e97e10b8101dcdc35e0e0cf6`  
		Last Modified: Fri, 09 Dec 2022 11:29:27 GMT  
		Size: 14.3 MB (14275912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983bf7e34e5b9f5fb2207ae928bb898e1afa0159b9552fef658628bc6788ccd7`  
		Last Modified: Fri, 09 Dec 2022 11:29:23 GMT  
		Size: 678.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37189f9eef4c26d18d3e1c19d505a8bb8a13e7f1ffeb3012e854786fc4849b46`  
		Last Modified: Fri, 09 Dec 2022 11:29:23 GMT  
		Size: 9.8 KB (9757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53559deff1be045ba11e3ad22be12abcdf333964b1ab5f06d3c1c7726bccaabc`  
		Last Modified: Fri, 09 Dec 2022 11:29:23 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0adb63f50a0a058e4606d0150a49cf63db03fe2e3ef6c7d52df711ba621d8568`  
		Last Modified: Fri, 09 Dec 2022 11:29:23 GMT  
		Size: 10.7 KB (10738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c766c9247e2f7de6b2ea663a727123c9165827d6bea0431375ecb3a07e0e7f3f`  
		Last Modified: Fri, 09 Dec 2022 11:29:25 GMT  
		Size: 5.9 MB (5854650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ff95f289fe1179a43856b140c651faf086dbd27e06ce6936e88db0ba5fd565`  
		Last Modified: Fri, 09 Dec 2022 11:30:08 GMT  
		Size: 324.8 MB (324834622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0a8614fc6abb15393073499c536be5aafca2408dc690a25793d53042d2d1c8`  
		Last Modified: Fri, 09 Dec 2022 11:29:51 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae16009682c20dde61f4ac4358ad976bfd7f99306815798135ea31856fafb3eb`  
		Last Modified: Fri, 09 Dec 2022 11:29:54 GMT  
		Size: 15.9 MB (15888319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:55c22eed1210277f80801715f2f591e0f861ce14d997439610d2c45cb5b23c79
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.0 MB (520987613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30aab9b8c5bed8771f575e58d387f76d70f968a23195531789b8dd259a28c560`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 09 Dec 2022 01:27:15 GMT
ADD file:05ec256cb279f6d94111b2413d31c85c4e1ff1365bce34d2fc4aa2788885fa06 in / 
# Fri, 09 Dec 2022 01:27:17 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:02:12 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 09 Dec 2022 03:02:46 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 03:02:47 GMT
ENV JAVA_VERSION=8.0.7.20
# Fri, 09 Dec 2022 03:05:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 09 Dec 2022 03:05:19 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 09 Dec 2022 04:38:06 GMT
ARG VERBOSE=false
# Fri, 09 Dec 2022 04:38:07 GMT
ARG OPENJ9_SCC=true
# Fri, 09 Dec 2022 04:38:07 GMT
ARG EN_SHA=1e17d4aaf1fa467f73b9b8b81c1cb0ef2839ef5e9772cad5821e0322fb3f455a
# Fri, 09 Dec 2022 04:38:07 GMT
ARG NON_IBM_SHA=bb36c29ffe57a4cb5805d5cdcaa2594229e8caded88ec178aea3561fac30b06a
# Fri, 09 Dec 2022 04:38:08 GMT
ARG NOTICES_SHA=3f1afde6d12d56d4c96bb3005aa9f80c78089b9b358e952974fe1fad9f4cf3a4
# Fri, 09 Dec 2022 04:38:08 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=22.0.0.12 org.opencontainers.image.revision=cl221220221107-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 09 Dec 2022 04:38:08 GMT
ENV LIBERTY_VERSION=22.0.0_12
# Fri, 09 Dec 2022 04:38:09 GMT
ARG LIBERTY_URL
# Fri, 09 Dec 2022 04:38:09 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 09 Dec 2022 04:39:23 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1e17d4aaf1fa467f73b9b8b81c1cb0ef2839ef5e9772cad5821e0322fb3f455a NON_IBM_SHA=bb36c29ffe57a4cb5805d5cdcaa2594229e8caded88ec178aea3561fac30b06a NOTICES_SHA=3f1afde6d12d56d4c96bb3005aa9f80c78089b9b358e952974fe1fad9f4cf3a4 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 04:39:24 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 04:39:24 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=22.0.0.12 BuildLabel=cl221220221107-1900
# Fri, 09 Dec 2022 04:39:24 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 09 Dec 2022 04:39:26 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1e17d4aaf1fa467f73b9b8b81c1cb0ef2839ef5e9772cad5821e0322fb3f455a NON_IBM_SHA=bb36c29ffe57a4cb5805d5cdcaa2594229e8caded88ec178aea3561fac30b06a NOTICES_SHA=3f1afde6d12d56d4c96bb3005aa9f80c78089b9b358e952974fe1fad9f4cf3a4 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 09 Dec 2022 04:39:27 GMT
COPY dir:8bf844c49178cf63745af9ec643f57d70bd92c28166fabfad188dfc250d88353 in /opt/ibm/helpers/ 
# Fri, 09 Dec 2022 04:39:27 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 09 Dec 2022 04:39:29 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1e17d4aaf1fa467f73b9b8b81c1cb0ef2839ef5e9772cad5821e0322fb3f455a NON_IBM_SHA=bb36c29ffe57a4cb5805d5cdcaa2594229e8caded88ec178aea3561fac30b06a NOTICES_SHA=3f1afde6d12d56d4c96bb3005aa9f80c78089b9b358e952974fe1fad9f4cf3a4 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 09 Dec 2022 04:39:43 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1e17d4aaf1fa467f73b9b8b81c1cb0ef2839ef5e9772cad5821e0322fb3f455a NON_IBM_SHA=bb36c29ffe57a4cb5805d5cdcaa2594229e8caded88ec178aea3561fac30b06a NOTICES_SHA=3f1afde6d12d56d4c96bb3005aa9f80c78089b9b358e952974fe1fad9f4cf3a4 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 09 Dec 2022 04:39:44 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 09 Dec 2022 04:39:44 GMT
USER 1001
# Fri, 09 Dec 2022 04:39:44 GMT
EXPOSE 9080 9443
# Fri, 09 Dec 2022 04:39:45 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 09 Dec 2022 04:39:45 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 09 Dec 2022 04:42:38 GMT
ARG VERBOSE=false
# Fri, 09 Dec 2022 04:42:39 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 09 Dec 2022 04:59:19 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Fri, 09 Dec 2022 04:59:24 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 09 Dec 2022 05:00:19 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:29d5a8bf9800ea1d873fe104fc2b0b6d4efed1269ce0f9a80e4d65e96d3246e2`  
		Last Modified: Fri, 09 Dec 2022 01:29:45 GMT  
		Size: 30.4 MB (30442475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b911794ae1ce4902a6daaf989e919ecf0eec34798ddaf26f80408d03d5779c`  
		Last Modified: Fri, 09 Dec 2022 03:10:49 GMT  
		Size: 3.1 MB (3075733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103bba608e4bcf78845fbe100e090c5cbdd4d12ecd86a1d8aaab5fb5d5778837`  
		Last Modified: Fri, 09 Dec 2022 03:11:06 GMT  
		Size: 129.0 MB (128996365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b0c68b578a40ea292adba62964695582d368b92198c14d6268281edd9713949`  
		Last Modified: Fri, 09 Dec 2022 06:27:03 GMT  
		Size: 14.3 MB (14276244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf9f637786cc18aeccadbb55dc47babbbe7981226086129109d4f0e9ee14c42`  
		Last Modified: Fri, 09 Dec 2022 06:26:58 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c351ddb30f5c266ad417754192ccbfd5631bb4757b0ac15ec40b5fa341fabdc3`  
		Last Modified: Fri, 09 Dec 2022 06:26:58 GMT  
		Size: 9.8 KB (9758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fcc93dcbd50d26fc703d3e6e4ac3f4dc00c13fa8b44be4f0a79cc0f8190eac`  
		Last Modified: Fri, 09 Dec 2022 06:26:58 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7902f0a9beb5f8a142ef0749a98a0aa4835504fd4f56f66b3fb059c66f06179`  
		Last Modified: Fri, 09 Dec 2022 06:26:58 GMT  
		Size: 10.7 KB (10733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64ab1a25fa2723f05f4d7958ec32f63b08178ccf7858ccac149689eda3283f6`  
		Last Modified: Fri, 09 Dec 2022 06:26:59 GMT  
		Size: 5.5 MB (5487309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f23d454f06360ff3edd15ba5b72ec8552591abdaedb0ef7436272ebba19876b`  
		Last Modified: Fri, 09 Dec 2022 06:28:04 GMT  
		Size: 324.8 MB (324835104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5d4ea6eff120492a96e3c2185c5d75794f31f10c37e6794823cf141a294a84`  
		Last Modified: Fri, 09 Dec 2022 06:27:34 GMT  
		Size: 951.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1bfd44f5806f0f6dd7424965e6538f50e9661430d5cc425e58d1cee8265636`  
		Last Modified: Fri, 09 Dec 2022 06:27:38 GMT  
		Size: 13.9 MB (13851979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:5fd2c1f0d61a5780dd2f15206d8cf03f5d2ea636d9702dca954ad8eb90ee1142
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.6 MB (515614429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1b0a389a67120c7b6c6a44662b480a821f7177bff7914966314266fb07b4c22`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 09 Dec 2022 01:52:21 GMT
ADD file:c2fcdae7883d865c232dfc26d514c111189f6940ba74273c78067624cd02c962 in / 
# Fri, 09 Dec 2022 01:52:24 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:15:50 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 09 Dec 2022 03:16:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 03:16:12 GMT
ENV JAVA_VERSION=8.0.7.20
# Fri, 09 Dec 2022 03:17:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 09 Dec 2022 03:17:19 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 09 Dec 2022 05:30:43 GMT
ARG VERBOSE=false
# Fri, 09 Dec 2022 05:30:44 GMT
ARG OPENJ9_SCC=true
# Fri, 09 Dec 2022 05:30:44 GMT
ARG EN_SHA=1e17d4aaf1fa467f73b9b8b81c1cb0ef2839ef5e9772cad5821e0322fb3f455a
# Fri, 09 Dec 2022 05:30:45 GMT
ARG NON_IBM_SHA=bb36c29ffe57a4cb5805d5cdcaa2594229e8caded88ec178aea3561fac30b06a
# Fri, 09 Dec 2022 05:30:46 GMT
ARG NOTICES_SHA=3f1afde6d12d56d4c96bb3005aa9f80c78089b9b358e952974fe1fad9f4cf3a4
# Fri, 09 Dec 2022 05:30:46 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=22.0.0.12 org.opencontainers.image.revision=cl221220221107-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 09 Dec 2022 05:30:47 GMT
ENV LIBERTY_VERSION=22.0.0_12
# Fri, 09 Dec 2022 05:30:47 GMT
ARG LIBERTY_URL
# Fri, 09 Dec 2022 05:30:48 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 09 Dec 2022 05:31:01 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1e17d4aaf1fa467f73b9b8b81c1cb0ef2839ef5e9772cad5821e0322fb3f455a NON_IBM_SHA=bb36c29ffe57a4cb5805d5cdcaa2594229e8caded88ec178aea3561fac30b06a NOTICES_SHA=3f1afde6d12d56d4c96bb3005aa9f80c78089b9b358e952974fe1fad9f4cf3a4 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 05:31:01 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 05:31:01 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=22.0.0.12 BuildLabel=cl221220221107-1900
# Fri, 09 Dec 2022 05:31:02 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 09 Dec 2022 05:31:03 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1e17d4aaf1fa467f73b9b8b81c1cb0ef2839ef5e9772cad5821e0322fb3f455a NON_IBM_SHA=bb36c29ffe57a4cb5805d5cdcaa2594229e8caded88ec178aea3561fac30b06a NOTICES_SHA=3f1afde6d12d56d4c96bb3005aa9f80c78089b9b358e952974fe1fad9f4cf3a4 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 09 Dec 2022 05:31:04 GMT
COPY dir:8bf844c49178cf63745af9ec643f57d70bd92c28166fabfad188dfc250d88353 in /opt/ibm/helpers/ 
# Fri, 09 Dec 2022 05:31:04 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 09 Dec 2022 05:31:04 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1e17d4aaf1fa467f73b9b8b81c1cb0ef2839ef5e9772cad5821e0322fb3f455a NON_IBM_SHA=bb36c29ffe57a4cb5805d5cdcaa2594229e8caded88ec178aea3561fac30b06a NOTICES_SHA=3f1afde6d12d56d4c96bb3005aa9f80c78089b9b358e952974fe1fad9f4cf3a4 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 09 Dec 2022 05:31:13 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1e17d4aaf1fa467f73b9b8b81c1cb0ef2839ef5e9772cad5821e0322fb3f455a NON_IBM_SHA=bb36c29ffe57a4cb5805d5cdcaa2594229e8caded88ec178aea3561fac30b06a NOTICES_SHA=3f1afde6d12d56d4c96bb3005aa9f80c78089b9b358e952974fe1fad9f4cf3a4 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 09 Dec 2022 05:31:13 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 09 Dec 2022 05:31:13 GMT
USER 1001
# Fri, 09 Dec 2022 05:31:13 GMT
EXPOSE 9080 9443
# Fri, 09 Dec 2022 05:31:13 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 09 Dec 2022 05:31:13 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 09 Dec 2022 05:32:14 GMT
ARG VERBOSE=false
# Fri, 09 Dec 2022 05:32:14 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 09 Dec 2022 05:39:43 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Fri, 09 Dec 2022 05:39:50 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 09 Dec 2022 05:40:18 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:3fb013d46f2fda49d6c671f39f55c3330f927a4c55ae7e5096daf0a638dc38ec`  
		Last Modified: Fri, 09 Dec 2022 01:54:45 GMT  
		Size: 25.4 MB (25371298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49e7e6835b120e4486c693b4f03bdf01ba76a250b74306406b7bd9fbb2d737c`  
		Last Modified: Fri, 09 Dec 2022 03:20:23 GMT  
		Size: 2.7 MB (2667341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fdd86aa56415e723ad1c625e8e84de704bd93370cb5380694e05e888e84210`  
		Last Modified: Fri, 09 Dec 2022 03:20:31 GMT  
		Size: 126.5 MB (126472625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a7bde17aa505ab16a065efbfb8e62bc82319f848c14150a142f3ef56e46a8d`  
		Last Modified: Fri, 09 Dec 2022 06:23:14 GMT  
		Size: 14.3 MB (14275976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d419e336e22abe179ad3f5c89125f3bd92c52d731eb3437505451a95a2d3cd5`  
		Last Modified: Fri, 09 Dec 2022 06:23:12 GMT  
		Size: 678.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a34f9d216b664a1be3cd1d6f7a4d6ba51bb8fa3a6d575714b6c296b08574fbf`  
		Last Modified: Fri, 09 Dec 2022 06:23:12 GMT  
		Size: 9.8 KB (9763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df3e9a432697476c52e593d3ba83adddfcce3b2caeff27d32ddb865f4ce123c`  
		Last Modified: Fri, 09 Dec 2022 06:23:12 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a2737c03e341378ab89cdeb8b5579d7dc55546a3eb9a6083022c1b428b3d1d`  
		Last Modified: Fri, 09 Dec 2022 06:23:12 GMT  
		Size: 10.7 KB (10733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b98b6b8df8341406ca3d89521987463ade3be86fcf059667f7a96145e271fa`  
		Last Modified: Fri, 09 Dec 2022 06:23:13 GMT  
		Size: 6.1 MB (6104893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb45dad892d375ac829a9266e91e38d8e12407d147fc31a2e39b0179ae5650b`  
		Last Modified: Fri, 09 Dec 2022 06:23:45 GMT  
		Size: 324.8 MB (324834066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edeed3adfa34135b9f80913751b236d54b7c83a90eef08543a683516f152240`  
		Last Modified: Fri, 09 Dec 2022 06:23:31 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:714580b3205a1b54624a76cb1c07e7f8fde7c0a7f019c2edb3c8885c841c978b`  
		Last Modified: Fri, 09 Dec 2022 06:23:33 GMT  
		Size: 15.9 MB (15865835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
