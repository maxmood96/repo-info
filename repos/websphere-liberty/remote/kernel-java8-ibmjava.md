## `websphere-liberty:kernel-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:d1fbd03b6c6033a361c80b2ffae03df0f325396c1d9cf8e8dabeda717b9b2752
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `websphere-liberty:kernel-java8-ibmjava` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:18d55e219d5e54bd61596c2c22bca6d536ab11ab1a81e040231eb090005115c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 MB (191246847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352f6b9a239bb563d715cdb45d07bfe43df0c5fc9976a2147100846e9e2b016b`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 19:04:32 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 22 Jan 2026 19:04:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Jan 2026 19:04:32 GMT
ENV JAVA_VERSION=8.0.8.60
# Thu, 22 Jan 2026 19:04:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0a965c513bb522004ddb195fbb3cda7124559b8c7c082fc8626b2f45b4ce9a94';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ebf5f90f77e524593cba310d9e73d993bc8d3357af0127ec4627b1ce8236f385';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8353fb367a56fd150bd5b1facb595bde690c9f9a1f3db7db3b7fb240399a6ae9';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 22 Jan 2026 19:04:41 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 27 Jan 2026 20:57:17 GMT
USER root
# Tue, 27 Jan 2026 20:57:17 GMT
ARG VERBOSE=false
# Tue, 27 Jan 2026 20:57:17 GMT
ARG OPENJ9_SCC=true
# Tue, 27 Jan 2026 20:57:17 GMT
ARG LIBERTY_VERSION=26.0.0.1
# Tue, 27 Jan 2026 20:57:17 GMT
ARG LIBERTY_BUILD_LABEL=cl260120260112-1902
# Tue, 27 Jan 2026 20:57:17 GMT
ARG LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8
# Tue, 27 Jan 2026 20:57:17 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.1 org.opencontainers.image.revision=cl260120260112-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.1 com.ibm.websphere.liberty.version=26.0.0.1
# Tue, 27 Jan 2026 20:57:17 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Tue, 27 Jan 2026 20:57:17 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.1 BuildLabel=cl260120260112-1902
# Tue, 27 Jan 2026 20:57:17 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 27 Jan 2026 20:57:17 GMT
ARG LIBERTY_URL
# Tue, 27 Jan 2026 20:57:17 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 27 Jan 2026 20:57:30 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 20:57:30 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 27 Jan 2026 20:57:30 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 27 Jan 2026 20:57:30 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 27 Jan 2026 20:57:30 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 27 Jan 2026 20:57:30 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 27 Jan 2026 20:57:30 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Tue, 27 Jan 2026 20:57:35 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 27 Jan 2026 20:57:35 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Tue, 27 Jan 2026 20:57:35 GMT
USER 1001
# Tue, 27 Jan 2026 20:57:35 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 27 Jan 2026 20:57:35 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 27 Jan 2026 20:57:35 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b3c52b2003009a78ec74c63cdfd50d1bd24ebaad519fdf90fb06116d245839`  
		Last Modified: Thu, 22 Jan 2026 19:04:55 GMT  
		Size: 1.5 MB (1450115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf35ae33af4a379d7530b0e245bb62918c9c2dddf88bb72055e73452273d762`  
		Last Modified: Thu, 22 Jan 2026 19:04:58 GMT  
		Size: 135.8 MB (135804366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1682e72b687218dfc505303c43797a3e17c2fffbb0ab219f3e4358a6ba23e965`  
		Last Modified: Tue, 27 Jan 2026 20:57:46 GMT  
		Size: 113.8 KB (113772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3db88ae34f41bdaab818667d4570b6666eec0619bac096bf2b7b994a3caf35`  
		Last Modified: Tue, 27 Jan 2026 20:57:47 GMT  
		Size: 18.4 MB (18441846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719f944ef1d2cd076ea4f72b193bcf1aba2f09da78a7cec994e1026a097375bb`  
		Last Modified: Tue, 27 Jan 2026 20:57:46 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696de7e20923511a2a70f9e4b90ef610b4da69679899d749ca9548c9ddb872d2`  
		Last Modified: Tue, 27 Jan 2026 20:57:46 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95a77d2b99daf365de8b41e263ad89f8b7b07e1ec02c17c86d79deac783ab39`  
		Last Modified: Tue, 27 Jan 2026 20:57:47 GMT  
		Size: 14.1 KB (14121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321419a0b5b0ea736dfd940168e2e10882f9f5835e04eca2eeefa4b183e476cd`  
		Last Modified: Tue, 27 Jan 2026 20:57:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e60c83b27b340cc2605051628cc6dd018e0851aa29928157f3ecf934674b11`  
		Last Modified: Tue, 27 Jan 2026 20:57:47 GMT  
		Size: 15.0 KB (14980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40071c3fb92f972ce7cb6c6de7f065fd56d05b06d6b9e2ee0531d0cd580e6bbb`  
		Last Modified: Tue, 27 Jan 2026 20:57:48 GMT  
		Size: 5.9 MB (5868629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:58ff097100acbfaa6fd856bfe5a04a535302df0e8ac4eae92c9ee3fe006546e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2345210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b1a423a0ba1067c78b9b89e31b2ce5087d2140d5691245148202769f9e44902`

```dockerfile
```

-	Layers:
	-	`sha256:bf904a0e2f2cb3c5e98d2f94f1bb4e099c1a53048258ecfd86347904d8f3784d`  
		Last Modified: Tue, 27 Jan 2026 20:57:46 GMT  
		Size: 2.3 MB (2306231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4cdd798d6d59e771840bceb509d11ef9d6dc376cbcca9d762da8551b3776b6a`  
		Last Modified: Tue, 27 Jan 2026 20:57:46 GMT  
		Size: 39.0 KB (38979 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:2a870ecd83a351496c7b6a7600292f0de178b5bb1cb74c1fa7edf8a69454fe96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 MB (196806299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20b3a28c953c3be1e299d4e161a3e00770c2abfdd80fafba8004453a9ac3e178`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:04 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:08 GMT
ADD file:db1efb6f83d2e5fbbebd44054afcb57c6ffff071d50a2434a5322064fe97af59 in / 
# Fri, 09 Jan 2026 07:03:08 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:48:26 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Jan 2026 22:48:26 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:48:26 GMT
ENV JAVA_VERSION=8.0.8.60
# Thu, 22 Jan 2026 19:27:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0a965c513bb522004ddb195fbb3cda7124559b8c7c082fc8626b2f45b4ce9a94';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ebf5f90f77e524593cba310d9e73d993bc8d3357af0127ec4627b1ce8236f385';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8353fb367a56fd150bd5b1facb595bde690c9f9a1f3db7db3b7fb240399a6ae9';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 22 Jan 2026 19:27:46 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 27 Jan 2026 21:04:51 GMT
USER root
# Tue, 27 Jan 2026 21:04:51 GMT
ARG VERBOSE=false
# Tue, 27 Jan 2026 21:04:51 GMT
ARG OPENJ9_SCC=true
# Tue, 27 Jan 2026 21:04:51 GMT
ARG LIBERTY_VERSION=26.0.0.1
# Tue, 27 Jan 2026 21:04:51 GMT
ARG LIBERTY_BUILD_LABEL=cl260120260112-1902
# Tue, 27 Jan 2026 21:04:51 GMT
ARG LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8
# Tue, 27 Jan 2026 21:04:51 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.1 org.opencontainers.image.revision=cl260120260112-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.1 com.ibm.websphere.liberty.version=26.0.0.1
# Tue, 27 Jan 2026 21:04:51 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Tue, 27 Jan 2026 21:04:51 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.1 BuildLabel=cl260120260112-1902
# Tue, 27 Jan 2026 21:04:51 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 27 Jan 2026 21:04:51 GMT
ARG LIBERTY_URL
# Tue, 27 Jan 2026 21:04:51 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 27 Jan 2026 21:05:24 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 21:05:24 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 27 Jan 2026 21:05:26 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 27 Jan 2026 21:05:26 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 27 Jan 2026 21:05:26 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 27 Jan 2026 21:05:27 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 27 Jan 2026 21:05:28 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Tue, 27 Jan 2026 21:05:38 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 27 Jan 2026 21:05:38 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Tue, 27 Jan 2026 21:05:38 GMT
USER 1001
# Tue, 27 Jan 2026 21:05:38 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 27 Jan 2026 21:05:38 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 27 Jan 2026 21:05:38 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:2490923be26ec970f7d805c10bc7c9c56e219061e875cf31dad74e227e0bbdc4`  
		Last Modified: Fri, 09 Jan 2026 07:36:16 GMT  
		Size: 34.4 MB (34446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814f9357ec073065f6203180cb4350e2f9485621f356fdf6fd2a944386ce11b4`  
		Last Modified: Thu, 15 Jan 2026 22:49:03 GMT  
		Size: 1.5 MB (1536144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93296e3c5abd8ee09936f707ba47540affc8d62c095e597030c281f68480448`  
		Last Modified: Thu, 22 Jan 2026 19:28:30 GMT  
		Size: 136.7 MB (136749858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89eec45161ad99d4a59b31c0dae638ae845a2faa5c702b09cd7a884bee3d3dfd`  
		Last Modified: Tue, 27 Jan 2026 21:06:01 GMT  
		Size: 118.0 KB (118021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0846600c00a3f0f3639324cb57ecf42cf94c034271db102102f61f27210c3ee3`  
		Last Modified: Tue, 27 Jan 2026 21:06:02 GMT  
		Size: 18.5 MB (18468088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ae5fbacf018ad41daab3ac844392dc7231d470f5152b80c7352df72e683ed6`  
		Last Modified: Tue, 27 Jan 2026 21:06:01 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6525b3f565b0fd6d3928a325080406f0b5733f1a7d8b7e29f2cf34902773bffd`  
		Last Modified: Tue, 27 Jan 2026 21:06:01 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041e1741eb7379e5c1a6c1cbbd110b93cc741b474e832a1036482134af2dc1d4`  
		Last Modified: Tue, 27 Jan 2026 21:06:03 GMT  
		Size: 14.1 KB (14122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffdb2b9f6aabfb0e0b0a8581c929bf584c7d1733273136d66c1883a0f4b56ac`  
		Last Modified: Tue, 27 Jan 2026 21:06:03 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710c5abc24fb8df8a3a85d8da0730a053b718bde7bfdb37cd7df343fd895c57a`  
		Last Modified: Tue, 27 Jan 2026 21:06:03 GMT  
		Size: 15.0 KB (15011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b2ad1be70b501b77b43786933d4c7ffd7e4b6f6f1e397f7b6eccf1ffc351e4`  
		Last Modified: Tue, 27 Jan 2026 21:06:04 GMT  
		Size: 5.5 MB (5455732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:74424dbbf8637c1d4f1f1c93f6f5373602776258c3c0887802196ad0263fef03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2348530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d593c71bab9469e0830d6317779b26eff02b49b1a55508cf9e91ee99295ea407`

```dockerfile
```

-	Layers:
	-	`sha256:24bed361a5c43cd761ad43c7e1c282a89b3264fe2cc252f39aaad86216cfffe8`  
		Last Modified: Tue, 27 Jan 2026 21:06:02 GMT  
		Size: 2.3 MB (2309506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b74a769e0dfb89ece6b0eb50826b6c86b4cd7108cc02a22dd5a6c4c717a414d`  
		Last Modified: Tue, 27 Jan 2026 21:06:01 GMT  
		Size: 39.0 KB (39024 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:8ffaf139b2e1c4436c66133c78da050da3dae73fd58b37bff1379c71d5b078a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.0 MB (187041841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011258346619e0f2509b86cadc2197e83d8df342147dc99d4dafe21ade125a4f`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 10 Feb 2026 17:41:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:41:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:41:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:41:31 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:41:33 GMT
ADD file:682bbddd1f3d784d0c4ab5eef9460f0b47a94f3c62f629b59163a7f6543a159f in / 
# Tue, 10 Feb 2026 17:41:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:25:49 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Feb 2026 20:25:49 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:25:49 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Feb 2026 20:26:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0a965c513bb522004ddb195fbb3cda7124559b8c7c082fc8626b2f45b4ce9a94';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ebf5f90f77e524593cba310d9e73d993bc8d3357af0127ec4627b1ce8236f385';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8353fb367a56fd150bd5b1facb595bde690c9f9a1f3db7db3b7fb240399a6ae9';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Feb 2026 20:26:39 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 17 Feb 2026 21:54:06 GMT
USER root
# Tue, 17 Feb 2026 21:54:06 GMT
ARG VERBOSE=false
# Tue, 17 Feb 2026 21:54:06 GMT
ARG OPENJ9_SCC=true
# Tue, 17 Feb 2026 21:54:06 GMT
ARG LIBERTY_VERSION=26.0.0.1
# Tue, 17 Feb 2026 21:54:06 GMT
ARG LIBERTY_BUILD_LABEL=cl260120260112-1902
# Tue, 17 Feb 2026 21:54:06 GMT
ARG LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8
# Tue, 17 Feb 2026 21:54:06 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.1 org.opencontainers.image.revision=cl260120260112-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.1 com.ibm.websphere.liberty.version=26.0.0.1
# Tue, 17 Feb 2026 21:54:06 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Tue, 17 Feb 2026 21:54:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.1 BuildLabel=cl260120260112-1902
# Tue, 17 Feb 2026 21:54:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 17 Feb 2026 21:54:06 GMT
ARG LIBERTY_URL
# Tue, 17 Feb 2026 21:54:06 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 17 Feb 2026 21:54:15 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:54:15 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 17 Feb 2026 21:54:16 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 17 Feb 2026 21:54:17 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 17 Feb 2026 21:54:17 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 17 Feb 2026 21:54:18 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 17 Feb 2026 21:54:18 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Tue, 17 Feb 2026 21:54:26 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 17 Feb 2026 21:54:26 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Tue, 17 Feb 2026 21:54:26 GMT
USER 1001
# Tue, 17 Feb 2026 21:54:26 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 17 Feb 2026 21:54:26 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 17 Feb 2026 21:54:26 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:4e2905dbd81d6a42c24ec5f7ce51f2d8f24a616b4fe2e90d0be791922a8d3b5f`  
		Last Modified: Tue, 10 Feb 2026 18:14:06 GMT  
		Size: 28.0 MB (28004382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77d17bf550a6cfe5ae28c00f12c4faa501f3dcc6d38bb384909465bb4f46478`  
		Last Modified: Tue, 17 Feb 2026 20:27:06 GMT  
		Size: 1.5 MB (1455847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbf297943659132d399cdba79372f26c58e6fba15ec4b1c07aa432bc5db1b72`  
		Last Modified: Tue, 17 Feb 2026 20:27:09 GMT  
		Size: 133.3 MB (133270713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c9619ea3b4d7570d7f8249be2d5e9a66be7fe3d817cfdfcccb65dad67eb9f9`  
		Last Modified: Tue, 17 Feb 2026 21:54:49 GMT  
		Size: 114.8 KB (114781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c93aa2219ab6916471647470a3c4d664bc40162c60dfbd8b4edab0b18346cd`  
		Last Modified: Tue, 17 Feb 2026 21:54:50 GMT  
		Size: 18.0 MB (18039178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1514283cb7e77c83b5f1e5e701676b245f04483680f9f525d674009f9bf94799`  
		Last Modified: Tue, 17 Feb 2026 21:54:49 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d65f0e5fb2836b522e48130265fe3255c05152b39cc7ab7240731bac14b66cd`  
		Last Modified: Tue, 17 Feb 2026 21:54:49 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9cef0ab9f21d03fa15559788fb4d89b2a355e5e589d30eb9ec253e60467949`  
		Last Modified: Tue, 17 Feb 2026 21:54:50 GMT  
		Size: 14.1 KB (14120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c9f487c1e07228d22c86419a1595aa4fdf7cc25dc327571d08b07c252ad43e`  
		Last Modified: Tue, 17 Feb 2026 21:54:50 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2feb2ebd7b0dcafa7373fa0583d0cc79e625a689292c8b82c443a11ea185a674`  
		Last Modified: Tue, 17 Feb 2026 21:54:50 GMT  
		Size: 15.0 KB (14991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48666323745ccb8ae3a4ead52f89f4ada719903044f2b3103888fb00b8db281c`  
		Last Modified: Tue, 17 Feb 2026 21:54:51 GMT  
		Size: 6.1 MB (6125480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:97ea5bff3a41854ee07a5eaaedb04c94343d67b5a2c69095be698d6e72f0b540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2342069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d329ba17928fb8b75f2116bbd4a05f55dfdfec6abb972ad7b1171a94bec4a100`

```dockerfile
```

-	Layers:
	-	`sha256:bcaab56de2a258aea35f7da3d4762459451010e23f9d6070be0db60b9d52bc74`  
		Last Modified: Tue, 17 Feb 2026 21:54:49 GMT  
		Size: 2.3 MB (2303089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76001dc0e72f07c5caaa8d1c7d521e0422010b89f016c9e657e77e49ef445fcf`  
		Last Modified: Tue, 17 Feb 2026 21:54:49 GMT  
		Size: 39.0 KB (38980 bytes)  
		MIME: application/vnd.in-toto+json
