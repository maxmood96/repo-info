## `websphere-liberty:latest`

```console
$ docker pull websphere-liberty@sha256:938c3c4ce8a4004c966ac8e7424f2bb0e559ddce247c0df797ffa2c0affbc6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:latest` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:435ee126d903bf9e1eb1e92c291748880b0aaf4d1d9f9d9d58c87f26062e0fbc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **519.3 MB (519338586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6376e988ee1eb28023a7989abe9e702b7cae3f5f47af28126bb7f1305dca5d`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 08 Mar 2023 03:22:42 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:22:44 GMT
ADD file:4560926e076acae6b8396a9f1e760eee0f53e22e90ce8554dda57f1103547795 in / 
# Wed, 08 Mar 2023 03:22:44 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:36:37 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 16 Mar 2023 03:36:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:36:47 GMT
ENV JAVA_VERSION=8.0.7.20
# Thu, 16 Mar 2023 03:37:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 16 Mar 2023 03:37:44 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Thu, 16 Mar 2023 09:36:18 GMT
ARG VERBOSE=false
# Thu, 16 Mar 2023 09:36:18 GMT
ARG OPENJ9_SCC=true
# Thu, 16 Mar 2023 09:36:18 GMT
ARG EN_SHA=2d77600f393a32877305f82957968c41d1e140ad4ebd3a2c07f5d77f601d5614
# Thu, 16 Mar 2023 09:36:18 GMT
ARG NON_IBM_SHA=565db37df01346ca4f611c4fc58431e845f1c4002908e1a4c696230d7f396d9c
# Thu, 16 Mar 2023 09:36:18 GMT
ARG NOTICES_SHA=c08df1e3fdf99be6f02fcf458e4533119a4785a92994d5950528f02f349ada4b
# Thu, 16 Mar 2023 09:36:18 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=23.0.0.2 org.opencontainers.image.revision=cl230220230222-1257 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 16 Mar 2023 09:36:18 GMT
ENV LIBERTY_VERSION=23.0.0_2
# Thu, 16 Mar 2023 09:36:18 GMT
ARG LIBERTY_URL
# Thu, 16 Mar 2023 09:36:18 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 16 Mar 2023 09:36:36 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2d77600f393a32877305f82957968c41d1e140ad4ebd3a2c07f5d77f601d5614 NON_IBM_SHA=565db37df01346ca4f611c4fc58431e845f1c4002908e1a4c696230d7f396d9c NOTICES_SHA=c08df1e3fdf99be6f02fcf458e4533119a4785a92994d5950528f02f349ada4b OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 09:36:36 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Thu, 16 Mar 2023 09:36:36 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=23.0.0.2 BuildLabel=cl230220230222-1257
# Thu, 16 Mar 2023 09:36:37 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 16 Mar 2023 09:36:38 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2d77600f393a32877305f82957968c41d1e140ad4ebd3a2c07f5d77f601d5614 NON_IBM_SHA=565db37df01346ca4f611c4fc58431e845f1c4002908e1a4c696230d7f396d9c NOTICES_SHA=c08df1e3fdf99be6f02fcf458e4533119a4785a92994d5950528f02f349ada4b VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 16 Mar 2023 09:36:38 GMT
COPY dir:0f3e336b1e5adb84a625050153035561e1c9802a57b7b90b5a17ebb82adba489 in /opt/ibm/helpers/ 
# Thu, 16 Mar 2023 09:36:38 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 16 Mar 2023 09:36:39 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2d77600f393a32877305f82957968c41d1e140ad4ebd3a2c07f5d77f601d5614 NON_IBM_SHA=565db37df01346ca4f611c4fc58431e845f1c4002908e1a4c696230d7f396d9c NOTICES_SHA=c08df1e3fdf99be6f02fcf458e4533119a4785a92994d5950528f02f349ada4b VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 16 Mar 2023 09:36:46 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2d77600f393a32877305f82957968c41d1e140ad4ebd3a2c07f5d77f601d5614 NON_IBM_SHA=565db37df01346ca4f611c4fc58431e845f1c4002908e1a4c696230d7f396d9c NOTICES_SHA=c08df1e3fdf99be6f02fcf458e4533119a4785a92994d5950528f02f349ada4b VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 16 Mar 2023 09:36:46 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Thu, 16 Mar 2023 09:36:46 GMT
USER 1001
# Thu, 16 Mar 2023 09:36:46 GMT
EXPOSE 9080 9443
# Thu, 16 Mar 2023 09:36:46 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 16 Mar 2023 09:36:46 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 16 Mar 2023 09:37:49 GMT
ARG VERBOSE=false
# Thu, 16 Mar 2023 09:37:49 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 16 Mar 2023 09:46:10 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Thu, 16 Mar 2023 09:46:11 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Thu, 16 Mar 2023 09:46:40 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:cd150c608fee7837e3a5b28be5c7b540eaf4efa27b3b755d55326470691ce2df`  
		Last Modified: Sun, 12 Mar 2023 07:24:55 GMT  
		Size: 26.7 MB (26710746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe43ddc3a069d2f66d64b9128ad2efde0e85efb6f720a7c7be3af6c784fe4211`  
		Last Modified: Thu, 16 Mar 2023 03:40:10 GMT  
		Size: 3.0 MB (2952384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53675c23cb3388a8e2418ba7a5a3f50b9e98313c6f68ae7895f0d2bd0774facc`  
		Last Modified: Thu, 16 Mar 2023 03:40:19 GMT  
		Size: 129.3 MB (129322656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40bae45b36272ea5da0e78b700f056d21c32b49b26d0f350e56118b4895f4d72`  
		Last Modified: Thu, 16 Mar 2023 11:02:25 GMT  
		Size: 14.3 MB (14344428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ee209749be34f97c6e4d1ecc6c955121bab5d5f3dbfd6621a3c1a9da73928`  
		Last Modified: Thu, 16 Mar 2023 11:02:21 GMT  
		Size: 684.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4114d8389bfb0c256917b7ae4638e3e99743241c8f496abcaefbaa61082be4`  
		Last Modified: Thu, 16 Mar 2023 11:02:21 GMT  
		Size: 9.8 KB (9818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827f0b947425dcff775801d2ac2826cd4d98bb2100ab4f17b297f40c4ef91c90`  
		Last Modified: Thu, 16 Mar 2023 11:02:22 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f168039a095b80b7c1279a2e64fe02919a1ea6e57d161fdd30fc124aba986f`  
		Last Modified: Thu, 16 Mar 2023 11:02:22 GMT  
		Size: 10.8 KB (10801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b75a36f0f027f8546046ceca132ed512e2345af23685689689a80af9c520cae`  
		Last Modified: Thu, 16 Mar 2023 11:02:22 GMT  
		Size: 5.9 MB (5896556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2f10c17938db546373a4ac0ea1216316193832cf1abcb4bbebbeee5aca4e545`  
		Last Modified: Thu, 16 Mar 2023 11:03:04 GMT  
		Size: 324.0 MB (324041160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7badae3c86852c0d2d4bbad0ff9955b63a79707a4e6dd2a7b4c275f6eeadc9f8`  
		Last Modified: Thu, 16 Mar 2023 11:02:49 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f72899855010c453877986179454e7d55716d590467b5f4c75add128f56213b`  
		Last Modified: Thu, 16 Mar 2023 11:02:51 GMT  
		Size: 16.0 MB (16048131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:latest` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:170641a910e4ee4e3721c3776d321adaac258da7631a1b8fa4ccba63c0f60b3e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.3 MB (520264830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1898e3aee52a9a25eeaac0a1342506d78e4c3e22b256a20f2e217a657430d730`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 08 Mar 2023 03:13:23 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:13:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:13:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:13:23 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:13:26 GMT
ADD file:5ea8615c09f693252cb9d45458421679f82f84d315200a7611165869195b3a69 in / 
# Wed, 08 Mar 2023 03:13:26 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:34:29 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 16 Mar 2023 01:34:56 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:34:57 GMT
ENV JAVA_VERSION=8.0.7.20
# Thu, 16 Mar 2023 01:37:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 16 Mar 2023 01:37:07 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Thu, 16 Mar 2023 04:38:52 GMT
ARG VERBOSE=false
# Thu, 16 Mar 2023 04:38:52 GMT
ARG OPENJ9_SCC=true
# Thu, 16 Mar 2023 04:38:53 GMT
ARG EN_SHA=2d77600f393a32877305f82957968c41d1e140ad4ebd3a2c07f5d77f601d5614
# Thu, 16 Mar 2023 04:38:53 GMT
ARG NON_IBM_SHA=565db37df01346ca4f611c4fc58431e845f1c4002908e1a4c696230d7f396d9c
# Thu, 16 Mar 2023 04:38:53 GMT
ARG NOTICES_SHA=c08df1e3fdf99be6f02fcf458e4533119a4785a92994d5950528f02f349ada4b
# Thu, 16 Mar 2023 04:38:54 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=23.0.0.2 org.opencontainers.image.revision=cl230220230222-1257 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 16 Mar 2023 04:38:54 GMT
ENV LIBERTY_VERSION=23.0.0_2
# Thu, 16 Mar 2023 04:38:54 GMT
ARG LIBERTY_URL
# Thu, 16 Mar 2023 04:38:55 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 16 Mar 2023 04:39:31 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2d77600f393a32877305f82957968c41d1e140ad4ebd3a2c07f5d77f601d5614 NON_IBM_SHA=565db37df01346ca4f611c4fc58431e845f1c4002908e1a4c696230d7f396d9c NOTICES_SHA=c08df1e3fdf99be6f02fcf458e4533119a4785a92994d5950528f02f349ada4b OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:39:32 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Thu, 16 Mar 2023 04:39:32 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=23.0.0.2 BuildLabel=cl230220230222-1257
# Thu, 16 Mar 2023 04:39:32 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 16 Mar 2023 04:39:36 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2d77600f393a32877305f82957968c41d1e140ad4ebd3a2c07f5d77f601d5614 NON_IBM_SHA=565db37df01346ca4f611c4fc58431e845f1c4002908e1a4c696230d7f396d9c NOTICES_SHA=c08df1e3fdf99be6f02fcf458e4533119a4785a92994d5950528f02f349ada4b VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 16 Mar 2023 04:39:37 GMT
COPY dir:0f3e336b1e5adb84a625050153035561e1c9802a57b7b90b5a17ebb82adba489 in /opt/ibm/helpers/ 
# Thu, 16 Mar 2023 04:39:37 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 16 Mar 2023 04:39:39 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2d77600f393a32877305f82957968c41d1e140ad4ebd3a2c07f5d77f601d5614 NON_IBM_SHA=565db37df01346ca4f611c4fc58431e845f1c4002908e1a4c696230d7f396d9c NOTICES_SHA=c08df1e3fdf99be6f02fcf458e4533119a4785a92994d5950528f02f349ada4b VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 16 Mar 2023 04:39:54 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2d77600f393a32877305f82957968c41d1e140ad4ebd3a2c07f5d77f601d5614 NON_IBM_SHA=565db37df01346ca4f611c4fc58431e845f1c4002908e1a4c696230d7f396d9c NOTICES_SHA=c08df1e3fdf99be6f02fcf458e4533119a4785a92994d5950528f02f349ada4b VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 16 Mar 2023 04:39:55 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Thu, 16 Mar 2023 04:39:55 GMT
USER 1001
# Thu, 16 Mar 2023 04:39:56 GMT
EXPOSE 9080 9443
# Thu, 16 Mar 2023 04:39:57 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 16 Mar 2023 04:39:57 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 16 Mar 2023 04:42:40 GMT
ARG VERBOSE=false
# Thu, 16 Mar 2023 04:42:40 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 16 Mar 2023 04:59:10 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Thu, 16 Mar 2023 04:59:16 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Thu, 16 Mar 2023 05:00:12 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:1c668e1b654ae9320eeecdef5ebc0faea219f3828f6cd3a05983984863b60058`  
		Last Modified: Thu, 16 Mar 2023 01:43:01 GMT  
		Size: 30.4 MB (30441944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a045bec75deb795fa894947efc21348c99f3e44cd0e657cf75429ed5eede9b51`  
		Last Modified: Thu, 16 Mar 2023 01:42:54 GMT  
		Size: 3.1 MB (3077290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34c33fe5fa53db198926168e620634620a106f3d43c3197b8bc2bbe668eea0e`  
		Last Modified: Thu, 16 Mar 2023 01:43:09 GMT  
		Size: 129.0 MB (128996421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9158a61beb0c5222b052ff511c8e0e7f98000920d7e59f197ce75d7023141ca`  
		Last Modified: Thu, 16 Mar 2023 07:21:47 GMT  
		Size: 14.3 MB (14344725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71019f6c54493154cff2524b84b6060ad3f00e54e0697fbe8ae68866155a11cb`  
		Last Modified: Thu, 16 Mar 2023 07:21:43 GMT  
		Size: 685.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fbfe2558a601e3d480784b033df01462a7e95f9f824de2bd2b98dfe95e0f7aa`  
		Last Modified: Thu, 16 Mar 2023 07:21:43 GMT  
		Size: 9.8 KB (9819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d105bd31b4b51cdfd46ba2a4e5dfcafdf659b75f3c8ee72b05eaf753c06663e`  
		Last Modified: Thu, 16 Mar 2023 07:21:43 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a1ebe08c6c0d1406396901eb3b4a22320441afe25c23f9c926c769ae3341be`  
		Last Modified: Thu, 16 Mar 2023 07:21:43 GMT  
		Size: 10.8 KB (10811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9ac2db771bb876fa04f4bd18f50f20b049e9527c7df978efa7be31ec491563`  
		Last Modified: Thu, 16 Mar 2023 07:21:44 GMT  
		Size: 5.5 MB (5502316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc1efc54f9d503992778ee8f3fec14de9d241745547269a9d8a9ac2b28e0dc92`  
		Last Modified: Thu, 16 Mar 2023 07:22:43 GMT  
		Size: 324.0 MB (324041919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:763c7bf462f8cdb9c46e08a4b74de397e06ab8ebda677b4b0e71e6c16deb3b15`  
		Last Modified: Thu, 16 Mar 2023 07:22:17 GMT  
		Size: 951.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75775dba606fa8f9b5f53eec7ff8c95cd42079d46ece105e31bbf54405a4966`  
		Last Modified: Thu, 16 Mar 2023 07:22:20 GMT  
		Size: 13.8 MB (13837674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:latest` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:1536bd3c47f58db4a215916e9668e934282971a1d35c24c66dd5281de2db8271
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.8 MB (514786064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd87e9b92ec7c6463f61235e650dabff00ac2dcac7d35ed51a98f27b6dd01b1`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 08 Mar 2023 03:23:29 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:23:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:23:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:23:29 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:23:31 GMT
ADD file:a6309e462d28398152cb726a11615118d79858da963b8c614772b87d87465967 in / 
# Wed, 08 Mar 2023 03:23:31 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:38:18 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 16 Mar 2023 02:38:24 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:38:24 GMT
ENV JAVA_VERSION=8.0.7.20
# Thu, 16 Mar 2023 02:39:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 16 Mar 2023 02:39:42 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Thu, 16 Mar 2023 19:34:49 GMT
ARG VERBOSE=false
# Thu, 16 Mar 2023 19:34:49 GMT
ARG OPENJ9_SCC=true
# Thu, 16 Mar 2023 19:34:50 GMT
ARG EN_SHA=2d77600f393a32877305f82957968c41d1e140ad4ebd3a2c07f5d77f601d5614
# Thu, 16 Mar 2023 19:34:50 GMT
ARG NON_IBM_SHA=565db37df01346ca4f611c4fc58431e845f1c4002908e1a4c696230d7f396d9c
# Thu, 16 Mar 2023 19:34:50 GMT
ARG NOTICES_SHA=c08df1e3fdf99be6f02fcf458e4533119a4785a92994d5950528f02f349ada4b
# Thu, 16 Mar 2023 19:34:50 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=23.0.0.2 org.opencontainers.image.revision=cl230220230222-1257 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 16 Mar 2023 19:34:50 GMT
ENV LIBERTY_VERSION=23.0.0_2
# Thu, 16 Mar 2023 19:34:50 GMT
ARG LIBERTY_URL
# Thu, 16 Mar 2023 19:34:50 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 16 Mar 2023 19:35:07 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2d77600f393a32877305f82957968c41d1e140ad4ebd3a2c07f5d77f601d5614 NON_IBM_SHA=565db37df01346ca4f611c4fc58431e845f1c4002908e1a4c696230d7f396d9c NOTICES_SHA=c08df1e3fdf99be6f02fcf458e4533119a4785a92994d5950528f02f349ada4b OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 19:35:08 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Thu, 16 Mar 2023 19:35:08 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=23.0.0.2 BuildLabel=cl230220230222-1257
# Thu, 16 Mar 2023 19:35:08 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 16 Mar 2023 19:35:09 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2d77600f393a32877305f82957968c41d1e140ad4ebd3a2c07f5d77f601d5614 NON_IBM_SHA=565db37df01346ca4f611c4fc58431e845f1c4002908e1a4c696230d7f396d9c NOTICES_SHA=c08df1e3fdf99be6f02fcf458e4533119a4785a92994d5950528f02f349ada4b VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 16 Mar 2023 19:35:09 GMT
COPY dir:0f3e336b1e5adb84a625050153035561e1c9802a57b7b90b5a17ebb82adba489 in /opt/ibm/helpers/ 
# Thu, 16 Mar 2023 19:35:09 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 16 Mar 2023 19:35:10 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2d77600f393a32877305f82957968c41d1e140ad4ebd3a2c07f5d77f601d5614 NON_IBM_SHA=565db37df01346ca4f611c4fc58431e845f1c4002908e1a4c696230d7f396d9c NOTICES_SHA=c08df1e3fdf99be6f02fcf458e4533119a4785a92994d5950528f02f349ada4b VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 16 Mar 2023 19:35:16 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2d77600f393a32877305f82957968c41d1e140ad4ebd3a2c07f5d77f601d5614 NON_IBM_SHA=565db37df01346ca4f611c4fc58431e845f1c4002908e1a4c696230d7f396d9c NOTICES_SHA=c08df1e3fdf99be6f02fcf458e4533119a4785a92994d5950528f02f349ada4b VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 16 Mar 2023 19:35:16 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Thu, 16 Mar 2023 19:35:16 GMT
USER 1001
# Thu, 16 Mar 2023 19:35:16 GMT
EXPOSE 9080 9443
# Thu, 16 Mar 2023 19:35:16 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 16 Mar 2023 19:35:17 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 16 Mar 2023 19:36:15 GMT
ARG VERBOSE=false
# Thu, 16 Mar 2023 19:36:15 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 16 Mar 2023 19:45:17 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Thu, 16 Mar 2023 19:45:28 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Thu, 16 Mar 2023 19:45:51 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:3a2279f06ab19f0d57823e69b999f54a344e28bd9f955b4db9a5875c0caa543a`  
		Last Modified: Thu, 16 Mar 2023 02:01:03 GMT  
		Size: 25.4 MB (25370993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c6fa88382e166a9b693d8b861f913ff7b356af9dff894ad987e650a41f3335`  
		Last Modified: Thu, 16 Mar 2023 02:44:12 GMT  
		Size: 2.7 MB (2668974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01be997ed4400e0fe5d3afd8cadfefcdd5752b094e25e29a3d047c35b373d2d7`  
		Last Modified: Thu, 16 Mar 2023 02:44:20 GMT  
		Size: 126.5 MB (126472597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0986c81f63f353618ad6b3f4ede8b6deb9e6f8218d4b847134daed90cfce5f68`  
		Last Modified: Thu, 16 Mar 2023 21:18:55 GMT  
		Size: 14.3 MB (14344469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa9638737b00eafa71b23cc41e4641030e5549c2cc0b97f32f747e9188c865c`  
		Last Modified: Thu, 16 Mar 2023 21:18:53 GMT  
		Size: 679.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000f4759880c6c74f5121b6104580fd42ccb2acba66cd6949f20dfee2322206e`  
		Last Modified: Thu, 16 Mar 2023 21:18:53 GMT  
		Size: 9.8 KB (9814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdfff1aefbb5175877557ec5e542d4b3bff6cd862d03112a2c14f5149d18007`  
		Last Modified: Thu, 16 Mar 2023 21:18:53 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c262ad69c24a350f924115250c56015514f75b1212db446e10602897f6db9a8d`  
		Last Modified: Thu, 16 Mar 2023 21:18:53 GMT  
		Size: 10.8 KB (10802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798d8276544bf87989c8f9f2fd3b186c691bf6b662ec34d10b0352af5070e0ba`  
		Last Modified: Thu, 16 Mar 2023 21:18:54 GMT  
		Size: 6.1 MB (6071809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931cc96790e636c59a0c09745c087723d7a4064e0792cc453d87a29ff65f6470`  
		Last Modified: Thu, 16 Mar 2023 21:19:29 GMT  
		Size: 324.0 MB (324040903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48de2e15b8391e126abfd92e7d5b88bc261fe06451e358d2c4b3245434a1bfc1`  
		Last Modified: Thu, 16 Mar 2023 21:19:15 GMT  
		Size: 947.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00c19ec973bfdd798439d48f0e8b6163f3cc022cd009fb7fc1a9ebd79173a6f`  
		Last Modified: Thu, 16 Mar 2023 21:19:17 GMT  
		Size: 15.8 MB (15793805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
