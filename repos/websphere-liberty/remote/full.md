## `websphere-liberty:full`

```console
$ docker pull websphere-liberty@sha256:a0b769b78bccac2696fbf49b4abd2d1cf4beafae967ae3c9bc11c5c0fb210d1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:full` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:bece48ab08074b0c671099a7f4be3856a0ed3f55afe9b18496997d5e99f4af87
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.8 MB (518750513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa9607847379f4259b4355e190a8ccfba0baea0c4b71b3b82f111c60e5aadeb1`
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
# Tue, 15 Nov 2022 03:24:52 GMT
ARG VERBOSE=false
# Tue, 15 Nov 2022 03:24:52 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 15 Nov 2022 03:32:57 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Tue, 15 Nov 2022 03:32:58 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Tue, 15 Nov 2022 03:33:30 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
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
	-	`sha256:bcabe5b2316c3b8b1c83ccd94463e837813f2e787c5fb3177f5930a58cf0923d`  
		Last Modified: Tue, 15 Nov 2022 03:53:17 GMT  
		Size: 323.6 MB (323559909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052e1ddb90f0642aa84944f0ce18cc069d6525ea3821025eabd8c6fa44ef79a2`  
		Last Modified: Tue, 15 Nov 2022 03:53:01 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44226e0e7e29bc8a2b1ee51f558ac5fc379168f7cb7e18317fa2423c515d1580`  
		Last Modified: Tue, 15 Nov 2022 03:53:04 GMT  
		Size: 16.1 MB (16055773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:a5346f6264cb3e455ed2706341a6cd9bd6de84940303c6d01e15b90c18b1b3e0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **519.7 MB (519666425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46577fea440af2fd243acae70d785bd57b5be0557993af43f50e4cfe868fe8ee`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 25 Oct 2022 03:25:34 GMT
ADD file:254e11be9bc865d645aba7c16a39a04f5ce227b7aa4280f7a42baec47b0c6ee0 in / 
# Tue, 25 Oct 2022 03:25:36 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 14:07:39 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 25 Oct 2022 14:08:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 14:08:09 GMT
ENV JAVA_VERSION=8.0.7.16
# Tue, 25 Oct 2022 14:10:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='70b5592485b0188b421cb0a072e913e3f93dfebcbc63096651258b622f19e710';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='2cf9c65de9a8dce78ebb4403b0d83a173cda3b3b5064ce5f6f63236f89e607c0';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='eaae9e57e497ab9850203384a373a473f0d8648b02c1de5c1e01af14794c5af9';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='aa301e7f2fa12ba5b3c2183674d232e8942fd6061ea2efa589d1f404969d810b';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='e091ac9b24b35f1c6cf28f3fb494e3643841bc7949c28bf6899bc384ef547ba7';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 25 Oct 2022 14:10:35 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 26 Oct 2022 03:12:54 GMT
ARG VERBOSE=false
# Wed, 26 Oct 2022 03:12:54 GMT
ARG OPENJ9_SCC=true
# Tue, 15 Nov 2022 04:15:13 GMT
ARG EN_SHA=1ce31500fa2422ed1410137cd50d33e18cf42ad0ae0b5a3e545183ae801869e0
# Tue, 15 Nov 2022 04:15:13 GMT
ARG NON_IBM_SHA=1f032aeb46b5f5f4262f123cb2339230e2755cac039cb1bf0285cbb0f37fe7c8
# Tue, 15 Nov 2022 04:15:13 GMT
ARG NOTICES_SHA=46056efcb4c0e11e1cc9a33104c4d2ae9b42d566ec74885804914c4eb41ef2ec
# Tue, 15 Nov 2022 04:15:14 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=22.0.0.11 org.opencontainers.image.revision=cl221120221010-1540 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Tue, 15 Nov 2022 04:15:14 GMT
ENV LIBERTY_VERSION=22.0.0_11
# Tue, 15 Nov 2022 04:15:14 GMT
ARG LIBERTY_URL
# Tue, 15 Nov 2022 04:15:15 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 15 Nov 2022 04:16:04 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ce31500fa2422ed1410137cd50d33e18cf42ad0ae0b5a3e545183ae801869e0 NON_IBM_SHA=1f032aeb46b5f5f4262f123cb2339230e2755cac039cb1bf0285cbb0f37fe7c8 NOTICES_SHA=46056efcb4c0e11e1cc9a33104c4d2ae9b42d566ec74885804914c4eb41ef2ec OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 04:16:04 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 04:16:05 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=22.0.0.11 BuildLabel=cl221120221010-1540
# Tue, 15 Nov 2022 04:16:05 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 15 Nov 2022 04:16:08 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ce31500fa2422ed1410137cd50d33e18cf42ad0ae0b5a3e545183ae801869e0 NON_IBM_SHA=1f032aeb46b5f5f4262f123cb2339230e2755cac039cb1bf0285cbb0f37fe7c8 NOTICES_SHA=46056efcb4c0e11e1cc9a33104c4d2ae9b42d566ec74885804914c4eb41ef2ec VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Tue, 15 Nov 2022 04:16:08 GMT
COPY dir:8bf844c49178cf63745af9ec643f57d70bd92c28166fabfad188dfc250d88353 in /opt/ibm/helpers/ 
# Tue, 15 Nov 2022 04:16:09 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Tue, 15 Nov 2022 04:16:10 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ce31500fa2422ed1410137cd50d33e18cf42ad0ae0b5a3e545183ae801869e0 NON_IBM_SHA=1f032aeb46b5f5f4262f123cb2339230e2755cac039cb1bf0285cbb0f37fe7c8 NOTICES_SHA=46056efcb4c0e11e1cc9a33104c4d2ae9b42d566ec74885804914c4eb41ef2ec VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Tue, 15 Nov 2022 04:16:25 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ce31500fa2422ed1410137cd50d33e18cf42ad0ae0b5a3e545183ae801869e0 NON_IBM_SHA=1f032aeb46b5f5f4262f123cb2339230e2755cac039cb1bf0285cbb0f37fe7c8 NOTICES_SHA=46056efcb4c0e11e1cc9a33104c4d2ae9b42d566ec74885804914c4eb41ef2ec VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Tue, 15 Nov 2022 04:16:25 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Tue, 15 Nov 2022 04:16:26 GMT
USER 1001
# Tue, 15 Nov 2022 04:16:26 GMT
EXPOSE 9080 9443
# Tue, 15 Nov 2022 04:16:26 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 15 Nov 2022 04:16:27 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 15 Nov 2022 04:19:14 GMT
ARG VERBOSE=false
# Tue, 15 Nov 2022 04:19:14 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 15 Nov 2022 04:35:24 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Tue, 15 Nov 2022 04:35:30 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Tue, 15 Nov 2022 04:36:25 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:21b8f46bc1957ff60412d81678134500cf7a4f0e7f198ba384fedb2e5747d847`  
		Last Modified: Tue, 25 Oct 2022 03:27:21 GMT  
		Size: 30.4 MB (30443225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3bd07fd743978e6c122138fc96d49720949d9378615ea1610865b23325b7af`  
		Last Modified: Tue, 25 Oct 2022 14:16:02 GMT  
		Size: 3.1 MB (3076044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427cc8d21232d28a4d9cf22428744eede16d9f7648416bbe8a5660da92d3a97f`  
		Last Modified: Tue, 25 Oct 2022 14:16:18 GMT  
		Size: 129.0 MB (129014166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e2f3998405ed64e34685f6ee1feda14a689ed31948b973218a57ea11c52ba9`  
		Last Modified: Tue, 15 Nov 2022 05:13:54 GMT  
		Size: 14.2 MB (14211767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9db5fc37d307cc00c9b8a99c297a0eceec8c321354126bec36e076342f6508a`  
		Last Modified: Tue, 15 Nov 2022 05:13:50 GMT  
		Size: 691.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8d0d4d30a99d58520ac70c3724f8c7e3b3861e0f458d80e42a5e7c38e07f56`  
		Last Modified: Tue, 15 Nov 2022 05:13:50 GMT  
		Size: 9.8 KB (9761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b9efd8909d15510643410987caf2a77b822acabff7079844972788749588bef`  
		Last Modified: Tue, 15 Nov 2022 05:13:50 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feb32bee6461fb253e2d0fc3296c150b2885695752ee68c2474c6f1bf9701461`  
		Last Modified: Tue, 15 Nov 2022 05:13:50 GMT  
		Size: 10.8 KB (10758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9536903d80c51793fc8d755d73810bd32ae553fa8fc7f2b84de96700e082eab4`  
		Last Modified: Tue, 15 Nov 2022 05:13:52 GMT  
		Size: 5.5 MB (5490419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798a04994bfa702f23b3ef30889a5d3d121b90765531ddca01673d7d312bd527`  
		Last Modified: Tue, 15 Nov 2022 05:14:52 GMT  
		Size: 323.6 MB (323560189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2dc20e318884416702e97b1238abcbedd1cd0066bf4e2a2584ba760254f749c`  
		Last Modified: Tue, 15 Nov 2022 05:14:24 GMT  
		Size: 951.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd0f26254e7e9c5be42059567774ad3bd44ba18d5cad4b74d5b1cf559f44e54`  
		Last Modified: Tue, 15 Nov 2022 05:14:27 GMT  
		Size: 13.8 MB (13848176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:68960ee57d2df1183a9f0b18fdb4289d40ad0e7b005b82020d5c2afb9501cca3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.1 MB (514145809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a04b31021501a31882f289dfcd9f973ba3d7e61de7d8a036956b83e639549698`
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
# Tue, 15 Nov 2022 00:56:10 GMT
ARG VERBOSE=false
# Tue, 15 Nov 2022 00:56:10 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 15 Nov 2022 01:03:34 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Tue, 15 Nov 2022 01:03:39 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Tue, 15 Nov 2022 01:04:03 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
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
	-	`sha256:ee66a4366d78fb11bb70626310cf83255faac6df21313b20fd17fb5181973e32`  
		Last Modified: Tue, 15 Nov 2022 01:24:33 GMT  
		Size: 323.6 MB (323559462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e3eb08a867ac31f396df828a1a069490da21a5cc16ff2290cefa88514c7f8e`  
		Last Modified: Tue, 15 Nov 2022 01:24:19 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c49d59ec3418c9f9759bc1f0076371fa832d6b7fa5da68e4bcf4c15cae7b1f`  
		Last Modified: Tue, 15 Nov 2022 01:24:21 GMT  
		Size: 15.8 MB (15797508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
