## `websphere-liberty:kernel`

```console
$ docker pull websphere-liberty@sha256:fad12d811d7f5844d767a9adf4d8b7047c557a30e989cf35284d6c1ec689cdc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:kernel` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:c89859ea6f3fbe298e9ef7ff7471968b2a9ee8d8c7990c07445d2b113eff3de8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.0 MB (178951020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1f908e89b691de90792afcf4431fa3649b0de1a8b748362e3ce71ffcfc3d46`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 29 Apr 2022 23:20:51 GMT
ADD file:f657a56a18426c3a88d620a7024e7b91424d926e7b47faa6a97c2369c4c4a228 in / 
# Fri, 29 Apr 2022 23:20:51 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 01:06:17 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Sat, 30 Apr 2022 01:06:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 01:06:25 GMT
ENV JAVA_VERSION=8.0.7.6
# Sat, 30 Apr 2022 01:06:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='04b9e508ec9d206296b4972f1e122a168fc5f2524f7606ec3ade6600cef193a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='d0fa8483f91717a478d3ae8cca82c8934966a7603287208da0ba6fd2261c544b';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2532804fa557187bb2b7a57d134b818b5cc9054cc3346d0b6ba93467e337fbdb';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='92323ebeb274e60f48f9301a8fe157382191927e50e97870cd9619461b527b5f';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='62e48b9b65d1266c017a890db6e5b3f24d28e543e04d1cf1ce553b280f9bf2c6';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Sat, 30 Apr 2022 01:06:59 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Sat, 30 Apr 2022 05:33:48 GMT
ARG VERBOSE=false
# Sat, 30 Apr 2022 05:33:48 GMT
ARG OPENJ9_SCC=true
# Wed, 18 May 2022 01:11:18 GMT
ARG EN_SHA=2c85b0e69fa3b281919e9db592846585762fc82a6cad058d53fa484013aaf4b8
# Wed, 18 May 2022 01:11:18 GMT
ARG NON_IBM_SHA=6e08202f7be09eb4e05a2e754285812724e169318596248763ff833e85a27b47
# Wed, 18 May 2022 01:11:18 GMT
ARG NOTICES_SHA=afc4329090afc2b5913c49afb9866137497bce169a2ca71e36c7e74ed6945759
# Wed, 18 May 2022 01:11:18 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=22.0.0.5 org.opencontainers.image.revision=cl220520220425-0301 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 18 May 2022 01:11:18 GMT
ENV LIBERTY_VERSION=22.0.0_05
# Wed, 18 May 2022 01:11:18 GMT
ARG LIBERTY_URL
# Wed, 18 May 2022 01:11:18 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 18 May 2022 01:11:33 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2c85b0e69fa3b281919e9db592846585762fc82a6cad058d53fa484013aaf4b8 NON_IBM_SHA=6e08202f7be09eb4e05a2e754285812724e169318596248763ff833e85a27b47 NOTICES_SHA=afc4329090afc2b5913c49afb9866137497bce169a2ca71e36c7e74ed6945759 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 18 May 2022 01:11:33 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 May 2022 01:11:34 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=22.0.0.5 BuildLabel=cl220520220425-0301
# Wed, 18 May 2022 01:11:34 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 18 May 2022 01:11:35 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2c85b0e69fa3b281919e9db592846585762fc82a6cad058d53fa484013aaf4b8 NON_IBM_SHA=6e08202f7be09eb4e05a2e754285812724e169318596248763ff833e85a27b47 NOTICES_SHA=afc4329090afc2b5913c49afb9866137497bce169a2ca71e36c7e74ed6945759 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 18 May 2022 01:11:35 GMT
COPY dir:b44499731da0f244ad2e27b60beff4f4cda216316903b60ecb41a7fba3784b48 in /opt/ibm/helpers/ 
# Wed, 18 May 2022 01:11:35 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 18 May 2022 01:11:36 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2c85b0e69fa3b281919e9db592846585762fc82a6cad058d53fa484013aaf4b8 NON_IBM_SHA=6e08202f7be09eb4e05a2e754285812724e169318596248763ff833e85a27b47 NOTICES_SHA=afc4329090afc2b5913c49afb9866137497bce169a2ca71e36c7e74ed6945759 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 18 May 2022 01:11:45 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2c85b0e69fa3b281919e9db592846585762fc82a6cad058d53fa484013aaf4b8 NON_IBM_SHA=6e08202f7be09eb4e05a2e754285812724e169318596248763ff833e85a27b47 NOTICES_SHA=afc4329090afc2b5913c49afb9866137497bce169a2ca71e36c7e74ed6945759 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 18 May 2022 01:11:45 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 18 May 2022 01:11:45 GMT
USER 1001
# Wed, 18 May 2022 01:11:45 GMT
EXPOSE 9080 9443
# Wed, 18 May 2022 01:11:45 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 18 May 2022 01:11:45 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:40dd5be53814ae70b2898558673b7ea18d58bf7ab3433560b9ce3cb76d9ff0b1`  
		Last Modified: Fri, 29 Apr 2022 23:22:07 GMT  
		Size: 26.7 MB (26709108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9274cc4ee93edf7c6c542860e9243251f72535f23aa9365dc6f25072d40216`  
		Last Modified: Sat, 30 Apr 2022 01:08:49 GMT  
		Size: 3.0 MB (2959981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f2e31e24dc6a646e66288b5787aba0b0ff58a51a88b9eb0173fe5285690727`  
		Last Modified: Sat, 30 Apr 2022 01:08:58 GMT  
		Size: 129.0 MB (129010262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f8ebe630c95f4f6bd318b3a425bcd91527bd4e3bc6c27871fd7827ef41be28`  
		Last Modified: Wed, 18 May 2022 01:36:21 GMT  
		Size: 14.5 MB (14494270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8939698b73d01ee522f9982536d5dca42e25acdb46737ad985e19d20ac07d813`  
		Last Modified: Wed, 18 May 2022 01:36:17 GMT  
		Size: 697.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2168229f0a6715d3112403c8e2c6b0f742ba337e5db61df51e4a3578e814e9db`  
		Last Modified: Wed, 18 May 2022 01:36:17 GMT  
		Size: 9.7 KB (9681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e2277dea2805c6ec1ef67f76ced41007ab06f21525c0b2d99e3727fddbf5e4`  
		Last Modified: Wed, 18 May 2022 01:36:18 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5731bdf00f6956a7b375374b87943d0158af4d998221a724f4d6c7aade379b09`  
		Last Modified: Wed, 18 May 2022 01:36:17 GMT  
		Size: 10.7 KB (10666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa66e74fe52b89d04d5383806c964ff099df28390c5083e71325ffa0ef8e0d4f`  
		Last Modified: Wed, 18 May 2022 01:36:18 GMT  
		Size: 5.8 MB (5756081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:b4a8f34ab65f1563fd62f15c7040adeabdd2ccbe2a66c2f3627a9bb53238f9fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.9 MB (181913033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17cf0f4c0987b19d99e48df477c7c449e13925537a25fb93d55bcb85e0253a6d`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 29 Apr 2022 23:22:00 GMT
ADD file:2d91cfcbab5facf9c027064efd477cfde81eca0c1a62c6611ac694bafb94d817 in / 
# Fri, 29 Apr 2022 23:22:04 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 01:49:39 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Sat, 30 Apr 2022 01:50:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 01:50:12 GMT
ENV JAVA_VERSION=8.0.7.6
# Sat, 30 Apr 2022 01:51:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='04b9e508ec9d206296b4972f1e122a168fc5f2524f7606ec3ade6600cef193a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='d0fa8483f91717a478d3ae8cca82c8934966a7603287208da0ba6fd2261c544b';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2532804fa557187bb2b7a57d134b818b5cc9054cc3346d0b6ba93467e337fbdb';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='92323ebeb274e60f48f9301a8fe157382191927e50e97870cd9619461b527b5f';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='62e48b9b65d1266c017a890db6e5b3f24d28e543e04d1cf1ce553b280f9bf2c6';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Sat, 30 Apr 2022 01:51:17 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Sat, 30 Apr 2022 05:17:10 GMT
ARG VERBOSE=false
# Sat, 30 Apr 2022 05:17:14 GMT
ARG OPENJ9_SCC=true
# Wed, 18 May 2022 02:51:56 GMT
ARG EN_SHA=2c85b0e69fa3b281919e9db592846585762fc82a6cad058d53fa484013aaf4b8
# Wed, 18 May 2022 02:52:02 GMT
ARG NON_IBM_SHA=6e08202f7be09eb4e05a2e754285812724e169318596248763ff833e85a27b47
# Wed, 18 May 2022 02:52:05 GMT
ARG NOTICES_SHA=afc4329090afc2b5913c49afb9866137497bce169a2ca71e36c7e74ed6945759
# Wed, 18 May 2022 02:52:09 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=22.0.0.5 org.opencontainers.image.revision=cl220520220425-0301 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 18 May 2022 02:52:13 GMT
ENV LIBERTY_VERSION=22.0.0_05
# Wed, 18 May 2022 02:52:17 GMT
ARG LIBERTY_URL
# Wed, 18 May 2022 02:52:19 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 18 May 2022 02:53:01 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2c85b0e69fa3b281919e9db592846585762fc82a6cad058d53fa484013aaf4b8 NON_IBM_SHA=6e08202f7be09eb4e05a2e754285812724e169318596248763ff833e85a27b47 NOTICES_SHA=afc4329090afc2b5913c49afb9866137497bce169a2ca71e36c7e74ed6945759 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 18 May 2022 02:53:04 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 May 2022 02:53:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=22.0.0.5 BuildLabel=cl220520220425-0301
# Wed, 18 May 2022 02:53:08 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 18 May 2022 02:53:24 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2c85b0e69fa3b281919e9db592846585762fc82a6cad058d53fa484013aaf4b8 NON_IBM_SHA=6e08202f7be09eb4e05a2e754285812724e169318596248763ff833e85a27b47 NOTICES_SHA=afc4329090afc2b5913c49afb9866137497bce169a2ca71e36c7e74ed6945759 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 18 May 2022 02:53:27 GMT
COPY dir:b44499731da0f244ad2e27b60beff4f4cda216316903b60ecb41a7fba3784b48 in /opt/ibm/helpers/ 
# Wed, 18 May 2022 02:53:27 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 18 May 2022 02:53:34 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2c85b0e69fa3b281919e9db592846585762fc82a6cad058d53fa484013aaf4b8 NON_IBM_SHA=6e08202f7be09eb4e05a2e754285812724e169318596248763ff833e85a27b47 NOTICES_SHA=afc4329090afc2b5913c49afb9866137497bce169a2ca71e36c7e74ed6945759 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 18 May 2022 02:53:53 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2c85b0e69fa3b281919e9db592846585762fc82a6cad058d53fa484013aaf4b8 NON_IBM_SHA=6e08202f7be09eb4e05a2e754285812724e169318596248763ff833e85a27b47 NOTICES_SHA=afc4329090afc2b5913c49afb9866137497bce169a2ca71e36c7e74ed6945759 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 18 May 2022 02:53:55 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 18 May 2022 02:53:57 GMT
USER 1001
# Wed, 18 May 2022 02:53:59 GMT
EXPOSE 9080 9443
# Wed, 18 May 2022 02:54:01 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 18 May 2022 02:54:04 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:c70b79613e1f9e69f0d6473fa0b3f8b10d376e24350617c381ed64978f4bae97`  
		Last Modified: Fri, 29 Apr 2022 23:24:58 GMT  
		Size: 30.4 MB (30443183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b9fc7dc4c2bad9d9f7db0ffd5b499212f90be1d458552dba4bd7e526ede046`  
		Last Modified: Sat, 30 Apr 2022 01:54:24 GMT  
		Size: 3.1 MB (3082255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824dce7232c365d3b1e5b341c057a63216c8b9e75a0fd0729b73ae58d2655cc8`  
		Last Modified: Sat, 30 Apr 2022 01:54:38 GMT  
		Size: 128.5 MB (128516348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1a1ae48e7b1e574602de7833e6cdff49f552eb0d4088057eddeb879ce7e591`  
		Last Modified: Wed, 18 May 2022 03:33:16 GMT  
		Size: 14.5 MB (14514771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c770073f8a6c0c60fe612879c8e224029687e7776ec083c4f1728e8a33132d`  
		Last Modified: Wed, 18 May 2022 03:33:12 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb11ef72f7e413434fff4f46ccc8246c37dd89a03907d677df8d5b992cd9495`  
		Last Modified: Wed, 18 May 2022 03:33:12 GMT  
		Size: 9.7 KB (9683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c605d8cf37c6319f0a02624dc1d99f09874b8178f28838c84d41fa89ed8112ff`  
		Last Modified: Wed, 18 May 2022 03:33:12 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814ee8a7aac2125bb8fec675778e2f3c4389ee235aeaf7758691d35f251c6943`  
		Last Modified: Wed, 18 May 2022 03:33:12 GMT  
		Size: 10.7 KB (10664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14318c794087ca97b766f8d969678d5329bf94de737667cf867ef7d70ff16dc`  
		Last Modified: Wed, 18 May 2022 03:33:13 GMT  
		Size: 5.3 MB (5335155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:c5066a0eea5271e6cdd110adf61b7312b7b1f88cb88e948781e04f57556a5f7f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174517616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2c01f99ae29b27d2a8626ea9ef8568aa6c1d383f4f3fa66ca7d4a9787caa67`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:50 GMT
ADD file:9b5ddd45fc485b5c5ea3d28339d1768fa5d8f60059022a971897d51d94ad5847 in / 
# Fri, 29 Apr 2022 22:49:54 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:27:15 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 29 Apr 2022 23:27:21 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Jun 2022 15:41:55 GMT
ENV JAVA_VERSION=8.0.7.10
# Wed, 01 Jun 2022 15:42:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='5d779014943fa5957ad5dbf2230e99d6a4e1cdc4e8d906414700309a53716a4f';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='607414268c0e2994f21b9c031a81e515286b4689ce283f03a12cc1a5f956fdd3';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='9f1f5b5ae2cf7ecfef9b3a8871e721724cb8edd50b671c557881d5479ecdf5cf';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1a9d7b060670ee27f8be95e8b781f5c85b4228ae4fe1b33f1daddb5d2e56c926';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='c609d711ba6ba2857faa285bb6df225df31d22a387f0857dc08976d0f65e7ba7';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 01 Jun 2022 15:43:05 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 01 Jun 2022 16:02:39 GMT
ARG VERBOSE=false
# Wed, 01 Jun 2022 16:02:39 GMT
ARG OPENJ9_SCC=true
# Wed, 01 Jun 2022 16:02:40 GMT
ARG EN_SHA=2c85b0e69fa3b281919e9db592846585762fc82a6cad058d53fa484013aaf4b8
# Wed, 01 Jun 2022 16:02:40 GMT
ARG NON_IBM_SHA=6e08202f7be09eb4e05a2e754285812724e169318596248763ff833e85a27b47
# Wed, 01 Jun 2022 16:02:40 GMT
ARG NOTICES_SHA=afc4329090afc2b5913c49afb9866137497bce169a2ca71e36c7e74ed6945759
# Wed, 01 Jun 2022 16:02:40 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=22.0.0.5 org.opencontainers.image.revision=cl220520220425-0301 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 01 Jun 2022 16:02:40 GMT
ENV LIBERTY_VERSION=22.0.0_05
# Wed, 01 Jun 2022 16:02:40 GMT
ARG LIBERTY_URL
# Wed, 01 Jun 2022 16:02:41 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 01 Jun 2022 16:02:55 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2c85b0e69fa3b281919e9db592846585762fc82a6cad058d53fa484013aaf4b8 NON_IBM_SHA=6e08202f7be09eb4e05a2e754285812724e169318596248763ff833e85a27b47 NOTICES_SHA=afc4329090afc2b5913c49afb9866137497bce169a2ca71e36c7e74ed6945759 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Jun 2022 16:02:55 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Jun 2022 16:02:56 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=22.0.0.5 BuildLabel=cl220520220425-0301
# Wed, 01 Jun 2022 16:02:56 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 01 Jun 2022 16:02:57 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2c85b0e69fa3b281919e9db592846585762fc82a6cad058d53fa484013aaf4b8 NON_IBM_SHA=6e08202f7be09eb4e05a2e754285812724e169318596248763ff833e85a27b47 NOTICES_SHA=afc4329090afc2b5913c49afb9866137497bce169a2ca71e36c7e74ed6945759 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 01 Jun 2022 16:02:57 GMT
COPY dir:b44499731da0f244ad2e27b60beff4f4cda216316903b60ecb41a7fba3784b48 in /opt/ibm/helpers/ 
# Wed, 01 Jun 2022 16:02:57 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 01 Jun 2022 16:02:58 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2c85b0e69fa3b281919e9db592846585762fc82a6cad058d53fa484013aaf4b8 NON_IBM_SHA=6e08202f7be09eb4e05a2e754285812724e169318596248763ff833e85a27b47 NOTICES_SHA=afc4329090afc2b5913c49afb9866137497bce169a2ca71e36c7e74ed6945759 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 01 Jun 2022 16:03:07 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=2c85b0e69fa3b281919e9db592846585762fc82a6cad058d53fa484013aaf4b8 NON_IBM_SHA=6e08202f7be09eb4e05a2e754285812724e169318596248763ff833e85a27b47 NOTICES_SHA=afc4329090afc2b5913c49afb9866137497bce169a2ca71e36c7e74ed6945759 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 01 Jun 2022 16:03:08 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 01 Jun 2022 16:03:08 GMT
USER 1001
# Wed, 01 Jun 2022 16:03:08 GMT
EXPOSE 9080 9443
# Wed, 01 Jun 2022 16:03:08 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 01 Jun 2022 16:03:08 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:1347a7b069ceb0e131b6f229b7b96bae189f8e4c594c1933170e278d0ed928b2`  
		Last Modified: Fri, 29 Apr 2022 22:51:49 GMT  
		Size: 25.4 MB (25365828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f94c1c13b8b89cf54909fe9580987f60938a39e09f8c39697300c3a17a3ec1`  
		Last Modified: Fri, 29 Apr 2022 23:30:09 GMT  
		Size: 2.7 MB (2677016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3a8e27eadcc5a6367050ff4089b3a282bdd954a86e38bb735c31a7567ad66a`  
		Last Modified: Wed, 01 Jun 2022 15:46:20 GMT  
		Size: 126.1 MB (126076388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71495882c19b0264d13ff6f2dc952db4d0a05bd5b533caf1f018ee1cb0dd56c`  
		Last Modified: Wed, 01 Jun 2022 16:42:59 GMT  
		Size: 14.5 MB (14499465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5d86a2dd10c613f3502546e9bf02ad6867c3dec626ae43850f8e23237de975`  
		Last Modified: Wed, 01 Jun 2022 16:42:56 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71bfb1e3667be884d5f81689618b7c991d30994b77285a56554ff4c3440a816`  
		Last Modified: Wed, 01 Jun 2022 16:42:56 GMT  
		Size: 9.7 KB (9676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0fea3049b1dfa2974dd7502473598fc826fa40c8ce75f3af0ac2ee8fe18ac90`  
		Last Modified: Wed, 01 Jun 2022 16:42:56 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3efd1019eda1482e45773ad5045cf04de3ff4173098082aaa9d82084e2a167bc`  
		Last Modified: Wed, 01 Jun 2022 16:42:56 GMT  
		Size: 10.7 KB (10656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b016538b63c7c4435168c8b94e8b1631d2cf73ed4175da535690b5906deb8cec`  
		Last Modified: Wed, 01 Jun 2022 16:42:57 GMT  
		Size: 5.9 MB (5877619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
