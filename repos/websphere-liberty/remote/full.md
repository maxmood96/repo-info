## `websphere-liberty:full`

```console
$ docker pull websphere-liberty@sha256:281b9733a50ee1c34e1a6b57a658376e971468cb08e2949fa269a417bc4ad742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:full` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:8f2d16043090091aa98cad510dbe79cd50427d8b5ab76b36b1a7eb0e0108e310
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.8 MB (462843689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59556339a8e63839840df14511aef646a314702108d715e06f4052c35c24da42`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:36 GMT
ADD file:c6039a4f004b6b6c2e4c281a228d64d8410cb9fdf0c67776f84bb173d3522be1 in / 
# Wed, 02 Feb 2022 02:14:36 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:40:26 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 02 Feb 2022 03:40:35 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 23 Feb 2022 18:19:41 GMT
ENV JAVA_VERSION=8.0.7.5
# Wed, 23 Feb 2022 18:20:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='e2036ff825599773d0da7ca65e526ef4653e8060b787e5f9a4967fa73756cb56';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='f4639c53ae366cda315db5f504bf7596a9757d7dccb4be66cce6e447613672cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='0961aedeaab4801cadb3d7a327344e66ef5d7f982f9269d5a0e447e4699feee7';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2469075243605203690306e9022150b86da5e9b5c563bba7ae1c3413c65b9cbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='71abbc456c06850a3f557465e988b73ecf66a22d9fd7d8a57a03dc56849f06a4';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 23 Feb 2022 18:20:16 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 23 Feb 2022 18:43:53 GMT
ARG VERBOSE=false
# Wed, 23 Feb 2022 18:43:53 GMT
ARG OPENJ9_SCC=true
# Fri, 25 Feb 2022 02:42:37 GMT
ARG EN_SHA=de0dc0b4f90213bfa8bbe8a786af91504f78b1967775a31d46dc55ff14f2d171
# Fri, 25 Feb 2022 02:42:37 GMT
ARG NON_IBM_SHA=20a37b8cc381d969d985faebf766bfe5efa07b803d063e0f8739fbe571f43f87
# Fri, 25 Feb 2022 02:42:38 GMT
ARG NOTICES_SHA=eaa5532a956414b08a405c8fe78dd7295bfd1f37980b496dbe855def1432a659
# Fri, 25 Feb 2022 02:42:38 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=22.0.0.2 org.opencontainers.image.revision=cl220220220201-1901 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 25 Feb 2022 02:42:38 GMT
ENV LIBERTY_VERSION=22.0.0_02
# Fri, 25 Feb 2022 02:42:38 GMT
ARG LIBERTY_URL
# Fri, 25 Feb 2022 02:42:39 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 25 Feb 2022 02:42:53 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=de0dc0b4f90213bfa8bbe8a786af91504f78b1967775a31d46dc55ff14f2d171 NON_IBM_SHA=20a37b8cc381d969d985faebf766bfe5efa07b803d063e0f8739fbe571f43f87 NOTICES_SHA=eaa5532a956414b08a405c8fe78dd7295bfd1f37980b496dbe855def1432a659 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 25 Feb 2022 02:42:53 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Feb 2022 02:42:53 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=22.0.0.2 BuildLabel=cl220220220201-1901
# Fri, 25 Feb 2022 02:42:54 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 25 Feb 2022 02:42:55 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=de0dc0b4f90213bfa8bbe8a786af91504f78b1967775a31d46dc55ff14f2d171 NON_IBM_SHA=20a37b8cc381d969d985faebf766bfe5efa07b803d063e0f8739fbe571f43f87 NOTICES_SHA=eaa5532a956414b08a405c8fe78dd7295bfd1f37980b496dbe855def1432a659 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 25 Feb 2022 02:42:56 GMT
COPY dir:b44499731da0f244ad2e27b60beff4f4cda216316903b60ecb41a7fba3784b48 in /opt/ibm/helpers/ 
# Fri, 25 Feb 2022 02:42:56 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 25 Feb 2022 02:42:57 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=de0dc0b4f90213bfa8bbe8a786af91504f78b1967775a31d46dc55ff14f2d171 NON_IBM_SHA=20a37b8cc381d969d985faebf766bfe5efa07b803d063e0f8739fbe571f43f87 NOTICES_SHA=eaa5532a956414b08a405c8fe78dd7295bfd1f37980b496dbe855def1432a659 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 25 Feb 2022 02:43:08 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=de0dc0b4f90213bfa8bbe8a786af91504f78b1967775a31d46dc55ff14f2d171 NON_IBM_SHA=20a37b8cc381d969d985faebf766bfe5efa07b803d063e0f8739fbe571f43f87 NOTICES_SHA=eaa5532a956414b08a405c8fe78dd7295bfd1f37980b496dbe855def1432a659 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 25 Feb 2022 02:43:08 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 25 Feb 2022 02:43:09 GMT
USER 1001
# Fri, 25 Feb 2022 02:43:09 GMT
EXPOSE 9080 9443
# Fri, 25 Feb 2022 02:43:09 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 25 Feb 2022 02:43:09 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 25 Feb 2022 02:44:19 GMT
ARG VERBOSE=false
# Fri, 25 Feb 2022 02:44:19 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 25 Feb 2022 02:48:04 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Fri, 25 Feb 2022 02:48:05 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 25 Feb 2022 02:48:43 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:68e7bb398b9ff421236990bfeaf5c1feab26c590eed93489e245375c23551e2a`  
		Last Modified: Sat, 29 Jan 2022 14:35:20 GMT  
		Size: 26.7 MB (26708066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fb07417efc9ce7b84eb9ed465e87c936352af2a77456046d4e4c6f7f3e7a57`  
		Last Modified: Wed, 02 Feb 2022 03:42:54 GMT  
		Size: 3.0 MB (2959756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce6137e2e1f619db66c2c9ff65965cfd31071423a32d9be3771cfd6b817e37f`  
		Last Modified: Wed, 23 Feb 2022 18:24:46 GMT  
		Size: 128.8 MB (128801682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d1b0859837afdd4f1b256d24f75d6016c7f46a28c790c3f756552361047e8a`  
		Last Modified: Fri, 25 Feb 2022 03:26:43 GMT  
		Size: 14.1 MB (14089056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511595bb26c852e22305665db2cd0964ae84b8b292b559d34c56ed7fc4ac1d96`  
		Last Modified: Fri, 25 Feb 2022 03:26:39 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:338445613f0c3b58ee60ec80c66f2ab364bde5f9054e80895e260be7abf0234a`  
		Last Modified: Fri, 25 Feb 2022 03:26:39 GMT  
		Size: 9.7 KB (9685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e470397963cb431ab42bb461e02d55f076c48d24dc0205c5a8c90e773b6f0b`  
		Last Modified: Fri, 25 Feb 2022 03:26:39 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba4201ba7b59f897588d9e3d95f953322f3db5bc4b5b5cc81baec20689597a0`  
		Last Modified: Fri, 25 Feb 2022 03:26:39 GMT  
		Size: 10.7 KB (10665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d321ac89357a586763da4166851de8be8225ea6a70e7a5f39ea1a8caaaf7c53`  
		Last Modified: Fri, 25 Feb 2022 03:26:40 GMT  
		Size: 5.8 MB (5804057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d800abce4dcf0328a293da15d24dac6ddb4d9aa4eea4c16a12e07bd5438dbfb`  
		Last Modified: Fri, 25 Feb 2022 03:27:25 GMT  
		Size: 268.4 MB (268390102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8adb306767d550c4fabb362c227f51a54d9bfac17365b864d969aa66902032`  
		Last Modified: Fri, 25 Feb 2022 03:27:11 GMT  
		Size: 944.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c3a68123d3abb3d6009734ffcd2d57d856948dbd07c7fdc45e8a2a7ae8234f`  
		Last Modified: Fri, 25 Feb 2022 03:27:14 GMT  
		Size: 16.1 MB (16068705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:882090f1d6336b86bc456c476c720068f41ec1c1d6ad2241a164bf2790be1e6f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.4 MB (463418093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e619136f898820a00336714c707a682be3c69b3249b7fd3976aa559691c0a717`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 02 Feb 2022 03:49:58 GMT
ADD file:19b6b516bfde37805273abae0012aaceb45030dcc0c1dbc11828a4dfa6549c29 in / 
# Wed, 02 Feb 2022 03:50:03 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 06:01:20 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 02 Feb 2022 06:01:55 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 23 Feb 2022 18:17:17 GMT
ENV JAVA_VERSION=8.0.7.5
# Wed, 23 Feb 2022 18:18:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='e2036ff825599773d0da7ca65e526ef4653e8060b787e5f9a4967fa73756cb56';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='f4639c53ae366cda315db5f504bf7596a9757d7dccb4be66cce6e447613672cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='0961aedeaab4801cadb3d7a327344e66ef5d7f982f9269d5a0e447e4699feee7';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2469075243605203690306e9022150b86da5e9b5c563bba7ae1c3413c65b9cbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='71abbc456c06850a3f557465e988b73ecf66a22d9fd7d8a57a03dc56849f06a4';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 23 Feb 2022 18:18:40 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 23 Feb 2022 18:48:55 GMT
ARG VERBOSE=false
# Wed, 23 Feb 2022 18:49:02 GMT
ARG OPENJ9_SCC=true
# Fri, 25 Feb 2022 02:56:55 GMT
ARG EN_SHA=de0dc0b4f90213bfa8bbe8a786af91504f78b1967775a31d46dc55ff14f2d171
# Fri, 25 Feb 2022 02:56:58 GMT
ARG NON_IBM_SHA=20a37b8cc381d969d985faebf766bfe5efa07b803d063e0f8739fbe571f43f87
# Fri, 25 Feb 2022 02:57:00 GMT
ARG NOTICES_SHA=eaa5532a956414b08a405c8fe78dd7295bfd1f37980b496dbe855def1432a659
# Fri, 25 Feb 2022 02:57:02 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=22.0.0.2 org.opencontainers.image.revision=cl220220220201-1901 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 25 Feb 2022 02:57:04 GMT
ENV LIBERTY_VERSION=22.0.0_02
# Fri, 25 Feb 2022 02:57:07 GMT
ARG LIBERTY_URL
# Fri, 25 Feb 2022 02:57:11 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 25 Feb 2022 02:57:57 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=de0dc0b4f90213bfa8bbe8a786af91504f78b1967775a31d46dc55ff14f2d171 NON_IBM_SHA=20a37b8cc381d969d985faebf766bfe5efa07b803d063e0f8739fbe571f43f87 NOTICES_SHA=eaa5532a956414b08a405c8fe78dd7295bfd1f37980b496dbe855def1432a659 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 25 Feb 2022 02:57:59 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Feb 2022 02:58:02 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=22.0.0.2 BuildLabel=cl220220220201-1901
# Fri, 25 Feb 2022 02:58:06 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 25 Feb 2022 02:58:36 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=de0dc0b4f90213bfa8bbe8a786af91504f78b1967775a31d46dc55ff14f2d171 NON_IBM_SHA=20a37b8cc381d969d985faebf766bfe5efa07b803d063e0f8739fbe571f43f87 NOTICES_SHA=eaa5532a956414b08a405c8fe78dd7295bfd1f37980b496dbe855def1432a659 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 25 Feb 2022 02:58:39 GMT
COPY dir:b44499731da0f244ad2e27b60beff4f4cda216316903b60ecb41a7fba3784b48 in /opt/ibm/helpers/ 
# Fri, 25 Feb 2022 02:58:41 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 25 Feb 2022 02:58:57 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=de0dc0b4f90213bfa8bbe8a786af91504f78b1967775a31d46dc55ff14f2d171 NON_IBM_SHA=20a37b8cc381d969d985faebf766bfe5efa07b803d063e0f8739fbe571f43f87 NOTICES_SHA=eaa5532a956414b08a405c8fe78dd7295bfd1f37980b496dbe855def1432a659 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 25 Feb 2022 02:59:22 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=de0dc0b4f90213bfa8bbe8a786af91504f78b1967775a31d46dc55ff14f2d171 NON_IBM_SHA=20a37b8cc381d969d985faebf766bfe5efa07b803d063e0f8739fbe571f43f87 NOTICES_SHA=eaa5532a956414b08a405c8fe78dd7295bfd1f37980b496dbe855def1432a659 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 25 Feb 2022 02:59:24 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 25 Feb 2022 02:59:29 GMT
USER 1001
# Fri, 25 Feb 2022 02:59:33 GMT
EXPOSE 9080 9443
# Fri, 25 Feb 2022 02:59:38 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 25 Feb 2022 02:59:45 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 25 Feb 2022 03:05:40 GMT
ARG VERBOSE=false
# Fri, 25 Feb 2022 03:05:45 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 25 Feb 2022 03:10:59 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Fri, 25 Feb 2022 03:11:03 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 25 Feb 2022 03:12:00 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:1dc99fe180768d17487534d27fca7d2aea3e7473c284314a65af7be77144eeaa`  
		Last Modified: Wed, 02 Feb 2022 03:52:51 GMT  
		Size: 30.4 MB (30437685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e519c40c78b488d71991dd0054bffe8260611286580cb61463ffb1d4b81bb2`  
		Last Modified: Wed, 02 Feb 2022 06:05:57 GMT  
		Size: 3.1 MB (3081867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b200af3378ba06b33bd6007bbe485b27c8ebe25abd5fd750e13c5223ea530e47`  
		Last Modified: Wed, 23 Feb 2022 18:22:40 GMT  
		Size: 128.3 MB (128315531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5a46af2e8c8bf2c29e0ad7f5b4dede68c87d1797d8085f8647713fa1dab889`  
		Last Modified: Fri, 25 Feb 2022 04:22:06 GMT  
		Size: 14.1 MB (14089694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09010666dfc846b385503765a75213287da9563694d29ae831a9d188962801c6`  
		Last Modified: Fri, 25 Feb 2022 04:21:55 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de38262c3d3960aff56d83c4681d4b42e963fa2d575c78ce85ddc0f3cc2697e`  
		Last Modified: Fri, 25 Feb 2022 04:21:55 GMT  
		Size: 9.7 KB (9683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c12ec83899f606d08b3acff2ceffe51031dd9ac14e3450670e6cd936d43cb8`  
		Last Modified: Fri, 25 Feb 2022 04:21:55 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b96fdf08aee619075b300e26c74b4b9705c6ba7b93b4f63f2697de9888b678`  
		Last Modified: Fri, 25 Feb 2022 04:21:55 GMT  
		Size: 10.7 KB (10672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86eff334204c796902d7425d9b774109da033e82cfe421f39aef5bfc6246ae4`  
		Last Modified: Fri, 25 Feb 2022 04:21:58 GMT  
		Size: 5.4 MB (5350322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055b2cd54bf8d5e23ebee1b333c7c38ab5bdd5d4c2714ca531a9a7c1d2ef4d4f`  
		Last Modified: Fri, 25 Feb 2022 04:24:25 GMT  
		Size: 268.4 MB (268391390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635d05a2043d0d8409e861f7b34b95f7ba1544f2814d114ae2365cc3309451bd`  
		Last Modified: Fri, 25 Feb 2022 04:22:46 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841e2584d9ff64eecd77c178d8446c41275685cdad6aaa2a8efe5e33151cb113`  
		Last Modified: Fri, 25 Feb 2022 04:22:54 GMT  
		Size: 13.7 MB (13729321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:51687d4304ea05cb74c08268f8d4fbefae30ae1f54c132ace56f568bd8271300
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **458.0 MB (458007459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aad946ba7b8768baa1c80e04b29f2381e96b43ab20ac3266041e9c4d9ce331e`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 02 Feb 2022 01:42:03 GMT
ADD file:3fe2ce9d5d8932ed39dc2c73abff4b15e244fb1e7eb456de0a05df07ede3bf39 in / 
# Wed, 02 Feb 2022 01:42:07 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:39:28 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 02 Feb 2022 02:39:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 23 Feb 2022 18:41:31 GMT
ENV JAVA_VERSION=8.0.7.5
# Wed, 23 Feb 2022 18:42:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='e2036ff825599773d0da7ca65e526ef4653e8060b787e5f9a4967fa73756cb56';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='f4639c53ae366cda315db5f504bf7596a9757d7dccb4be66cce6e447613672cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='0961aedeaab4801cadb3d7a327344e66ef5d7f982f9269d5a0e447e4699feee7';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2469075243605203690306e9022150b86da5e9b5c563bba7ae1c3413c65b9cbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='71abbc456c06850a3f557465e988b73ecf66a22d9fd7d8a57a03dc56849f06a4';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 23 Feb 2022 18:42:14 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 23 Feb 2022 20:13:04 GMT
ARG VERBOSE=false
# Wed, 23 Feb 2022 20:13:04 GMT
ARG OPENJ9_SCC=true
# Fri, 25 Feb 2022 02:55:42 GMT
ARG EN_SHA=de0dc0b4f90213bfa8bbe8a786af91504f78b1967775a31d46dc55ff14f2d171
# Fri, 25 Feb 2022 02:55:42 GMT
ARG NON_IBM_SHA=20a37b8cc381d969d985faebf766bfe5efa07b803d063e0f8739fbe571f43f87
# Fri, 25 Feb 2022 02:55:43 GMT
ARG NOTICES_SHA=eaa5532a956414b08a405c8fe78dd7295bfd1f37980b496dbe855def1432a659
# Fri, 25 Feb 2022 02:55:43 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=22.0.0.2 org.opencontainers.image.revision=cl220220220201-1901 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 25 Feb 2022 02:55:43 GMT
ENV LIBERTY_VERSION=22.0.0_02
# Fri, 25 Feb 2022 02:55:43 GMT
ARG LIBERTY_URL
# Fri, 25 Feb 2022 02:55:43 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 25 Feb 2022 02:55:56 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=de0dc0b4f90213bfa8bbe8a786af91504f78b1967775a31d46dc55ff14f2d171 NON_IBM_SHA=20a37b8cc381d969d985faebf766bfe5efa07b803d063e0f8739fbe571f43f87 NOTICES_SHA=eaa5532a956414b08a405c8fe78dd7295bfd1f37980b496dbe855def1432a659 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 25 Feb 2022 02:55:56 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Feb 2022 02:55:56 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=22.0.0.2 BuildLabel=cl220220220201-1901
# Fri, 25 Feb 2022 02:55:56 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 25 Feb 2022 02:55:57 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=de0dc0b4f90213bfa8bbe8a786af91504f78b1967775a31d46dc55ff14f2d171 NON_IBM_SHA=20a37b8cc381d969d985faebf766bfe5efa07b803d063e0f8739fbe571f43f87 NOTICES_SHA=eaa5532a956414b08a405c8fe78dd7295bfd1f37980b496dbe855def1432a659 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 25 Feb 2022 02:55:57 GMT
COPY dir:b44499731da0f244ad2e27b60beff4f4cda216316903b60ecb41a7fba3784b48 in /opt/ibm/helpers/ 
# Fri, 25 Feb 2022 02:55:57 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 25 Feb 2022 02:55:58 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=de0dc0b4f90213bfa8bbe8a786af91504f78b1967775a31d46dc55ff14f2d171 NON_IBM_SHA=20a37b8cc381d969d985faebf766bfe5efa07b803d063e0f8739fbe571f43f87 NOTICES_SHA=eaa5532a956414b08a405c8fe78dd7295bfd1f37980b496dbe855def1432a659 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 25 Feb 2022 02:56:05 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=de0dc0b4f90213bfa8bbe8a786af91504f78b1967775a31d46dc55ff14f2d171 NON_IBM_SHA=20a37b8cc381d969d985faebf766bfe5efa07b803d063e0f8739fbe571f43f87 NOTICES_SHA=eaa5532a956414b08a405c8fe78dd7295bfd1f37980b496dbe855def1432a659 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 25 Feb 2022 02:56:06 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 25 Feb 2022 02:56:06 GMT
USER 1001
# Fri, 25 Feb 2022 02:56:06 GMT
EXPOSE 9080 9443
# Fri, 25 Feb 2022 02:56:06 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 25 Feb 2022 02:56:06 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 25 Feb 2022 02:57:08 GMT
ARG VERBOSE=false
# Fri, 25 Feb 2022 02:57:08 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 25 Feb 2022 03:01:31 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Fri, 25 Feb 2022 03:01:38 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 25 Feb 2022 03:02:02 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:cf002da3924024b39105dcc613288421b394e45e04d7a3c245ce5dcaf544dd98`  
		Last Modified: Wed, 02 Feb 2022 01:43:50 GMT  
		Size: 25.4 MB (25364307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4bcdb503991176c9486c76e56946053a4588fc20649c5465c056a465c592dee`  
		Last Modified: Wed, 02 Feb 2022 02:42:23 GMT  
		Size: 2.7 MB (2676856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2efbc3c7e039fae97f57de25d9911c5048feb8e0c8f76e1b1dab7aefa32fb69`  
		Last Modified: Wed, 23 Feb 2022 18:44:23 GMT  
		Size: 125.8 MB (125807341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44de3c59657aef0b761459ef653c7f1e0f84053eecaecf24a9829ebcefabdb4`  
		Last Modified: Fri, 25 Feb 2022 03:45:46 GMT  
		Size: 14.1 MB (14089228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc62f65e46df9a8013844316fa6197a744a0f0f95c24e4e7b8a59ae51cc562ab`  
		Last Modified: Fri, 25 Feb 2022 03:45:43 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c71d6f811c7e16b3de76058420edd31e62f74c84432a300c07957b3dcd300e`  
		Last Modified: Fri, 25 Feb 2022 03:45:44 GMT  
		Size: 9.7 KB (9680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa13ae32757492117a0a35f52632ba535b06aa488f42f584bb9457ddc56a928`  
		Last Modified: Fri, 25 Feb 2022 03:45:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9ec7536151f185397f98cf6e7b6ee70c51480a4dfbf8dfb1ba029dd615e4cc`  
		Last Modified: Fri, 25 Feb 2022 03:45:43 GMT  
		Size: 10.7 KB (10657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d6a0efd38340508a7ac0f1b73cdecf6f0608d6a9324dc55a319eddc36a479b`  
		Last Modified: Fri, 25 Feb 2022 03:45:44 GMT  
		Size: 5.9 MB (5918931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded8fa901d85f56d64afbd2ea96a16dcefe27d092e3fc776607464327c2cac3a`  
		Last Modified: Fri, 25 Feb 2022 03:46:15 GMT  
		Size: 268.4 MB (268392387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952776762a0d8d1f6bb31023bf0943dcc0332ff6f0498d7fc9f5c3a51bd6edba`  
		Last Modified: Fri, 25 Feb 2022 03:46:03 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4aa3fed3e5b43076d2ca241e8624b3d85cb1cae340143ea9ad4683a80ab46cf`  
		Last Modified: Fri, 25 Feb 2022 03:46:05 GMT  
		Size: 15.7 MB (15736150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
