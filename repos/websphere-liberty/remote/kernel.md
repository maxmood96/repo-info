## `websphere-liberty:kernel`

```console
$ docker pull websphere-liberty@sha256:8491059d2dca81b049a8591ffd9903a2f7d806f89282c49ae0e80e2e72b5dc9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:kernel` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:4e9113fd7f10f679efae6e02e12b2599576c720e4241ad3d04ef435fc7ce047f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179133882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4c3e8434fa16e852cec77ad674ee4a6e30329a9fad11da138aef875782c01a`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:28 GMT
ADD file:fc5d658c47ede58827812b75a311353be776e41e2dd339b8906839527c9b5247 in / 
# Tue, 25 Oct 2022 01:53:28 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 16:56:49 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 25 Oct 2022 16:56:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 16:56:58 GMT
ENV JAVA_VERSION=8.0.7.16
# Tue, 25 Oct 2022 16:57:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='70b5592485b0188b421cb0a072e913e3f93dfebcbc63096651258b622f19e710';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='2cf9c65de9a8dce78ebb4403b0d83a173cda3b3b5064ce5f6f63236f89e607c0';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='eaae9e57e497ab9850203384a373a473f0d8648b02c1de5c1e01af14794c5af9';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='aa301e7f2fa12ba5b3c2183674d232e8942fd6061ea2efa589d1f404969d810b';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='e091ac9b24b35f1c6cf28f3fb494e3643841bc7949c28bf6899bc384ef547ba7';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 25 Oct 2022 16:57:57 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 26 Oct 2022 19:34:36 GMT
ARG VERBOSE=false
# Wed, 26 Oct 2022 19:34:36 GMT
ARG OPENJ9_SCC=true
# Tue, 15 Nov 2022 03:23:22 GMT
ARG EN_SHA=1ce31500fa2422ed1410137cd50d33e18cf42ad0ae0b5a3e545183ae801869e0
# Tue, 15 Nov 2022 03:23:22 GMT
ARG NON_IBM_SHA=1f032aeb46b5f5f4262f123cb2339230e2755cac039cb1bf0285cbb0f37fe7c8
# Tue, 15 Nov 2022 03:23:22 GMT
ARG NOTICES_SHA=46056efcb4c0e11e1cc9a33104c4d2ae9b42d566ec74885804914c4eb41ef2ec
# Tue, 15 Nov 2022 03:23:22 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=22.0.0.11 org.opencontainers.image.revision=cl221120221010-1540 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Tue, 15 Nov 2022 03:23:22 GMT
ENV LIBERTY_VERSION=22.0.0_11
# Tue, 15 Nov 2022 03:23:22 GMT
ARG LIBERTY_URL
# Tue, 15 Nov 2022 03:23:23 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 15 Nov 2022 03:23:41 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ce31500fa2422ed1410137cd50d33e18cf42ad0ae0b5a3e545183ae801869e0 NON_IBM_SHA=1f032aeb46b5f5f4262f123cb2339230e2755cac039cb1bf0285cbb0f37fe7c8 NOTICES_SHA=46056efcb4c0e11e1cc9a33104c4d2ae9b42d566ec74885804914c4eb41ef2ec OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 03:23:41 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 03:23:41 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=22.0.0.11 BuildLabel=cl221120221010-1540
# Tue, 15 Nov 2022 03:23:41 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 15 Nov 2022 03:23:43 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ce31500fa2422ed1410137cd50d33e18cf42ad0ae0b5a3e545183ae801869e0 NON_IBM_SHA=1f032aeb46b5f5f4262f123cb2339230e2755cac039cb1bf0285cbb0f37fe7c8 NOTICES_SHA=46056efcb4c0e11e1cc9a33104c4d2ae9b42d566ec74885804914c4eb41ef2ec VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Tue, 15 Nov 2022 03:23:43 GMT
COPY dir:8bf844c49178cf63745af9ec643f57d70bd92c28166fabfad188dfc250d88353 in /opt/ibm/helpers/ 
# Tue, 15 Nov 2022 03:23:43 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Tue, 15 Nov 2022 03:23:44 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ce31500fa2422ed1410137cd50d33e18cf42ad0ae0b5a3e545183ae801869e0 NON_IBM_SHA=1f032aeb46b5f5f4262f123cb2339230e2755cac039cb1bf0285cbb0f37fe7c8 NOTICES_SHA=46056efcb4c0e11e1cc9a33104c4d2ae9b42d566ec74885804914c4eb41ef2ec VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Tue, 15 Nov 2022 03:23:53 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ce31500fa2422ed1410137cd50d33e18cf42ad0ae0b5a3e545183ae801869e0 NON_IBM_SHA=1f032aeb46b5f5f4262f123cb2339230e2755cac039cb1bf0285cbb0f37fe7c8 NOTICES_SHA=46056efcb4c0e11e1cc9a33104c4d2ae9b42d566ec74885804914c4eb41ef2ec VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Tue, 15 Nov 2022 03:23:53 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Tue, 15 Nov 2022 03:23:53 GMT
USER 1001
# Tue, 15 Nov 2022 03:23:53 GMT
EXPOSE 9080 9443
# Tue, 15 Nov 2022 03:23:53 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 15 Nov 2022 03:23:53 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:a404e54162968593b8d92b571f3cdd673e4c9eab5d9be28d7c494595c0aa6682`  
		Last Modified: Wed, 19 Oct 2022 22:03:02 GMT  
		Size: 26.7 MB (26712500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c575a748d387bc29aaca33bf9a03ae2a062e61b424be275006c0d73ba2c2273`  
		Last Modified: Tue, 25 Oct 2022 17:00:16 GMT  
		Size: 3.0 MB (2957891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df73c475e4c165c33762ecd295e86b6eb72e5746b0c6badee7693a16b61f040d`  
		Last Modified: Tue, 25 Oct 2022 17:00:25 GMT  
		Size: 129.4 MB (129351634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571ce8ed913bdcb0c1bbdf7729bbcc9be32e9acf7a87fd9bf01a935f800d85e1`  
		Last Modified: Tue, 15 Nov 2022 03:52:37 GMT  
		Size: 14.2 MB (14211250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95d2a19a1004fb04c687e77d860e536b2fb50d6abafb93b8a0dbb0004243ae2`  
		Last Modified: Tue, 15 Nov 2022 03:52:33 GMT  
		Size: 690.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e1f234c117dfd2385dc328983125774857b081a7fab479441dfa1810766b96`  
		Last Modified: Tue, 15 Nov 2022 03:52:34 GMT  
		Size: 9.8 KB (9762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89236850111edd79069ec47942c1ba56f7dacd114d62e12e333b1ada5da603d`  
		Last Modified: Tue, 15 Nov 2022 03:52:34 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61018e6eb697e3a96d82fa25d090b9a27e4658c0875e3096dfc416e9d99443bc`  
		Last Modified: Tue, 15 Nov 2022 03:52:33 GMT  
		Size: 10.7 KB (10747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb66d649467d22bf412ec8e7ffd0d0d2ed8ace150b392bdbf7df18a156ed3252`  
		Last Modified: Tue, 15 Nov 2022 03:52:35 GMT  
		Size: 5.9 MB (5879134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:a50634b1b2e0e4fe02a589abeb0249f2d449917546f93b6a1393de743d1a5938
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.2 MB (182211530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd59a199b4b87d806c6007429238f4da5da81e913461746b6ec3b210993da7d`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 05 Oct 2022 10:51:52 GMT
ADD file:d93b8e74342ae6048a42c90c30192dd384e92b697ad4d8d5944868e03325820c in / 
# Wed, 05 Oct 2022 10:51:54 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 20:30:38 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 05 Oct 2022 20:30:55 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 20:30:56 GMT
ENV JAVA_VERSION=8.0.7.16
# Wed, 05 Oct 2022 20:33:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='70b5592485b0188b421cb0a072e913e3f93dfebcbc63096651258b622f19e710';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='2cf9c65de9a8dce78ebb4403b0d83a173cda3b3b5064ce5f6f63236f89e607c0';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='eaae9e57e497ab9850203384a373a473f0d8648b02c1de5c1e01af14794c5af9';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='aa301e7f2fa12ba5b3c2183674d232e8942fd6061ea2efa589d1f404969d810b';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='e091ac9b24b35f1c6cf28f3fb494e3643841bc7949c28bf6899bc384ef547ba7';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 05 Oct 2022 20:33:17 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 05 Oct 2022 22:34:11 GMT
ARG VERBOSE=false
# Wed, 05 Oct 2022 22:34:12 GMT
ARG OPENJ9_SCC=true
# Wed, 05 Oct 2022 22:34:12 GMT
ARG EN_SHA=44a2cb9704f0ed8e871e9d1a8faa55563d093d0c34af3c248492dd1790a794eb
# Wed, 05 Oct 2022 22:34:13 GMT
ARG NON_IBM_SHA=9e1ddbc876eb5fd3182799b2ccf6619f23acfe6d4b0b8ee82c72e3944ad15b34
# Wed, 05 Oct 2022 22:34:13 GMT
ARG NOTICES_SHA=1f852693234e6b9fabccb4218a21a88b485300dccd76ee089fb007aaf3180725
# Wed, 05 Oct 2022 22:34:13 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=22.0.0.10 org.opencontainers.image.revision=cl221020220912-1100 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 05 Oct 2022 22:34:14 GMT
ENV LIBERTY_VERSION=22.0.0_10
# Wed, 05 Oct 2022 22:34:14 GMT
ARG LIBERTY_URL
# Wed, 05 Oct 2022 22:34:14 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 05 Oct 2022 22:34:54 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=44a2cb9704f0ed8e871e9d1a8faa55563d093d0c34af3c248492dd1790a794eb NON_IBM_SHA=9e1ddbc876eb5fd3182799b2ccf6619f23acfe6d4b0b8ee82c72e3944ad15b34 NOTICES_SHA=1f852693234e6b9fabccb4218a21a88b485300dccd76ee089fb007aaf3180725 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 22:34:55 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 22:34:55 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=22.0.0.10 BuildLabel=cl221020220912-1100
# Wed, 05 Oct 2022 22:34:55 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 05 Oct 2022 22:34:58 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=44a2cb9704f0ed8e871e9d1a8faa55563d093d0c34af3c248492dd1790a794eb NON_IBM_SHA=9e1ddbc876eb5fd3182799b2ccf6619f23acfe6d4b0b8ee82c72e3944ad15b34 NOTICES_SHA=1f852693234e6b9fabccb4218a21a88b485300dccd76ee089fb007aaf3180725 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 05 Oct 2022 22:34:58 GMT
COPY dir:8bf844c49178cf63745af9ec643f57d70bd92c28166fabfad188dfc250d88353 in /opt/ibm/helpers/ 
# Wed, 05 Oct 2022 22:34:59 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 05 Oct 2022 22:35:00 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=44a2cb9704f0ed8e871e9d1a8faa55563d093d0c34af3c248492dd1790a794eb NON_IBM_SHA=9e1ddbc876eb5fd3182799b2ccf6619f23acfe6d4b0b8ee82c72e3944ad15b34 NOTICES_SHA=1f852693234e6b9fabccb4218a21a88b485300dccd76ee089fb007aaf3180725 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 05 Oct 2022 22:35:14 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=44a2cb9704f0ed8e871e9d1a8faa55563d093d0c34af3c248492dd1790a794eb NON_IBM_SHA=9e1ddbc876eb5fd3182799b2ccf6619f23acfe6d4b0b8ee82c72e3944ad15b34 NOTICES_SHA=1f852693234e6b9fabccb4218a21a88b485300dccd76ee089fb007aaf3180725 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 05 Oct 2022 22:35:15 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 05 Oct 2022 22:35:15 GMT
USER 1001
# Wed, 05 Oct 2022 22:35:16 GMT
EXPOSE 9080 9443
# Wed, 05 Oct 2022 22:35:16 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 05 Oct 2022 22:35:17 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:faece833463c99bd10748da29171f2d588a627912f7bbb982b3ca4512dd39eed`  
		Last Modified: Wed, 05 Oct 2022 10:54:03 GMT  
		Size: 30.4 MB (30442565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52af0b72f683bca4c76215658777957eba73fde39f2157d70f361b51f1e4c42`  
		Last Modified: Wed, 05 Oct 2022 20:38:46 GMT  
		Size: 3.1 MB (3075970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46038b192d2e7c544903b03f01644aad2ba1b5d0e70be5a02dac1b3997ff4bd`  
		Last Modified: Wed, 05 Oct 2022 20:39:02 GMT  
		Size: 129.0 MB (129014178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df214124ef3129c9d23e801433511dc9523afaecc76ead85623f8293d5761f5d`  
		Last Modified: Thu, 06 Oct 2022 01:00:44 GMT  
		Size: 14.2 MB (14179054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13dad937f24561e59f398a1fa1912ded0549cf466931f6269d56e1d602a850a6`  
		Last Modified: Thu, 06 Oct 2022 01:00:39 GMT  
		Size: 679.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59b2e9ede0732dde4300a47b1d39fadbcc5970c466fb76a87aa4b97bdd606d6`  
		Last Modified: Thu, 06 Oct 2022 01:00:39 GMT  
		Size: 9.8 KB (9757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40047f82754a673adde51b41e5f8f0d597f7f905298d176332dd4988ee0b4564`  
		Last Modified: Thu, 06 Oct 2022 01:00:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dfdd39276a4b6a129d8610e4c0a79f6fe9b40f9a6e28958d1cde7aef6176865`  
		Last Modified: Thu, 06 Oct 2022 01:00:39 GMT  
		Size: 10.7 KB (10740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932d61cfac976e78b8e821694cc79d5b9a9d6be8d8203c8b16b0707b96b9bde6`  
		Last Modified: Thu, 06 Oct 2022 01:00:40 GMT  
		Size: 5.5 MB (5478312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:bf5ba3b73fc7893485541299bb29678c3906e62623cde9a184caf7c45b82c58c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174787891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8cc20bedbda27b4ea8838ee853ffac9623ec3a877a49c808c43e8d81bfe041b`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 25 Oct 2022 01:23:02 GMT
ADD file:0843e89b8865a30626cece7a42cf27708a86422aadb28029168b2f159a8768fa in / 
# Tue, 25 Oct 2022 01:23:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:08:47 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 25 Oct 2022 08:09:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:09:02 GMT
ENV JAVA_VERSION=8.0.7.16
# Tue, 25 Oct 2022 08:09:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='70b5592485b0188b421cb0a072e913e3f93dfebcbc63096651258b622f19e710';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='2cf9c65de9a8dce78ebb4403b0d83a173cda3b3b5064ce5f6f63236f89e607c0';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='eaae9e57e497ab9850203384a373a473f0d8648b02c1de5c1e01af14794c5af9';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='aa301e7f2fa12ba5b3c2183674d232e8942fd6061ea2efa589d1f404969d810b';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='e091ac9b24b35f1c6cf28f3fb494e3643841bc7949c28bf6899bc384ef547ba7';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 25 Oct 2022 08:09:53 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 25 Oct 2022 17:41:20 GMT
ARG VERBOSE=false
# Tue, 25 Oct 2022 17:41:20 GMT
ARG OPENJ9_SCC=true
# Tue, 15 Nov 2022 00:54:45 GMT
ARG EN_SHA=1ce31500fa2422ed1410137cd50d33e18cf42ad0ae0b5a3e545183ae801869e0
# Tue, 15 Nov 2022 00:54:45 GMT
ARG NON_IBM_SHA=1f032aeb46b5f5f4262f123cb2339230e2755cac039cb1bf0285cbb0f37fe7c8
# Tue, 15 Nov 2022 00:54:45 GMT
ARG NOTICES_SHA=46056efcb4c0e11e1cc9a33104c4d2ae9b42d566ec74885804914c4eb41ef2ec
# Tue, 15 Nov 2022 00:54:45 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=22.0.0.11 org.opencontainers.image.revision=cl221120221010-1540 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Tue, 15 Nov 2022 00:54:45 GMT
ENV LIBERTY_VERSION=22.0.0_11
# Tue, 15 Nov 2022 00:54:46 GMT
ARG LIBERTY_URL
# Tue, 15 Nov 2022 00:54:46 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 15 Nov 2022 00:54:59 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ce31500fa2422ed1410137cd50d33e18cf42ad0ae0b5a3e545183ae801869e0 NON_IBM_SHA=1f032aeb46b5f5f4262f123cb2339230e2755cac039cb1bf0285cbb0f37fe7c8 NOTICES_SHA=46056efcb4c0e11e1cc9a33104c4d2ae9b42d566ec74885804914c4eb41ef2ec OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 00:54:59 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 00:54:59 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=22.0.0.11 BuildLabel=cl221120221010-1540
# Tue, 15 Nov 2022 00:55:00 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 15 Nov 2022 00:55:01 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ce31500fa2422ed1410137cd50d33e18cf42ad0ae0b5a3e545183ae801869e0 NON_IBM_SHA=1f032aeb46b5f5f4262f123cb2339230e2755cac039cb1bf0285cbb0f37fe7c8 NOTICES_SHA=46056efcb4c0e11e1cc9a33104c4d2ae9b42d566ec74885804914c4eb41ef2ec VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Tue, 15 Nov 2022 00:55:01 GMT
COPY dir:8bf844c49178cf63745af9ec643f57d70bd92c28166fabfad188dfc250d88353 in /opt/ibm/helpers/ 
# Tue, 15 Nov 2022 00:55:01 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Tue, 15 Nov 2022 00:55:02 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ce31500fa2422ed1410137cd50d33e18cf42ad0ae0b5a3e545183ae801869e0 NON_IBM_SHA=1f032aeb46b5f5f4262f123cb2339230e2755cac039cb1bf0285cbb0f37fe7c8 NOTICES_SHA=46056efcb4c0e11e1cc9a33104c4d2ae9b42d566ec74885804914c4eb41ef2ec VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Tue, 15 Nov 2022 00:55:10 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ce31500fa2422ed1410137cd50d33e18cf42ad0ae0b5a3e545183ae801869e0 NON_IBM_SHA=1f032aeb46b5f5f4262f123cb2339230e2755cac039cb1bf0285cbb0f37fe7c8 NOTICES_SHA=46056efcb4c0e11e1cc9a33104c4d2ae9b42d566ec74885804914c4eb41ef2ec VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Tue, 15 Nov 2022 00:55:10 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Tue, 15 Nov 2022 00:55:10 GMT
USER 1001
# Tue, 15 Nov 2022 00:55:10 GMT
EXPOSE 9080 9443
# Tue, 15 Nov 2022 00:55:11 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 15 Nov 2022 00:55:11 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:4cd692a206d359f66e10c4f4f2a37009c4162f022df78a9bb8e8c24def290167`  
		Last Modified: Tue, 25 Oct 2022 01:24:23 GMT  
		Size: 25.4 MB (25371461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b48aa864b900d3e1ae35d49fc6be512e393a95d7020a8372679d9d04253958`  
		Last Modified: Tue, 25 Oct 2022 08:12:34 GMT  
		Size: 2.7 MB (2671897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531feab56e821d4ffe255d1300f353374850ebbcc72b32bebce77416818308b4`  
		Last Modified: Tue, 25 Oct 2022 08:12:42 GMT  
		Size: 126.5 MB (126472281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af39b5f12550895528fbc296d508af9d452a5a56c6420adec180da6da977668`  
		Last Modified: Tue, 15 Nov 2022 01:23:59 GMT  
		Size: 14.2 MB (14211275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237041ff3fc422b00da2230c8b1dac8c8f72273f1b5699fec2e9fb9225c48d89`  
		Last Modified: Tue, 15 Nov 2022 01:23:56 GMT  
		Size: 675.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b161861ce53c38136e05129983e84b0676905d749f2a599e019c4ce8394d7964`  
		Last Modified: Tue, 15 Nov 2022 01:23:56 GMT  
		Size: 9.8 KB (9760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33901029ac83aec57348ef02dac0fd6132b3cfd0f7d524ad329b92398d811848`  
		Last Modified: Tue, 15 Nov 2022 01:23:56 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f0d7513fbef9b3e172a40ba630406daa23b0bc11e8b0da9645b79a79073f91`  
		Last Modified: Tue, 15 Nov 2022 01:23:56 GMT  
		Size: 10.7 KB (10738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39894e61f71a00c59f85f2012a5187f1c0fbd87af61bef0a7403abfa82817e17`  
		Last Modified: Tue, 15 Nov 2022 01:23:57 GMT  
		Size: 6.0 MB (6039529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
