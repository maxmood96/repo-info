## `websphere-liberty:full`

```console
$ docker pull websphere-liberty@sha256:d20f4c9a1b566bdd83ba20ae66018a08d6120009d06f80cd0381f29d10260b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:full` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:abf074ece8a99d4149dfff127714e276d4ab367f07af85a6821abb8deb6df58c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.0 MB (526034946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b9ca401decfee21b4a47cdc146d9e55fcc8fc144df3895d79823bcab68be1a`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Fri, 31 Mar 2023 22:19:33 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 31 Mar 2023 22:19:41 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 31 Mar 2023 22:19:41 GMT
ENV JAVA_VERSION=8.0.8.0
# Fri, 31 Mar 2023 22:20:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='39cf0ebeda2461c0ee81636d745643713a37863d729784c46a48b4eded4717fb';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bef3e93e4b1025e8350492fed0f6a5a743a2d35fbacdb7820cc539d24c891a4e';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='87d22ee3d2e20faa9854044aa46bf6be5d39f8ceb9ccf91574c7518f2535dfcb';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='227ada7516542c170a920bc78a416c1dc492cba4321a23f42bd7e640ddc890e5';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 31 Mar 2023 22:20:41 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 31 Mar 2023 22:41:18 GMT
ARG VERBOSE=false
# Fri, 31 Mar 2023 22:41:18 GMT
ARG OPENJ9_SCC=true
# Fri, 31 Mar 2023 22:41:18 GMT
ARG EN_SHA=2d77600f393a32877305f82957968c41d1e140ad4ebd3a2c07f5d77f601d5614
# Fri, 31 Mar 2023 22:41:18 GMT
ARG NON_IBM_SHA=565db37df01346ca4f611c4fc58431e845f1c4002908e1a4c696230d7f396d9c
# Fri, 31 Mar 2023 22:41:19 GMT
ARG NOTICES_SHA=c08df1e3fdf99be6f02fcf458e4533119a4785a92994d5950528f02f349ada4b
# Fri, 31 Mar 2023 22:41:19 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=23.0.0.2 org.opencontainers.image.revision=cl230220230222-1257 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 31 Mar 2023 22:41:19 GMT
ENV LIBERTY_VERSION=23.0.0_2
# Fri, 31 Mar 2023 22:41:19 GMT
ARG LIBERTY_URL
# Fri, 31 Mar 2023 22:41:19 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 31 Mar 2023 22:41:34 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2d77600f393a32877305f82957968c41d1e140ad4ebd3a2c07f5d77f601d5614 NON_IBM_SHA=565db37df01346ca4f611c4fc58431e845f1c4002908e1a4c696230d7f396d9c NOTICES_SHA=c08df1e3fdf99be6f02fcf458e4533119a4785a92994d5950528f02f349ada4b OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 31 Mar 2023 22:41:34 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Fri, 31 Mar 2023 22:41:34 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=23.0.0.2 BuildLabel=cl230220230222-1257
# Fri, 31 Mar 2023 22:41:34 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 31 Mar 2023 22:41:35 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2d77600f393a32877305f82957968c41d1e140ad4ebd3a2c07f5d77f601d5614 NON_IBM_SHA=565db37df01346ca4f611c4fc58431e845f1c4002908e1a4c696230d7f396d9c NOTICES_SHA=c08df1e3fdf99be6f02fcf458e4533119a4785a92994d5950528f02f349ada4b VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 31 Mar 2023 22:41:35 GMT
COPY dir:0f3e336b1e5adb84a625050153035561e1c9802a57b7b90b5a17ebb82adba489 in /opt/ibm/helpers/ 
# Fri, 31 Mar 2023 22:41:35 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 31 Mar 2023 22:41:36 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2d77600f393a32877305f82957968c41d1e140ad4ebd3a2c07f5d77f601d5614 NON_IBM_SHA=565db37df01346ca4f611c4fc58431e845f1c4002908e1a4c696230d7f396d9c NOTICES_SHA=c08df1e3fdf99be6f02fcf458e4533119a4785a92994d5950528f02f349ada4b VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 31 Mar 2023 22:41:43 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2d77600f393a32877305f82957968c41d1e140ad4ebd3a2c07f5d77f601d5614 NON_IBM_SHA=565db37df01346ca4f611c4fc58431e845f1c4002908e1a4c696230d7f396d9c NOTICES_SHA=c08df1e3fdf99be6f02fcf458e4533119a4785a92994d5950528f02f349ada4b VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 31 Mar 2023 22:41:43 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 31 Mar 2023 22:41:43 GMT
USER 1001
# Fri, 31 Mar 2023 22:41:43 GMT
EXPOSE 9080 9443
# Fri, 31 Mar 2023 22:41:43 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 31 Mar 2023 22:41:43 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 31 Mar 2023 22:41:49 GMT
ARG VERBOSE=false
# Fri, 31 Mar 2023 22:41:50 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 31 Mar 2023 22:50:02 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Fri, 31 Mar 2023 22:50:03 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 31 Mar 2023 22:50:32 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76592b838d832d2f6a0e0691d8d3efa85fffa35e81c119bed83fd87227183a5f`  
		Last Modified: Fri, 31 Mar 2023 22:23:03 GMT  
		Size: 1.4 MB (1446443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6a8364e7523c158c9be9f157f3cfc1f1c1330d1346c1eed379cda08e2607e7`  
		Last Modified: Fri, 31 Mar 2023 22:23:12 GMT  
		Size: 133.9 MB (133853339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf9be7239e4d712e9a1c2742df36e36cc6d3d328dc8282ef23c2498e1fa4c704`  
		Last Modified: Fri, 31 Mar 2023 23:09:56 GMT  
		Size: 14.3 MB (14342888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83851d26d039bd3c7e2860ea8870efe201c430b51884b18c8a7de17f99865516`  
		Last Modified: Fri, 31 Mar 2023 23:09:53 GMT  
		Size: 681.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3499e134de4195664ab2231d4634adcd5f15629c324fb66cfcffc768f0750c`  
		Last Modified: Fri, 31 Mar 2023 23:09:53 GMT  
		Size: 9.8 KB (9817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0edf0096c25db415a679ff7ffad9ed689ac4c23782867bc718a83db77071371`  
		Last Modified: Fri, 31 Mar 2023 23:09:53 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66916a6a7b342c5d23b06abf2d9012c93cbea38d99f8b2b125794ca84760f383`  
		Last Modified: Fri, 31 Mar 2023 23:09:53 GMT  
		Size: 10.8 KB (10799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf292763d2fd46296287d848b1329495c41beca87d71af41e0d3ca9118af24c`  
		Last Modified: Fri, 31 Mar 2023 23:09:54 GMT  
		Size: 5.8 MB (5841391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5af52f19821fc6f04f93c126a632c43daa6d15f322a63fa8886eaa3b541ba8e`  
		Last Modified: Fri, 31 Mar 2023 23:10:18 GMT  
		Size: 324.0 MB (324040706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51874a14fb4c73bd862d8b5cb8b1bd16978cc5859f516d25d2003d5e780e6cd`  
		Last Modified: Fri, 31 Mar 2023 23:10:03 GMT  
		Size: 945.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16a9e1f4ace249fa3a5bf14521be1575265a256276d54c30ab50d58d864df6e`  
		Last Modified: Fri, 31 Mar 2023 23:10:05 GMT  
		Size: 16.1 MB (16057702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:d6915ff325a228fe736919d6066a9946bf2879fbb29c91b3e5989c35f0962c6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.7 MB (528689684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c0ca316614e282a0761b264c765a74fb690f2909e739c7a6b3d228cd5c64752`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:16 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:20 GMT
ADD file:d7434a52d8d8aa6288e788f6fe7e156f0e11bf9b8275efaf70aab0bfc4d919cf in / 
# Wed, 08 Mar 2023 04:39:20 GMT
CMD ["/bin/bash"]
# Fri, 31 Mar 2023 22:21:07 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 31 Mar 2023 22:21:31 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 31 Mar 2023 22:21:31 GMT
ENV JAVA_VERSION=8.0.8.0
# Fri, 31 Mar 2023 22:24:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='39cf0ebeda2461c0ee81636d745643713a37863d729784c46a48b4eded4717fb';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bef3e93e4b1025e8350492fed0f6a5a743a2d35fbacdb7820cc539d24c891a4e';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='87d22ee3d2e20faa9854044aa46bf6be5d39f8ceb9ccf91574c7518f2535dfcb';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='227ada7516542c170a920bc78a416c1dc492cba4321a23f42bd7e640ddc890e5';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 31 Mar 2023 22:24:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 31 Mar 2023 22:48:26 GMT
ARG VERBOSE=false
# Fri, 31 Mar 2023 22:48:26 GMT
ARG OPENJ9_SCC=true
# Fri, 31 Mar 2023 22:48:27 GMT
ARG EN_SHA=2d77600f393a32877305f82957968c41d1e140ad4ebd3a2c07f5d77f601d5614
# Fri, 31 Mar 2023 22:48:27 GMT
ARG NON_IBM_SHA=565db37df01346ca4f611c4fc58431e845f1c4002908e1a4c696230d7f396d9c
# Fri, 31 Mar 2023 22:48:28 GMT
ARG NOTICES_SHA=c08df1e3fdf99be6f02fcf458e4533119a4785a92994d5950528f02f349ada4b
# Fri, 31 Mar 2023 22:48:28 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=23.0.0.2 org.opencontainers.image.revision=cl230220230222-1257 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 31 Mar 2023 22:48:28 GMT
ENV LIBERTY_VERSION=23.0.0_2
# Fri, 31 Mar 2023 22:48:29 GMT
ARG LIBERTY_URL
# Fri, 31 Mar 2023 22:48:29 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 31 Mar 2023 22:49:00 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2d77600f393a32877305f82957968c41d1e140ad4ebd3a2c07f5d77f601d5614 NON_IBM_SHA=565db37df01346ca4f611c4fc58431e845f1c4002908e1a4c696230d7f396d9c NOTICES_SHA=c08df1e3fdf99be6f02fcf458e4533119a4785a92994d5950528f02f349ada4b OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 31 Mar 2023 22:49:01 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Fri, 31 Mar 2023 22:49:01 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=23.0.0.2 BuildLabel=cl230220230222-1257
# Fri, 31 Mar 2023 22:49:02 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 31 Mar 2023 22:49:04 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2d77600f393a32877305f82957968c41d1e140ad4ebd3a2c07f5d77f601d5614 NON_IBM_SHA=565db37df01346ca4f611c4fc58431e845f1c4002908e1a4c696230d7f396d9c NOTICES_SHA=c08df1e3fdf99be6f02fcf458e4533119a4785a92994d5950528f02f349ada4b VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 31 Mar 2023 22:49:04 GMT
COPY dir:0f3e336b1e5adb84a625050153035561e1c9802a57b7b90b5a17ebb82adba489 in /opt/ibm/helpers/ 
# Fri, 31 Mar 2023 22:49:04 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 31 Mar 2023 22:49:06 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2d77600f393a32877305f82957968c41d1e140ad4ebd3a2c07f5d77f601d5614 NON_IBM_SHA=565db37df01346ca4f611c4fc58431e845f1c4002908e1a4c696230d7f396d9c NOTICES_SHA=c08df1e3fdf99be6f02fcf458e4533119a4785a92994d5950528f02f349ada4b VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 31 Mar 2023 22:49:19 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2d77600f393a32877305f82957968c41d1e140ad4ebd3a2c07f5d77f601d5614 NON_IBM_SHA=565db37df01346ca4f611c4fc58431e845f1c4002908e1a4c696230d7f396d9c NOTICES_SHA=c08df1e3fdf99be6f02fcf458e4533119a4785a92994d5950528f02f349ada4b VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 31 Mar 2023 22:49:20 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 31 Mar 2023 22:49:20 GMT
USER 1001
# Fri, 31 Mar 2023 22:49:21 GMT
EXPOSE 9080 9443
# Fri, 31 Mar 2023 22:49:22 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 31 Mar 2023 22:49:22 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 31 Mar 2023 22:49:29 GMT
ARG VERBOSE=false
# Fri, 31 Mar 2023 22:49:30 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 31 Mar 2023 23:05:37 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Fri, 31 Mar 2023 23:05:39 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 31 Mar 2023 23:06:37 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:deffc758660db3b0ee7a1f211d720633f06f27ab1e4c31db4caf8c27f4a80eeb`  
		Last Modified: Thu, 16 Mar 2023 02:22:27 GMT  
		Size: 35.7 MB (35711728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edde4d0991b2fc61228d445220b004d843c08e4eb5f5dba26f3e2f7edaf14848`  
		Last Modified: Fri, 31 Mar 2023 22:29:44 GMT  
		Size: 1.6 MB (1552384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131d0f08b83cbc1ee206685d06deab38a4588725489739b0c7295ec5734c21db`  
		Last Modified: Fri, 31 Mar 2023 22:30:01 GMT  
		Size: 133.6 MB (133555981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd93a68c304219f54655d16e82265626635ced25771a093cb944d1e3bb754733`  
		Last Modified: Fri, 31 Mar 2023 23:41:50 GMT  
		Size: 14.3 MB (14343464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b9c6f9b70250acf3de2eed3b9ee7723cfca9c9c211f8368575d06f062e4644`  
		Last Modified: Fri, 31 Mar 2023 23:41:45 GMT  
		Size: 681.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435f4768569b7904cf6e80d7f0e589496bbf0aa24c13dbc270940d6be48ea4d0`  
		Last Modified: Fri, 31 Mar 2023 23:41:45 GMT  
		Size: 9.8 KB (9816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0cf81ac063301d361c5d7abb2d1132569a4608dc473d797edc0d8987a25771`  
		Last Modified: Fri, 31 Mar 2023 23:41:45 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1077a7021ef4daa3642fbb332d46b70e6d706821c39c66612f41503c149211b3`  
		Last Modified: Fri, 31 Mar 2023 23:41:45 GMT  
		Size: 10.8 KB (10803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1645e5b06801a6b92248a392bab90825d05f14aea7e06a91b924ebe75aa1bb0f`  
		Last Modified: Fri, 31 Mar 2023 23:41:47 GMT  
		Size: 5.5 MB (5504702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feea42137c227a572f3809cb7a80cb04ed486b945b30f0b21d58f7875279db5d`  
		Last Modified: Fri, 31 Mar 2023 23:42:23 GMT  
		Size: 324.0 MB (324041899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46f18f96ec4827a0a915bdbb35764fba01ff4ddef0d82582fb60d269cc7800f`  
		Last Modified: Fri, 31 Mar 2023 23:41:57 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91185104307929c4405da969afb1edd7772c343a7b9f43d7061e691caf9b5694`  
		Last Modified: Fri, 31 Mar 2023 23:42:00 GMT  
		Size: 14.0 MB (13957005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:c7089ed490938f4fba3989c63a48269d5a3268261ff3206ec286ec601bdc5054
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.1 MB (521051588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4bb569ec84b96433dec75b2344effb94377181f61da0afcc0f55fdc18237884`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:24 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:26 GMT
ADD file:630f9865d3d4fd4294d45cac7cbaea83fb549c2e563de454348da964d19fbbba in / 
# Wed, 08 Mar 2023 04:39:26 GMT
CMD ["/bin/bash"]
# Fri, 31 Mar 2023 21:42:09 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 31 Mar 2023 21:42:22 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 31 Mar 2023 21:42:22 GMT
ENV JAVA_VERSION=8.0.8.0
# Fri, 31 Mar 2023 21:43:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='39cf0ebeda2461c0ee81636d745643713a37863d729784c46a48b4eded4717fb';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bef3e93e4b1025e8350492fed0f6a5a743a2d35fbacdb7820cc539d24c891a4e';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='87d22ee3d2e20faa9854044aa46bf6be5d39f8ceb9ccf91574c7518f2535dfcb';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='227ada7516542c170a920bc78a416c1dc492cba4321a23f42bd7e640ddc890e5';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 31 Mar 2023 21:43:12 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 31 Mar 2023 22:03:17 GMT
ARG VERBOSE=false
# Fri, 31 Mar 2023 22:03:18 GMT
ARG OPENJ9_SCC=true
# Fri, 31 Mar 2023 22:03:18 GMT
ARG EN_SHA=2d77600f393a32877305f82957968c41d1e140ad4ebd3a2c07f5d77f601d5614
# Fri, 31 Mar 2023 22:03:18 GMT
ARG NON_IBM_SHA=565db37df01346ca4f611c4fc58431e845f1c4002908e1a4c696230d7f396d9c
# Fri, 31 Mar 2023 22:03:18 GMT
ARG NOTICES_SHA=c08df1e3fdf99be6f02fcf458e4533119a4785a92994d5950528f02f349ada4b
# Fri, 31 Mar 2023 22:03:18 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=23.0.0.2 org.opencontainers.image.revision=cl230220230222-1257 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 31 Mar 2023 22:03:18 GMT
ENV LIBERTY_VERSION=23.0.0_2
# Fri, 31 Mar 2023 22:03:19 GMT
ARG LIBERTY_URL
# Fri, 31 Mar 2023 22:03:19 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 31 Mar 2023 22:03:33 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2d77600f393a32877305f82957968c41d1e140ad4ebd3a2c07f5d77f601d5614 NON_IBM_SHA=565db37df01346ca4f611c4fc58431e845f1c4002908e1a4c696230d7f396d9c NOTICES_SHA=c08df1e3fdf99be6f02fcf458e4533119a4785a92994d5950528f02f349ada4b OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 31 Mar 2023 22:03:34 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Fri, 31 Mar 2023 22:03:34 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=23.0.0.2 BuildLabel=cl230220230222-1257
# Fri, 31 Mar 2023 22:03:34 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 31 Mar 2023 22:03:35 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2d77600f393a32877305f82957968c41d1e140ad4ebd3a2c07f5d77f601d5614 NON_IBM_SHA=565db37df01346ca4f611c4fc58431e845f1c4002908e1a4c696230d7f396d9c NOTICES_SHA=c08df1e3fdf99be6f02fcf458e4533119a4785a92994d5950528f02f349ada4b VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 31 Mar 2023 22:03:35 GMT
COPY dir:0f3e336b1e5adb84a625050153035561e1c9802a57b7b90b5a17ebb82adba489 in /opt/ibm/helpers/ 
# Fri, 31 Mar 2023 22:03:35 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 31 Mar 2023 22:03:35 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2d77600f393a32877305f82957968c41d1e140ad4ebd3a2c07f5d77f601d5614 NON_IBM_SHA=565db37df01346ca4f611c4fc58431e845f1c4002908e1a4c696230d7f396d9c NOTICES_SHA=c08df1e3fdf99be6f02fcf458e4533119a4785a92994d5950528f02f349ada4b VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 31 Mar 2023 22:03:41 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2d77600f393a32877305f82957968c41d1e140ad4ebd3a2c07f5d77f601d5614 NON_IBM_SHA=565db37df01346ca4f611c4fc58431e845f1c4002908e1a4c696230d7f396d9c NOTICES_SHA=c08df1e3fdf99be6f02fcf458e4533119a4785a92994d5950528f02f349ada4b VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 31 Mar 2023 22:03:42 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 31 Mar 2023 22:03:42 GMT
USER 1001
# Fri, 31 Mar 2023 22:03:42 GMT
EXPOSE 9080 9443
# Fri, 31 Mar 2023 22:03:42 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 31 Mar 2023 22:03:42 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 31 Mar 2023 22:03:56 GMT
ARG VERBOSE=false
# Fri, 31 Mar 2023 22:03:56 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 31 Mar 2023 22:16:05 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Fri, 31 Mar 2023 22:16:12 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 31 Mar 2023 22:16:35 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:2c7366af510b72cc0b3456fb93cfa0bfc76f7d383db5cb315967e7b1ce2e0c42`  
		Last Modified: Thu, 16 Mar 2023 02:02:40 GMT  
		Size: 28.6 MB (28647599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e458936873e72c656dd508c3163aeef4a5e866071e6fc64d093fee431ee1683`  
		Last Modified: Fri, 31 Mar 2023 21:45:26 GMT  
		Size: 1.5 MB (1452441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8404bcd692b90ddc679ed6235e935f46248daa910b7a28c6f4650a6438eccda9`  
		Last Modified: Fri, 31 Mar 2023 21:45:34 GMT  
		Size: 130.7 MB (130656029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab350c23be089ffe27e99b3b8bdcf5ec0fecf26cf5be0281fcb210e30ae489b`  
		Last Modified: Fri, 31 Mar 2023 22:37:07 GMT  
		Size: 14.3 MB (14343145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e4972a6959041d8e7edf73dc5bf2d18f3a9481c5a37063683d567e3469b950`  
		Last Modified: Fri, 31 Mar 2023 22:37:05 GMT  
		Size: 677.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1908efc2efbbe8c97f48f6b74a329f16ecda797e25115079b03a14a1f6967d`  
		Last Modified: Fri, 31 Mar 2023 22:37:05 GMT  
		Size: 9.8 KB (9814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e324b268675b61f69168ba6f8564c6f78db22d29b9a79b1e4a41db62d72ca4ca`  
		Last Modified: Fri, 31 Mar 2023 22:37:04 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5433a0426929770211057bd41df3977075c9ba3ddb854e33cd307051fb8efc`  
		Last Modified: Fri, 31 Mar 2023 22:37:05 GMT  
		Size: 10.8 KB (10793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf73c7d95f7e3e3167bf48cf378b18ba6bf96c9466dc7b5455cf6e20adf9ce7`  
		Last Modified: Fri, 31 Mar 2023 22:37:05 GMT  
		Size: 6.0 MB (5968797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fe5576529ea3160fb2304099dc120b38a5f4ebad1963ab8e3a1072c816826d`  
		Last Modified: Fri, 31 Mar 2023 22:37:24 GMT  
		Size: 324.0 MB (324041470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e75543ef72c54b7fe63a8aefa669d43752189fd80dd10310a46045150db495`  
		Last Modified: Fri, 31 Mar 2023 22:37:11 GMT  
		Size: 947.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6079e19fd7e85d7ff8aa67e4ac4ad0a1ad8e2c664c151914b7b4f3c53d0e21f`  
		Last Modified: Fri, 31 Mar 2023 22:37:12 GMT  
		Size: 15.9 MB (15919604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
