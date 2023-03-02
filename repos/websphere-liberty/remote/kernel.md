## `websphere-liberty:kernel`

```console
$ docker pull websphere-liberty@sha256:389dcf3df0dce3f303ccd6d8ffd4b8124a0084380058d78869ec577bc3a447dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:kernel` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:205201c7dccc60770d916159faf3acaee4d0473868a385e93bd2b6bfdd00e828
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.2 MB (179192447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52fc02b58f547a90056db7fabf6deb162de26718f0f834d7ab6c564e364968c8`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 01 Mar 2023 03:18:00 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:18:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:18:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:18:00 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:18:02 GMT
ADD file:66eb2ef5574cdf80bc0cb3af1637407620c1869f58cc7514395e3f5aea45cc3b in / 
# Wed, 01 Mar 2023 03:18:02 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:33:47 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 02 Mar 2023 04:33:55 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:33:55 GMT
ENV JAVA_VERSION=8.0.7.20
# Thu, 02 Mar 2023 04:34:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 02 Mar 2023 04:34:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Thu, 02 Mar 2023 12:30:16 GMT
ARG VERBOSE=false
# Thu, 02 Mar 2023 12:30:16 GMT
ARG OPENJ9_SCC=true
# Thu, 02 Mar 2023 12:30:16 GMT
ARG EN_SHA=dd3e1f52b274ac7551192d7ff07a2858396132ece9a26e8d3e8e28830e84183e
# Thu, 02 Mar 2023 12:30:16 GMT
ARG NON_IBM_SHA=0a41a7fa840ccd132d68f0fc6138f573fe110dafaa36f2bcdeab9f2b495876a5
# Thu, 02 Mar 2023 12:30:16 GMT
ARG NOTICES_SHA=d4e03fe4b7d7492aba18a7ed449c0a5666258e4318c1a929042f53ed87abafa1
# Thu, 02 Mar 2023 12:30:16 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=23.0.0.1 org.opencontainers.image.revision=cl230120230123-2118 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 02 Mar 2023 12:30:16 GMT
ENV LIBERTY_VERSION=23.0.0_1
# Thu, 02 Mar 2023 12:30:17 GMT
ARG LIBERTY_URL
# Thu, 02 Mar 2023 12:30:17 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 02 Mar 2023 12:30:38 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=dd3e1f52b274ac7551192d7ff07a2858396132ece9a26e8d3e8e28830e84183e NON_IBM_SHA=0a41a7fa840ccd132d68f0fc6138f573fe110dafaa36f2bcdeab9f2b495876a5 NOTICES_SHA=d4e03fe4b7d7492aba18a7ed449c0a5666258e4318c1a929042f53ed87abafa1 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 12:30:38 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Thu, 02 Mar 2023 12:30:38 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=23.0.0.1 BuildLabel=cl230120230123-2118
# Thu, 02 Mar 2023 12:30:38 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 02 Mar 2023 12:30:40 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=dd3e1f52b274ac7551192d7ff07a2858396132ece9a26e8d3e8e28830e84183e NON_IBM_SHA=0a41a7fa840ccd132d68f0fc6138f573fe110dafaa36f2bcdeab9f2b495876a5 NOTICES_SHA=d4e03fe4b7d7492aba18a7ed449c0a5666258e4318c1a929042f53ed87abafa1 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 02 Mar 2023 12:30:40 GMT
COPY dir:8bf844c49178cf63745af9ec643f57d70bd92c28166fabfad188dfc250d88353 in /opt/ibm/helpers/ 
# Thu, 02 Mar 2023 12:30:40 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 02 Mar 2023 12:30:41 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=dd3e1f52b274ac7551192d7ff07a2858396132ece9a26e8d3e8e28830e84183e NON_IBM_SHA=0a41a7fa840ccd132d68f0fc6138f573fe110dafaa36f2bcdeab9f2b495876a5 NOTICES_SHA=d4e03fe4b7d7492aba18a7ed449c0a5666258e4318c1a929042f53ed87abafa1 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 02 Mar 2023 12:30:48 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=dd3e1f52b274ac7551192d7ff07a2858396132ece9a26e8d3e8e28830e84183e NON_IBM_SHA=0a41a7fa840ccd132d68f0fc6138f573fe110dafaa36f2bcdeab9f2b495876a5 NOTICES_SHA=d4e03fe4b7d7492aba18a7ed449c0a5666258e4318c1a929042f53ed87abafa1 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 02 Mar 2023 12:30:48 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Thu, 02 Mar 2023 12:30:48 GMT
USER 1001
# Thu, 02 Mar 2023 12:30:48 GMT
EXPOSE 9080 9443
# Thu, 02 Mar 2023 12:30:49 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 02 Mar 2023 12:30:49 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:0064b1b97ec0775813740e8cb92821a6d84fd38eee70bafba9c12d9c37534661`  
		Last Modified: Wed, 01 Mar 2023 13:18:18 GMT  
		Size: 26.7 MB (26711153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4584491976e0a2288553243d3caf1fc9a32b4827c131397e78d378040794a302`  
		Last Modified: Thu, 02 Mar 2023 04:37:19 GMT  
		Size: 3.0 MB (2952434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238eab0aea5a72c0181d2465938a0dd5d6bab89c961d28625b89db693305b8ec`  
		Last Modified: Thu, 02 Mar 2023 04:37:27 GMT  
		Size: 129.3 MB (129322614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724b10ec88314370b7c4521c8ff7bcc66b4107b1959b6fa2eb1a36d66d598803`  
		Last Modified: Thu, 02 Mar 2023 14:02:09 GMT  
		Size: 14.3 MB (14342518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af285a2e8fc7d6e350f2a8149c29b095f347c1dbd574ea2e6479de28e798f2e8`  
		Last Modified: Thu, 02 Mar 2023 14:02:06 GMT  
		Size: 685.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bfa5a16abb508cc2cb2ec242d51ea2fe39b9abfb6be819d3c6d39db73484962`  
		Last Modified: Thu, 02 Mar 2023 14:02:06 GMT  
		Size: 9.8 KB (9755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e974cc7107d563731c09f96ba142f534ee717f018a510aa6525ac8c8a92e139`  
		Last Modified: Thu, 02 Mar 2023 14:02:05 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df65b223f580a3acc86f4a3922494cebb5b32d35a7438c7e9bc1469f856fe52e`  
		Last Modified: Thu, 02 Mar 2023 14:02:06 GMT  
		Size: 10.7 KB (10737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaadf5a58873cee0144d5d1d68c4d02da49105f152cbe512ac01b1014b8083fc`  
		Last Modified: Thu, 02 Mar 2023 14:02:07 GMT  
		Size: 5.8 MB (5842278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:d107006e75f41b12ce4aa20ddf28d4bbe81ed74bbed7c22991900e01b475cfe6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.4 MB (182394746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3950677abb5bc4c8dc7f601c749a906d27807759fed272cd0c7180620cd5d33`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 01 Mar 2023 03:15:24 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:15:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:15:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:15:24 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:15:27 GMT
ADD file:ca5a453351fddb6d7937e334f0331321829a5bebca3d726ef3dddad1f23b35c8 in / 
# Wed, 01 Mar 2023 03:15:27 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:26:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 02 Mar 2023 04:26:46 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:26:47 GMT
ENV JAVA_VERSION=8.0.7.20
# Thu, 02 Mar 2023 04:29:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 02 Mar 2023 04:29:07 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Thu, 02 Mar 2023 08:11:26 GMT
ARG VERBOSE=false
# Thu, 02 Mar 2023 08:11:27 GMT
ARG OPENJ9_SCC=true
# Thu, 02 Mar 2023 08:11:28 GMT
ARG EN_SHA=dd3e1f52b274ac7551192d7ff07a2858396132ece9a26e8d3e8e28830e84183e
# Thu, 02 Mar 2023 08:11:29 GMT
ARG NON_IBM_SHA=0a41a7fa840ccd132d68f0fc6138f573fe110dafaa36f2bcdeab9f2b495876a5
# Thu, 02 Mar 2023 08:11:30 GMT
ARG NOTICES_SHA=d4e03fe4b7d7492aba18a7ed449c0a5666258e4318c1a929042f53ed87abafa1
# Thu, 02 Mar 2023 08:11:32 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=23.0.0.1 org.opencontainers.image.revision=cl230120230123-2118 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 02 Mar 2023 08:11:32 GMT
ENV LIBERTY_VERSION=23.0.0_1
# Thu, 02 Mar 2023 08:11:36 GMT
ARG LIBERTY_URL
# Thu, 02 Mar 2023 08:11:39 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 02 Mar 2023 08:12:29 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=dd3e1f52b274ac7551192d7ff07a2858396132ece9a26e8d3e8e28830e84183e NON_IBM_SHA=0a41a7fa840ccd132d68f0fc6138f573fe110dafaa36f2bcdeab9f2b495876a5 NOTICES_SHA=d4e03fe4b7d7492aba18a7ed449c0a5666258e4318c1a929042f53ed87abafa1 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 08:12:30 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Thu, 02 Mar 2023 08:12:32 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=23.0.0.1 BuildLabel=cl230120230123-2118
# Thu, 02 Mar 2023 08:12:33 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 02 Mar 2023 08:12:36 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=dd3e1f52b274ac7551192d7ff07a2858396132ece9a26e8d3e8e28830e84183e NON_IBM_SHA=0a41a7fa840ccd132d68f0fc6138f573fe110dafaa36f2bcdeab9f2b495876a5 NOTICES_SHA=d4e03fe4b7d7492aba18a7ed449c0a5666258e4318c1a929042f53ed87abafa1 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 02 Mar 2023 08:12:36 GMT
COPY dir:8bf844c49178cf63745af9ec643f57d70bd92c28166fabfad188dfc250d88353 in /opt/ibm/helpers/ 
# Thu, 02 Mar 2023 08:12:36 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 02 Mar 2023 08:12:39 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=dd3e1f52b274ac7551192d7ff07a2858396132ece9a26e8d3e8e28830e84183e NON_IBM_SHA=0a41a7fa840ccd132d68f0fc6138f573fe110dafaa36f2bcdeab9f2b495876a5 NOTICES_SHA=d4e03fe4b7d7492aba18a7ed449c0a5666258e4318c1a929042f53ed87abafa1 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 02 Mar 2023 08:12:52 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=dd3e1f52b274ac7551192d7ff07a2858396132ece9a26e8d3e8e28830e84183e NON_IBM_SHA=0a41a7fa840ccd132d68f0fc6138f573fe110dafaa36f2bcdeab9f2b495876a5 NOTICES_SHA=d4e03fe4b7d7492aba18a7ed449c0a5666258e4318c1a929042f53ed87abafa1 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 02 Mar 2023 08:12:53 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Thu, 02 Mar 2023 08:12:53 GMT
USER 1001
# Thu, 02 Mar 2023 08:12:55 GMT
EXPOSE 9080 9443
# Thu, 02 Mar 2023 08:12:55 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 02 Mar 2023 08:12:56 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:27fbc2bd86045e72ba8d9901b237295e3094b37f456824337175e24a0f0afe98`  
		Last Modified: Thu, 02 Mar 2023 03:09:44 GMT  
		Size: 30.4 MB (30442026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ba0371be9483ee0b28a477686cea779ddaceb8d8bac7c4e6fe24bf77052c7e`  
		Last Modified: Thu, 02 Mar 2023 04:34:32 GMT  
		Size: 3.1 MB (3077279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66fd4a431fe0afda0b63e76bfe7d54d7b07f959c8f5301822db4d57252cf1a04`  
		Last Modified: Thu, 02 Mar 2023 04:34:48 GMT  
		Size: 129.0 MB (128996346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9284cefefd99d243cc080546d25cc6c18ce9064265ffb17c4b4d9c784c0e44a9`  
		Last Modified: Thu, 02 Mar 2023 11:07:25 GMT  
		Size: 14.3 MB (14343000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1bc7a656e38c24e176d1cfaba00276aa7fc958995c51886fa2617e72822aa7`  
		Last Modified: Thu, 02 Mar 2023 11:07:21 GMT  
		Size: 680.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc79de6bee04f13f0ba85e2aff788c1d016ec9b80e08cd56597adb3e6e1e65d`  
		Last Modified: Thu, 02 Mar 2023 11:07:21 GMT  
		Size: 9.7 KB (9749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1eb7d58c486894a8159b3dbe29d7c5283b7967f01654fd88958055f38a3dda1`  
		Last Modified: Thu, 02 Mar 2023 11:07:21 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f114fdad6d60801e3acd1715d64ee3348fb8ca1ecf599b34689a052503d8044`  
		Last Modified: Thu, 02 Mar 2023 11:07:21 GMT  
		Size: 10.7 KB (10738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76897a21b0cc524a7fc3400b0844589de716f4e6ff31c268e139ba83f2e1ca33`  
		Last Modified: Thu, 02 Mar 2023 11:07:22 GMT  
		Size: 5.5 MB (5514655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:d510a6a06f68744719c86d589884206f2474d709763af9085a197bae5e059bb3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.2 MB (175160022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cbf01816b5588f59780fd8274cd1491811c2c3248d6aa14bea2b972b3239cb7`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 26 Jan 2023 09:55:41 GMT
ARG RELEASE
# Thu, 26 Jan 2023 09:55:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 09:55:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 09:55:41 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 09:55:43 GMT
ADD file:04d4137c9183cee18560fc26a092e288ff403f3dde266237eab245bd38eb9b3a in / 
# Thu, 26 Jan 2023 09:55:43 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:38:24 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 31 Jan 2023 18:38:31 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:38:31 GMT
ENV JAVA_VERSION=8.0.7.20
# Tue, 31 Jan 2023 18:39:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 31 Jan 2023 18:39:22 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 31 Jan 2023 20:37:16 GMT
ARG VERBOSE=false
# Tue, 31 Jan 2023 20:37:16 GMT
ARG OPENJ9_SCC=true
# Fri, 10 Feb 2023 02:11:00 GMT
ARG EN_SHA=dd3e1f52b274ac7551192d7ff07a2858396132ece9a26e8d3e8e28830e84183e
# Fri, 10 Feb 2023 02:11:00 GMT
ARG NON_IBM_SHA=0a41a7fa840ccd132d68f0fc6138f573fe110dafaa36f2bcdeab9f2b495876a5
# Fri, 10 Feb 2023 02:11:00 GMT
ARG NOTICES_SHA=d4e03fe4b7d7492aba18a7ed449c0a5666258e4318c1a929042f53ed87abafa1
# Fri, 10 Feb 2023 02:11:00 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=23.0.0.1 org.opencontainers.image.revision=cl230120230123-2118 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 10 Feb 2023 02:11:00 GMT
ENV LIBERTY_VERSION=23.0.0_1
# Fri, 10 Feb 2023 02:11:01 GMT
ARG LIBERTY_URL
# Fri, 10 Feb 2023 02:11:01 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 10 Feb 2023 02:11:19 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=dd3e1f52b274ac7551192d7ff07a2858396132ece9a26e8d3e8e28830e84183e NON_IBM_SHA=0a41a7fa840ccd132d68f0fc6138f573fe110dafaa36f2bcdeab9f2b495876a5 NOTICES_SHA=d4e03fe4b7d7492aba18a7ed449c0a5666258e4318c1a929042f53ed87abafa1 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 10 Feb 2023 02:11:20 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Fri, 10 Feb 2023 02:11:20 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=23.0.0.1 BuildLabel=cl230120230123-2118
# Fri, 10 Feb 2023 02:11:20 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 10 Feb 2023 02:11:22 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=dd3e1f52b274ac7551192d7ff07a2858396132ece9a26e8d3e8e28830e84183e NON_IBM_SHA=0a41a7fa840ccd132d68f0fc6138f573fe110dafaa36f2bcdeab9f2b495876a5 NOTICES_SHA=d4e03fe4b7d7492aba18a7ed449c0a5666258e4318c1a929042f53ed87abafa1 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 10 Feb 2023 02:11:22 GMT
COPY dir:8bf844c49178cf63745af9ec643f57d70bd92c28166fabfad188dfc250d88353 in /opt/ibm/helpers/ 
# Fri, 10 Feb 2023 02:11:22 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 10 Feb 2023 02:11:23 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=dd3e1f52b274ac7551192d7ff07a2858396132ece9a26e8d3e8e28830e84183e NON_IBM_SHA=0a41a7fa840ccd132d68f0fc6138f573fe110dafaa36f2bcdeab9f2b495876a5 NOTICES_SHA=d4e03fe4b7d7492aba18a7ed449c0a5666258e4318c1a929042f53ed87abafa1 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 10 Feb 2023 02:11:29 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=dd3e1f52b274ac7551192d7ff07a2858396132ece9a26e8d3e8e28830e84183e NON_IBM_SHA=0a41a7fa840ccd132d68f0fc6138f573fe110dafaa36f2bcdeab9f2b495876a5 NOTICES_SHA=d4e03fe4b7d7492aba18a7ed449c0a5666258e4318c1a929042f53ed87abafa1 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 10 Feb 2023 02:11:29 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 10 Feb 2023 02:11:29 GMT
USER 1001
# Fri, 10 Feb 2023 02:11:29 GMT
EXPOSE 9080 9443
# Fri, 10 Feb 2023 02:11:30 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 10 Feb 2023 02:11:30 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:4727db5881c26ec0d79df6d172cfc50624c09ca7869b8146052e0692734d2cac`  
		Last Modified: Tue, 31 Jan 2023 17:53:57 GMT  
		Size: 25.4 MB (25371457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b35b388f9f9b6d25e2f70fc595153cc50356a94e5866b3b8b3d7e2e7632e68`  
		Last Modified: Tue, 31 Jan 2023 18:41:41 GMT  
		Size: 2.7 MB (2667334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e351d12a594cc2263e72741a7da47fa2910deb84f8d146117a7853347fcb46cb`  
		Last Modified: Tue, 31 Jan 2023 18:41:49 GMT  
		Size: 126.5 MB (126472616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2341959db57ca420e729df64c0ccf001c6e8a9300497c8c68fcf77af5697798e`  
		Last Modified: Fri, 10 Feb 2023 03:37:27 GMT  
		Size: 14.7 MB (14653384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd9d40ac4dd73c7a99169ae38cbcbd72f6eb07386a467dc69255978db3662ca`  
		Last Modified: Fri, 10 Feb 2023 03:37:25 GMT  
		Size: 681.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd09e20b358aa8611089a82a72a7fcb0f5900cacf67ffefab27bf5609d239608`  
		Last Modified: Fri, 10 Feb 2023 03:37:25 GMT  
		Size: 9.8 KB (9756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75644860cf8f3ad7a52ce51e8139f5dd9db63f4d35cfac6c671e027002dee42f`  
		Last Modified: Fri, 10 Feb 2023 03:37:25 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beda129720f6baa9e2a5fbd8e7d3027476ff390073f52fb06ed94d9dea2639c6`  
		Last Modified: Fri, 10 Feb 2023 03:37:25 GMT  
		Size: 10.7 KB (10733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c10c91c7af22de0eae440166acad65af46cfc89af8c06d7ffbe307a386b660`  
		Last Modified: Fri, 10 Feb 2023 03:37:26 GMT  
		Size: 6.0 MB (5973785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
