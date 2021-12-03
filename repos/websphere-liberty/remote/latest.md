## `websphere-liberty:latest`

```console
$ docker pull websphere-liberty@sha256:83792a6610ef1aecbb71047a99802d27e22cef6d318a1fb83cf470f13ab54864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:latest` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:b176a6e50d5f986abc93266554c013007cff80793a7d337c5f1199fe4c8f0770
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.6 MB (404648546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb53cfd2204f22b76cf12dba78836282fa2589149a9840138f9205501c92a660`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:23 GMT
ADD file:0d82cd095966e8ee78b593cb47a352eec842edb7bd9d9468e8a70154522447d1 in / 
# Fri, 01 Oct 2021 02:23:24 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 02:55:25 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 01 Oct 2021 02:55:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 02:55:32 GMT
ENV JAVA_VERSION=8.0.6.36
# Fri, 01 Oct 2021 02:56:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='d0198a37b63810174dc972eb06976e3e761efb21524c1fa3f9f1ed1246f3a9e3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='05dddc6918557b3bf72ba48060e73804dcba692dfddeaaaee5551fcd3ac63915';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='48bbf5a656b06db138d79aeaecc4d63d86f133288d6c3e51084d1c2c5e9321b8';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='087140a55103a896ba134c82ef065fb9486b4de0a72a5f4f42f96f5728c68968';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='471b567c6f42291704020a77e0d1c219dcdefe0e0bfb85a9f0f3c8ecf66a1161';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 01 Oct 2021 02:56:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 01 Oct 2021 07:13:40 GMT
ARG VERBOSE=false
# Fri, 01 Oct 2021 07:13:40 GMT
ARG OPENJ9_SCC=true
# Wed, 10 Nov 2021 03:49:03 GMT
ARG EN_SHA=39558bcbc71aaa5c1489bc482387f8990e92f243d44947040ea42bde14570307
# Wed, 10 Nov 2021 03:49:03 GMT
ARG NON_IBM_SHA=da12daa83c49b6717a96130ba4c5ef693afe9128eee45f4d0a93aa5c4ae7049f
# Wed, 10 Nov 2021 03:49:03 GMT
ARG NOTICES_SHA=30b744fc9c35a76a5054af78e635a67188b8971d8649bbce95498af9c029a8c6
# Wed, 10 Nov 2021 03:49:03 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.11 org.opencontainers.image.revision=cl21.0.0.11920-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 10 Nov 2021 03:49:03 GMT
ENV LIBERTY_VERSION=21.0.0_11
# Wed, 10 Nov 2021 03:49:04 GMT
ARG LIBERTY_URL
# Wed, 10 Nov 2021 03:49:04 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 10 Nov 2021 03:49:17 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=39558bcbc71aaa5c1489bc482387f8990e92f243d44947040ea42bde14570307 NON_IBM_SHA=da12daa83c49b6717a96130ba4c5ef693afe9128eee45f4d0a93aa5c4ae7049f NOTICES_SHA=30b744fc9c35a76a5054af78e635a67188b8971d8649bbce95498af9c029a8c6 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 03:49:18 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Nov 2021 03:49:18 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.11 BuildLabel=cl21.0.0.11920-1900
# Wed, 10 Nov 2021 03:49:18 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 10 Nov 2021 03:49:20 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=39558bcbc71aaa5c1489bc482387f8990e92f243d44947040ea42bde14570307 NON_IBM_SHA=da12daa83c49b6717a96130ba4c5ef693afe9128eee45f4d0a93aa5c4ae7049f NOTICES_SHA=30b744fc9c35a76a5054af78e635a67188b8971d8649bbce95498af9c029a8c6 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 10 Nov 2021 03:49:20 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Wed, 10 Nov 2021 03:49:20 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 10 Nov 2021 03:49:21 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=39558bcbc71aaa5c1489bc482387f8990e92f243d44947040ea42bde14570307 NON_IBM_SHA=da12daa83c49b6717a96130ba4c5ef693afe9128eee45f4d0a93aa5c4ae7049f NOTICES_SHA=30b744fc9c35a76a5054af78e635a67188b8971d8649bbce95498af9c029a8c6 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 10 Nov 2021 03:49:34 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=39558bcbc71aaa5c1489bc482387f8990e92f243d44947040ea42bde14570307 NON_IBM_SHA=da12daa83c49b6717a96130ba4c5ef693afe9128eee45f4d0a93aa5c4ae7049f NOTICES_SHA=30b744fc9c35a76a5054af78e635a67188b8971d8649bbce95498af9c029a8c6 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 10 Nov 2021 03:49:34 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 10 Nov 2021 03:49:34 GMT
USER 1001
# Wed, 10 Nov 2021 03:49:34 GMT
EXPOSE 9080 9443
# Wed, 10 Nov 2021 03:49:35 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 10 Nov 2021 03:49:35 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 10 Nov 2021 03:50:17 GMT
ARG VERBOSE=false
# Wed, 10 Nov 2021 03:50:17 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 10 Nov 2021 03:53:24 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Wed, 10 Nov 2021 03:53:25 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 10 Nov 2021 03:54:48 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:284055322776031bac33723839acb0db2d063a525ba4fa1fd268a831c7553b26`  
		Last Modified: Fri, 01 Oct 2021 02:25:02 GMT  
		Size: 26.7 MB (26705075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf7ef5b4a4700901695d7489ffa25c9a36a0c54f7003664412a2a582dd362fa`  
		Last Modified: Fri, 01 Oct 2021 02:59:16 GMT  
		Size: 3.0 MB (2959872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58286f2e604db89582fc1898b2d2a229d5920927e7705c94e32f38a70e29902e`  
		Last Modified: Fri, 01 Oct 2021 02:59:26 GMT  
		Size: 128.4 MB (128395032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6e8f3a2feed44c8101a548a6e20c145f39b16e25f78957bb49283e33108172`  
		Last Modified: Wed, 10 Nov 2021 04:19:09 GMT  
		Size: 14.1 MB (14066584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83171950e9149fe8e935a005ab8c8705ec3896a4407fda19eaaa16587004fd27`  
		Last Modified: Wed, 10 Nov 2021 04:19:05 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61983426e42e616abc61cd996dc257151b4131a6fa8d64caccd04daa6624b32`  
		Last Modified: Wed, 10 Nov 2021 04:19:05 GMT  
		Size: 9.7 KB (9676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3c35fe983d8651227e07d718def11b6808a7859b41ed9e04be75a11c54bb8f`  
		Last Modified: Wed, 10 Nov 2021 04:19:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d38b30e71508384be9b62a3b694f369d89c45f456e1d187155ac7f3136e774`  
		Last Modified: Wed, 10 Nov 2021 04:19:05 GMT  
		Size: 10.7 KB (10666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6689586c1b5a6064371258ee769aa63497d4d799cc863141df4d275d43c2e3b0`  
		Last Modified: Wed, 10 Nov 2021 04:19:06 GMT  
		Size: 5.9 MB (5898752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4317aaf7fb6eeafa027aa24e646f09e732067b6c78061fc43d730c954f70aad2`  
		Last Modified: Wed, 10 Nov 2021 04:19:37 GMT  
		Size: 210.5 MB (210479779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26fe792562fe49b013681b294f57ed8ab2538d8ebfcf0ad23750fcf7bb9cf5f0`  
		Last Modified: Wed, 10 Nov 2021 04:19:26 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bce07d01557c690ae2132d296ee54898a02cf8f05fa2af09ed7ced6f1bfb677`  
		Last Modified: Wed, 10 Nov 2021 04:19:29 GMT  
		Size: 16.1 MB (16121184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:latest` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:dd237787f899f2a9fc46852bdce0d1bacd18dbf45de0723407ad3661f0b8180c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.8 MB (404807553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9c43a7dc5cfc1b2110867843df94999ea833bcb58c4c1be0604fd62bf64e1ce`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 05 Oct 2021 11:07:29 GMT
ADD file:fd96554dfb72307c3cf9292c343050a8b9f0848735b7555820f0068914ebd758 in / 
# Tue, 05 Oct 2021 11:07:35 GMT
CMD ["bash"]
# Wed, 06 Oct 2021 17:55:28 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 06 Oct 2021 17:56:05 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 17:56:16 GMT
ENV JAVA_VERSION=8.0.6.36
# Wed, 06 Oct 2021 17:57:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='d0198a37b63810174dc972eb06976e3e761efb21524c1fa3f9f1ed1246f3a9e3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='05dddc6918557b3bf72ba48060e73804dcba692dfddeaaaee5551fcd3ac63915';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='48bbf5a656b06db138d79aeaecc4d63d86f133288d6c3e51084d1c2c5e9321b8';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='087140a55103a896ba134c82ef065fb9486b4de0a72a5f4f42f96f5728c68968';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='471b567c6f42291704020a77e0d1c219dcdefe0e0bfb85a9f0f3c8ecf66a1161';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 Oct 2021 17:57:38 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Thu, 07 Oct 2021 10:35:31 GMT
ARG VERBOSE=false
# Thu, 07 Oct 2021 10:35:33 GMT
ARG OPENJ9_SCC=true
# Wed, 10 Nov 2021 07:44:54 GMT
ARG EN_SHA=39558bcbc71aaa5c1489bc482387f8990e92f243d44947040ea42bde14570307
# Wed, 10 Nov 2021 07:44:58 GMT
ARG NON_IBM_SHA=da12daa83c49b6717a96130ba4c5ef693afe9128eee45f4d0a93aa5c4ae7049f
# Wed, 10 Nov 2021 07:45:00 GMT
ARG NOTICES_SHA=30b744fc9c35a76a5054af78e635a67188b8971d8649bbce95498af9c029a8c6
# Wed, 10 Nov 2021 07:45:02 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.11 org.opencontainers.image.revision=cl21.0.0.11920-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 10 Nov 2021 07:45:05 GMT
ENV LIBERTY_VERSION=21.0.0_11
# Wed, 10 Nov 2021 07:45:08 GMT
ARG LIBERTY_URL
# Wed, 10 Nov 2021 07:45:12 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 10 Nov 2021 07:46:02 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=39558bcbc71aaa5c1489bc482387f8990e92f243d44947040ea42bde14570307 NON_IBM_SHA=da12daa83c49b6717a96130ba4c5ef693afe9128eee45f4d0a93aa5c4ae7049f NOTICES_SHA=30b744fc9c35a76a5054af78e635a67188b8971d8649bbce95498af9c029a8c6 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 10 Nov 2021 07:46:14 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Nov 2021 07:46:19 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.11 BuildLabel=cl21.0.0.11920-1900
# Wed, 10 Nov 2021 07:46:21 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 10 Nov 2021 07:46:41 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=39558bcbc71aaa5c1489bc482387f8990e92f243d44947040ea42bde14570307 NON_IBM_SHA=da12daa83c49b6717a96130ba4c5ef693afe9128eee45f4d0a93aa5c4ae7049f NOTICES_SHA=30b744fc9c35a76a5054af78e635a67188b8971d8649bbce95498af9c029a8c6 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 10 Nov 2021 07:46:43 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Wed, 10 Nov 2021 07:46:44 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 10 Nov 2021 07:46:57 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=39558bcbc71aaa5c1489bc482387f8990e92f243d44947040ea42bde14570307 NON_IBM_SHA=da12daa83c49b6717a96130ba4c5ef693afe9128eee45f4d0a93aa5c4ae7049f NOTICES_SHA=30b744fc9c35a76a5054af78e635a67188b8971d8649bbce95498af9c029a8c6 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 10 Nov 2021 07:47:18 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=39558bcbc71aaa5c1489bc482387f8990e92f243d44947040ea42bde14570307 NON_IBM_SHA=da12daa83c49b6717a96130ba4c5ef693afe9128eee45f4d0a93aa5c4ae7049f NOTICES_SHA=30b744fc9c35a76a5054af78e635a67188b8971d8649bbce95498af9c029a8c6 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 10 Nov 2021 07:47:22 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 10 Nov 2021 07:47:25 GMT
USER 1001
# Wed, 10 Nov 2021 07:47:27 GMT
EXPOSE 9080 9443
# Wed, 10 Nov 2021 07:47:28 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 10 Nov 2021 07:47:31 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 10 Nov 2021 07:50:29 GMT
ARG VERBOSE=false
# Wed, 10 Nov 2021 07:50:30 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 10 Nov 2021 07:54:08 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Wed, 10 Nov 2021 07:54:16 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 10 Nov 2021 07:55:22 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:db28fc1e594e5598e665c54ac1b7fd602d86dddaf8bb237a72303cec22a9185c`  
		Last Modified: Tue, 05 Oct 2021 11:10:31 GMT  
		Size: 30.4 MB (30432921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce6e130fd3d09fd3fe6d741e0fa3f77120aa82717cf6d0a1cb49439939243a6`  
		Last Modified: Wed, 06 Oct 2021 18:04:08 GMT  
		Size: 3.1 MB (3081580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8fc8962750bc0e8c7c6ca6d1498e303c66e1f0b3f9613d204da9abf0200933`  
		Last Modified: Wed, 06 Oct 2021 18:04:22 GMT  
		Size: 127.9 MB (127898987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb219dde7179a7f7b997ff6ee756e1df764baa53e4df37889ce6089aecfd5485`  
		Last Modified: Wed, 10 Nov 2021 08:32:58 GMT  
		Size: 14.1 MB (14067094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec5e223b75b5c9e29be437538ab22d9bb413050f74cd38fd737b1c2d2d1e602`  
		Last Modified: Wed, 10 Nov 2021 08:32:51 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9187fac23d5c3c572740429a27c7e38a546dd0118e4643e84a8798b7b9255d1`  
		Last Modified: Wed, 10 Nov 2021 08:32:51 GMT  
		Size: 9.7 KB (9675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d781b79a8fd921cb9b87312ed1170dd29bd2217a8fb20ac778a0bae0c324036`  
		Last Modified: Wed, 10 Nov 2021 08:32:51 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3039aa0ef084aeb735e320d6971dc1e0753bcf10b1b0f8b5490855d47af19f83`  
		Last Modified: Wed, 10 Nov 2021 08:32:51 GMT  
		Size: 10.7 KB (10673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253dbdca69d40e699608cedc144c8092d1fdae2239871957cfc40c6577cb29a1`  
		Last Modified: Wed, 10 Nov 2021 08:32:53 GMT  
		Size: 5.3 MB (5348213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa216c14173a7f93c6828b9279333c1c977e935989cec75fad7818b2138b1d0`  
		Last Modified: Wed, 10 Nov 2021 08:33:39 GMT  
		Size: 210.5 MB (210479708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fdcfc44b4353d1ffa8dc4bfd8cc5406d32f73b3edb3a272e73a42e4798d629`  
		Last Modified: Wed, 10 Nov 2021 08:33:18 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267708dff2baadb443f51412e217022daa67edff154a4ac9cd83a3c527e9b604`  
		Last Modified: Wed, 10 Nov 2021 08:33:22 GMT  
		Size: 13.5 MB (13476776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:latest` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:69031b2a4d9d276d36fdc1a5097d6ed1db5286a0ab0aa6ecb024f0acb04b3fbd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.3 MB (454312810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001806a1602bfeb66a8bb976d8812c6056392a52963a60f4b6f5d380eaa42db1`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 01 Oct 2021 01:42:17 GMT
ADD file:d248d4b5739ee5d07e920ec481dc4af81b314aa52e64618322197a642394a41d in / 
# Fri, 01 Oct 2021 01:42:19 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 02:23:32 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 01 Oct 2021 02:23:36 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Mon, 29 Nov 2021 20:00:19 GMT
ENV JAVA_VERSION=8.0.7.0
# Mon, 29 Nov 2021 20:00:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='18d56640102a5e6b1326cc762dbf9ae19f00f81574f38ae1857d9f65761123ff';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='24af7fb9be209a68314dc341e5b62284d3625567872286f484cb296b9c551974';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='75ccfbaf6526ab854e193060110a9bef7878d186a95c3e0d57448ab96c09aa1a';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='200621b68eb39ae00ee875b31d6455bb2dcc5c8d050a4e4f8aa4fc7525a53d35';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='73f941590d60287d9d480884698120149bf2f9b8da04d2501b450f320a5be181';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Mon, 29 Nov 2021 20:01:01 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Mon, 29 Nov 2021 20:46:01 GMT
ARG VERBOSE=false
# Mon, 29 Nov 2021 20:46:01 GMT
ARG OPENJ9_SCC=true
# Fri, 03 Dec 2021 01:31:21 GMT
ARG EN_SHA=3e0b8b39a5c8000b0ad1458943454d8ad2e4b4712030cd0f96846a0aa1090078
# Fri, 03 Dec 2021 01:31:21 GMT
ARG NON_IBM_SHA=66d73b0d3e0cb314134e9fee966dbda6c388bf33645583921f63e00851242ff2
# Fri, 03 Dec 2021 01:31:21 GMT
ARG NOTICES_SHA=30a37bfd567f61c63daf4726d95ee3bf6d1c5f2b885678af4d52e44fa2f93e54
# Fri, 03 Dec 2021 01:31:22 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.12 org.opencontainers.image.revision=cl21.0.0.12920-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 03 Dec 2021 01:31:22 GMT
ENV LIBERTY_VERSION=21.0.0_12
# Fri, 03 Dec 2021 01:31:22 GMT
ARG LIBERTY_URL
# Fri, 03 Dec 2021 01:31:22 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 03 Dec 2021 01:31:34 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=3e0b8b39a5c8000b0ad1458943454d8ad2e4b4712030cd0f96846a0aa1090078 NON_IBM_SHA=66d73b0d3e0cb314134e9fee966dbda6c388bf33645583921f63e00851242ff2 NOTICES_SHA=30a37bfd567f61c63daf4726d95ee3bf6d1c5f2b885678af4d52e44fa2f93e54 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 01:31:34 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 01:31:34 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.12 BuildLabel=cl21.0.0.12920-1900
# Fri, 03 Dec 2021 01:31:34 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 03 Dec 2021 01:31:36 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=3e0b8b39a5c8000b0ad1458943454d8ad2e4b4712030cd0f96846a0aa1090078 NON_IBM_SHA=66d73b0d3e0cb314134e9fee966dbda6c388bf33645583921f63e00851242ff2 NOTICES_SHA=30a37bfd567f61c63daf4726d95ee3bf6d1c5f2b885678af4d52e44fa2f93e54 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 03 Dec 2021 01:31:36 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Fri, 03 Dec 2021 01:31:36 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 03 Dec 2021 01:31:37 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=3e0b8b39a5c8000b0ad1458943454d8ad2e4b4712030cd0f96846a0aa1090078 NON_IBM_SHA=66d73b0d3e0cb314134e9fee966dbda6c388bf33645583921f63e00851242ff2 NOTICES_SHA=30a37bfd567f61c63daf4726d95ee3bf6d1c5f2b885678af4d52e44fa2f93e54 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 03 Dec 2021 01:31:44 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=3e0b8b39a5c8000b0ad1458943454d8ad2e4b4712030cd0f96846a0aa1090078 NON_IBM_SHA=66d73b0d3e0cb314134e9fee966dbda6c388bf33645583921f63e00851242ff2 NOTICES_SHA=30a37bfd567f61c63daf4726d95ee3bf6d1c5f2b885678af4d52e44fa2f93e54 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 03 Dec 2021 01:31:45 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 03 Dec 2021 01:31:45 GMT
USER 1001
# Fri, 03 Dec 2021 01:31:45 GMT
EXPOSE 9080 9443
# Fri, 03 Dec 2021 01:31:45 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 03 Dec 2021 01:31:45 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 03 Dec 2021 01:32:20 GMT
ARG VERBOSE=false
# Fri, 03 Dec 2021 01:32:20 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 03 Dec 2021 01:36:35 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Fri, 03 Dec 2021 01:36:41 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 03 Dec 2021 01:37:05 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:97372e5b313b6b8bab9913de546bc50f73818d8275c94fc6491993c97b9d8bad`  
		Last Modified: Fri, 01 Oct 2021 01:43:49 GMT  
		Size: 25.4 MB (25362918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf425722012c2264c66ba97a53ff25a2f196330fbcc0872474e5e4562fa95f0`  
		Last Modified: Fri, 01 Oct 2021 02:27:43 GMT  
		Size: 2.7 MB (2676365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede8c251d47c91dd474c4cf5f7999def5ff3617e4865b8adceefa0c32d11395d`  
		Last Modified: Mon, 29 Nov 2021 20:03:23 GMT  
		Size: 125.7 MB (125737330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a99a0d5574284cb8d11eb5a5ab186146924e0d423984411481264f6ae77cf8f`  
		Last Modified: Fri, 03 Dec 2021 01:43:15 GMT  
		Size: 14.2 MB (14187170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30794f21393a8a943888f0fb89535a924242b8308ce676d95f753306daf4919a`  
		Last Modified: Fri, 03 Dec 2021 01:43:13 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2ce444eb0a71dfb09656562c8ea04fda52c8ee6949c21c553d3233f765d6b1`  
		Last Modified: Fri, 03 Dec 2021 01:43:13 GMT  
		Size: 9.7 KB (9675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a93942d381a7a45ea0f1acae8ce1978b65f8cff3e5b5e855f0c21ee2926598b`  
		Last Modified: Fri, 03 Dec 2021 01:43:13 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aff798a08db60b191b5c3c1b5e7c8d2eb28c25ee99c23cb3b6712f846818a11`  
		Last Modified: Fri, 03 Dec 2021 01:43:13 GMT  
		Size: 10.7 KB (10652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ce740f69ad70aa57d138d57b783894e5dff791306052beabc2c9672486968f`  
		Last Modified: Fri, 03 Dec 2021 01:43:14 GMT  
		Size: 5.8 MB (5795276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906d13ed98eeb042451e88210ef2af96abbfd537c9d4c4d79349770656a1887e`  
		Last Modified: Fri, 03 Dec 2021 01:43:37 GMT  
		Size: 264.6 MB (264635120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7897eba620c785124634c25befdb033e0ee7dc473a3aa35c930a15f9165edc6`  
		Last Modified: Fri, 03 Dec 2021 01:43:26 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdcbd816cdab9a024928e7efd5aefd485a62051b1ae6ee4d30d743765cc1fbe`  
		Last Modified: Fri, 03 Dec 2021 01:43:28 GMT  
		Size: 15.9 MB (15896379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
