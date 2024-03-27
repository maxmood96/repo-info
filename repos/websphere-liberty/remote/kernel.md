## `websphere-liberty:kernel`

```console
$ docker pull websphere-liberty@sha256:879feffa4cd3953a5e00aa28f118f55b1763dc3ad268b55ca1adf55c12aa0c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:kernel` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:8331b126079fa9e944fc8f5c3bc107d892c364d0cd57b9ba7db493c95baddb31
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189924430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8cfb809768f0c224fa55c55c05237f3767c7fea03fe6a394a09512e9b25ade`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:28:57 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 06 Mar 2024 04:29:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Mar 2024 19:52:50 GMT
ENV JAVA_VERSION=8.0.8.21
# Tue, 19 Mar 2024 19:53:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a381d174001bbc558c8911b952c30c2a4fe6dea78a9ff6a25a2db9ac5e7fd952';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='7e1ee0174aea6cd2a41a561beb4e9b61b7b1d73bc3b8bf68a7d47c2f6ba7e555';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='80aed9b6510c2cdc2484435d44d7a50fb744ce4f2ae673fa090eddb222cf66fc';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='e7f5d2623a6932095deb2320b3eaa8fd70cf4131653113eb7ff950e276af1cfb';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz;
# Tue, 19 Mar 2024 19:53:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 19 Mar 2024 20:17:35 GMT
USER root
# Tue, 19 Mar 2024 20:17:35 GMT
ARG VERBOSE=false
# Tue, 19 Mar 2024 20:17:35 GMT
ARG OPENJ9_SCC=true
# Wed, 27 Mar 2024 00:04:44 GMT
ARG LIBERTY_VERSION=24.0.0.3
# Wed, 27 Mar 2024 00:04:44 GMT
ARG LIBERTY_BUILD_LABEL=cl240320240311-1901
# Wed, 27 Mar 2024 00:04:44 GMT
ARG LIBERTY_SHA=b5bcf3002850f5891d07a912f9673c5b89a10071
# Wed, 27 Mar 2024 00:04:44 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.3 org.opencontainers.image.revision=cl240320240311-1901 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 27 Mar 2024 00:04:45 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 27 Mar 2024 00:04:45 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.3 BuildLabel=cl240320240311-1901
# Wed, 27 Mar 2024 00:04:54 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240320240311-1901 LIBERTY_SHA=b5bcf3002850f5891d07a912f9673c5b89a10071 LIBERTY_VERSION=24.0.0.3 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*;
# Wed, 27 Mar 2024 00:04:54 GMT
ARG LIBERTY_URL
# Wed, 27 Mar 2024 00:04:55 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 27 Mar 2024 00:05:03 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240320240311-1901 LIBERTY_SHA=b5bcf3002850f5891d07a912f9673c5b89a10071 LIBERTY_VERSION=24.0.0.3 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 27 Mar 2024 00:05:03 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 27 Mar 2024 00:05:04 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240320240311-1901 LIBERTY_SHA=b5bcf3002850f5891d07a912f9673c5b89a10071 LIBERTY_VERSION=24.0.0.3 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env
# Wed, 27 Mar 2024 00:05:04 GMT
COPY file:7278f8f20139aab77b5c9fa76ad85e8a92836053c3ecfb9f5925f1a19788ef47 in /opt/ibm/NOTICES 
# Wed, 27 Mar 2024 00:05:05 GMT
COPY dir:f656e580b7f8af010b78a1edbf92e39c72d0fe4747bc6b8d0d82a780dffe857c in /opt/ibm/helpers/ 
# Wed, 27 Mar 2024 00:05:05 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 27 Mar 2024 00:05:05 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240320240311-1901 LIBERTY_SHA=b5bcf3002850f5891d07a912f9673c5b89a10071 LIBERTY_VERSION=24.0.0.3 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 27 Mar 2024 00:05:12 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240320240311-1901 LIBERTY_SHA=b5bcf3002850f5891d07a912f9673c5b89a10071 LIBERTY_VERSION=24.0.0.3 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 27 Mar 2024 00:05:13 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 27 Mar 2024 00:05:13 GMT
USER 1001
# Wed, 27 Mar 2024 00:05:13 GMT
EXPOSE 9080 9443
# Wed, 27 Mar 2024 00:05:13 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 27 Mar 2024 00:05:13 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba89721884a18e231a2358fec4f8d2aa4e12399d5170f30d637f3cc1e9edc12`  
		Last Modified: Wed, 06 Mar 2024 04:30:07 GMT  
		Size: 1.5 MB (1469281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d568370898a8f62b6ca614d4586aa22d69d0219c71b7a8a4e207d0c4ca2257f`  
		Last Modified: Tue, 19 Mar 2024 19:53:53 GMT  
		Size: 135.0 MB (134973422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14981c715a4bd6478374196ebb802f3679dd0a06de35f2888aaea332b73c5b7b`  
		Last Modified: Wed, 27 Mar 2024 00:30:19 GMT  
		Size: 266.2 KB (266181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c065cf3c370b192daf83144b6d6a4e25ba681dd202b645a4f4e1f1a8bc4fdff`  
		Last Modified: Wed, 27 Mar 2024 00:30:20 GMT  
		Size: 17.0 MB (17030937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536039f2fe46bbb89e8d97eec1eda3b775c532c7df5c0e97ecb50c48462d4042`  
		Last Modified: Wed, 27 Mar 2024 00:30:18 GMT  
		Size: 643.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e415b6079d478727708adc7c61874c56fa73830d535e60a936a90980a663d5`  
		Last Modified: Wed, 27 Mar 2024 00:30:16 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87247a0fc49026acfeb477f9f9bbbe422f331019b05ce2854b7b65381d1c5cd`  
		Last Modified: Wed, 27 Mar 2024 00:30:17 GMT  
		Size: 11.7 KB (11743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:118bb1248e997726b6c82809b0b653200ec791e77d5d258291414a0ad4e96f07`  
		Last Modified: Wed, 27 Mar 2024 00:30:16 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7098ffa2ca138acc0daf0bf1ebf2b9212607ad31e4624aeb4e0f3d696b38e8`  
		Last Modified: Wed, 27 Mar 2024 00:30:16 GMT  
		Size: 12.7 KB (12658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e0c46b743abf7e06ae95f8a89c39714817634bdb6928ac4f75ef9ad551abd1`  
		Last Modified: Wed, 27 Mar 2024 00:30:17 GMT  
		Size: 5.7 MB (5706464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:df6a567d587ad34bbb1956ca96a9f22669fcd23952ff5345acb8d507568a3ae9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.2 MB (195232894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d2a2f64ff544492ca232df96d0e889e9a5ca5c87b505862f6b08030fd4e186`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 01:50:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 06 Mar 2024 01:50:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Mar 2024 19:25:39 GMT
ENV JAVA_VERSION=8.0.8.21
# Tue, 19 Mar 2024 19:25:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a381d174001bbc558c8911b952c30c2a4fe6dea78a9ff6a25a2db9ac5e7fd952';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='7e1ee0174aea6cd2a41a561beb4e9b61b7b1d73bc3b8bf68a7d47c2f6ba7e555';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='80aed9b6510c2cdc2484435d44d7a50fb744ce4f2ae673fa090eddb222cf66fc';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='e7f5d2623a6932095deb2320b3eaa8fd70cf4131653113eb7ff950e276af1cfb';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz;
# Tue, 19 Mar 2024 19:25:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 19 Mar 2024 19:52:25 GMT
USER root
# Tue, 19 Mar 2024 19:52:26 GMT
ARG VERBOSE=false
# Tue, 19 Mar 2024 19:52:26 GMT
ARG OPENJ9_SCC=true
# Tue, 26 Mar 2024 23:42:13 GMT
ARG LIBERTY_VERSION=24.0.0.3
# Tue, 26 Mar 2024 23:42:13 GMT
ARG LIBERTY_BUILD_LABEL=cl240320240311-1901
# Tue, 26 Mar 2024 23:42:13 GMT
ARG LIBERTY_SHA=b5bcf3002850f5891d07a912f9673c5b89a10071
# Tue, 26 Mar 2024 23:42:14 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.3 org.opencontainers.image.revision=cl240320240311-1901 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Tue, 26 Mar 2024 23:42:14 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Tue, 26 Mar 2024 23:42:15 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.3 BuildLabel=cl240320240311-1901
# Tue, 26 Mar 2024 23:42:31 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240320240311-1901 LIBERTY_SHA=b5bcf3002850f5891d07a912f9673c5b89a10071 LIBERTY_VERSION=24.0.0.3 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*;
# Tue, 26 Mar 2024 23:42:32 GMT
ARG LIBERTY_URL
# Tue, 26 Mar 2024 23:42:32 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 26 Mar 2024 23:42:42 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240320240311-1901 LIBERTY_SHA=b5bcf3002850f5891d07a912f9673c5b89a10071 LIBERTY_VERSION=24.0.0.3 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Tue, 26 Mar 2024 23:42:43 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 26 Mar 2024 23:42:46 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240320240311-1901 LIBERTY_SHA=b5bcf3002850f5891d07a912f9673c5b89a10071 LIBERTY_VERSION=24.0.0.3 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env
# Tue, 26 Mar 2024 23:42:46 GMT
COPY file:7278f8f20139aab77b5c9fa76ad85e8a92836053c3ecfb9f5925f1a19788ef47 in /opt/ibm/NOTICES 
# Tue, 26 Mar 2024 23:42:46 GMT
COPY dir:f656e580b7f8af010b78a1edbf92e39c72d0fe4747bc6b8d0d82a780dffe857c in /opt/ibm/helpers/ 
# Tue, 26 Mar 2024 23:42:47 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Tue, 26 Mar 2024 23:42:48 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240320240311-1901 LIBERTY_SHA=b5bcf3002850f5891d07a912f9673c5b89a10071 LIBERTY_VERSION=24.0.0.3 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Tue, 26 Mar 2024 23:42:57 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240320240311-1901 LIBERTY_SHA=b5bcf3002850f5891d07a912f9673c5b89a10071 LIBERTY_VERSION=24.0.0.3 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Tue, 26 Mar 2024 23:42:58 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Tue, 26 Mar 2024 23:42:58 GMT
USER 1001
# Tue, 26 Mar 2024 23:42:58 GMT
EXPOSE 9080 9443
# Tue, 26 Mar 2024 23:42:58 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 26 Mar 2024 23:42:58 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140a853d05db5896b4301801c8f248e4544bc9cbe992489bc58fdbf0a2147cf8`  
		Last Modified: Wed, 06 Mar 2024 01:51:25 GMT  
		Size: 1.6 MB (1574416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448073ef720a52d0348ad31c320f57162b98335785796cbf039ae632bd05a154`  
		Last Modified: Tue, 19 Mar 2024 19:26:50 GMT  
		Size: 135.4 MB (135415301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d62c72b2f09e4bbe59ae0123ff15d2a5c00e02994222a54f232f577638be95b`  
		Last Modified: Wed, 27 Mar 2024 00:10:26 GMT  
		Size: 270.6 KB (270625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6ae33c160f0a54ced68291c877f40dbfdb7b73068b2145739cf3bfdeba612ad`  
		Last Modified: Wed, 27 Mar 2024 00:10:27 GMT  
		Size: 17.0 MB (17031546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a187a1435328be3342dd2af359b8ec641aca62a947cc4d1971062f176aaac24`  
		Last Modified: Wed, 27 Mar 2024 00:10:25 GMT  
		Size: 644.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670506d871e680afe675d852342a9c6be4ef0d1dba9bf01bf1de6143b970e634`  
		Last Modified: Wed, 27 Mar 2024 00:10:23 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b7f58f66a47cc2c2096d869ed2098cb8a724e1c3f2dc0fd9c9a0a1e65c2104`  
		Last Modified: Wed, 27 Mar 2024 00:10:22 GMT  
		Size: 11.7 KB (11737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d282465499f69ab5220de5d3a3ff24d5bcca498bb4cda5ae4b4429e29600630a`  
		Last Modified: Wed, 27 Mar 2024 00:10:22 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e7264e5221580e85bddd274030170986279c95f4965c7eccff0a8699b1bbd7`  
		Last Modified: Wed, 27 Mar 2024 00:10:22 GMT  
		Size: 12.7 KB (12662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a09fa7593bbefcd312f7318af6d1a9c1e7efebf2a68556c7fb653309a17614`  
		Last Modified: Wed, 27 Mar 2024 00:10:23 GMT  
		Size: 5.3 MB (5291421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:0f85c8d664c959910a86d7470903ac1d9e58050657601a09cdb093998f4de621
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185170159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc664b236f641d5a4b7646616a9773ed93cd8a2e411bd7c96e8cab2a10ff787`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:00 GMT
ADD file:fc6c0c3ab39493d732bf2a969cf1478735923705ad656cbc6398d4dbe45626fe in / 
# Tue, 27 Feb 2024 18:53:00 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:53:10 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 06 Mar 2024 04:53:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Mar 2024 20:08:32 GMT
ENV JAVA_VERSION=8.0.8.21
# Tue, 19 Mar 2024 20:08:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a381d174001bbc558c8911b952c30c2a4fe6dea78a9ff6a25a2db9ac5e7fd952';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='7e1ee0174aea6cd2a41a561beb4e9b61b7b1d73bc3b8bf68a7d47c2f6ba7e555';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='80aed9b6510c2cdc2484435d44d7a50fb744ce4f2ae673fa090eddb222cf66fc';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='e7f5d2623a6932095deb2320b3eaa8fd70cf4131653113eb7ff950e276af1cfb';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz;
# Tue, 19 Mar 2024 20:08:50 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 19 Mar 2024 21:08:40 GMT
USER root
# Tue, 19 Mar 2024 21:08:40 GMT
ARG VERBOSE=false
# Tue, 19 Mar 2024 21:08:40 GMT
ARG OPENJ9_SCC=true
# Wed, 27 Mar 2024 00:02:17 GMT
ARG LIBERTY_VERSION=24.0.0.3
# Wed, 27 Mar 2024 00:02:17 GMT
ARG LIBERTY_BUILD_LABEL=cl240320240311-1901
# Wed, 27 Mar 2024 00:02:17 GMT
ARG LIBERTY_SHA=b5bcf3002850f5891d07a912f9673c5b89a10071
# Wed, 27 Mar 2024 00:02:18 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.3 org.opencontainers.image.revision=cl240320240311-1901 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 27 Mar 2024 00:02:18 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 27 Mar 2024 00:02:18 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.3 BuildLabel=cl240320240311-1901
# Wed, 27 Mar 2024 00:02:25 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240320240311-1901 LIBERTY_SHA=b5bcf3002850f5891d07a912f9673c5b89a10071 LIBERTY_VERSION=24.0.0.3 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*;
# Wed, 27 Mar 2024 00:02:25 GMT
ARG LIBERTY_URL
# Wed, 27 Mar 2024 00:02:25 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 27 Mar 2024 00:02:31 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240320240311-1901 LIBERTY_SHA=b5bcf3002850f5891d07a912f9673c5b89a10071 LIBERTY_VERSION=24.0.0.3 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 27 Mar 2024 00:02:31 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 27 Mar 2024 00:02:33 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240320240311-1901 LIBERTY_SHA=b5bcf3002850f5891d07a912f9673c5b89a10071 LIBERTY_VERSION=24.0.0.3 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env
# Wed, 27 Mar 2024 00:02:33 GMT
COPY file:7278f8f20139aab77b5c9fa76ad85e8a92836053c3ecfb9f5925f1a19788ef47 in /opt/ibm/NOTICES 
# Wed, 27 Mar 2024 00:02:33 GMT
COPY dir:f656e580b7f8af010b78a1edbf92e39c72d0fe4747bc6b8d0d82a780dffe857c in /opt/ibm/helpers/ 
# Wed, 27 Mar 2024 00:02:33 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 27 Mar 2024 00:02:33 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240320240311-1901 LIBERTY_SHA=b5bcf3002850f5891d07a912f9673c5b89a10071 LIBERTY_VERSION=24.0.0.3 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 27 Mar 2024 00:02:39 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240320240311-1901 LIBERTY_SHA=b5bcf3002850f5891d07a912f9673c5b89a10071 LIBERTY_VERSION=24.0.0.3 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 27 Mar 2024 00:02:39 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 27 Mar 2024 00:02:39 GMT
USER 1001
# Wed, 27 Mar 2024 00:02:39 GMT
EXPOSE 9080 9443
# Wed, 27 Mar 2024 00:02:40 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 27 Mar 2024 00:02:40 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:34c2c4dff60b52886f8ffe75945626cde03551a775fc6e99a1aaee265e75df5f`  
		Last Modified: Wed, 06 Mar 2024 03:56:35 GMT  
		Size: 28.6 MB (28636756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030bdb96287595f0898b0f731954aac1bc39f56c6377e3b5474bfd5d2f48b5c8`  
		Last Modified: Wed, 06 Mar 2024 04:57:08 GMT  
		Size: 1.5 MB (1477377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7119bce7310bbd768fef2435363fd06765241e919f5fcc81bdc2b5db0082751`  
		Last Modified: Tue, 19 Mar 2024 20:13:22 GMT  
		Size: 132.0 MB (131955414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa88db6159cdd5c7e7c6dcf98da0845083f2dc9e0188bca708debe19c32203f`  
		Last Modified: Wed, 27 Mar 2024 00:48:53 GMT  
		Size: 267.6 KB (267650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2bb20e63ea8ae7ef2ae7ab986d12e55c3b79da1234846d035057c4a8a2e8b3`  
		Last Modified: Wed, 27 Mar 2024 00:48:55 GMT  
		Size: 17.0 MB (17031292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ca3727ebb783b697471f1f56542a07d2fe8f3630ad1848ce08ce5ce7ebe0d6`  
		Last Modified: Wed, 27 Mar 2024 00:48:53 GMT  
		Size: 641.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56051040cb076d0b2508191a5686989f035f5339ddbab358d496e6bbca170a17`  
		Last Modified: Wed, 27 Mar 2024 00:48:52 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921cd4c92f0c48b252d1028b5f405a6359979caf54ec897e2ab9d1e4483c70a2`  
		Last Modified: Wed, 27 Mar 2024 00:48:52 GMT  
		Size: 11.7 KB (11738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69c1f884c1f1492fee6933808b90b786c7f74acddde78c24f100aec83f0e050`  
		Last Modified: Wed, 27 Mar 2024 00:48:52 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a198dafc6cc2c96c2455a74f81f0442500552119ded13985cc23ebee3359d822`  
		Last Modified: Wed, 27 Mar 2024 00:48:52 GMT  
		Size: 12.7 KB (12655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360954d594f54573fccdab7a9d49e10e09e4a34e527bca47cb622a446e5755a5`  
		Last Modified: Wed, 27 Mar 2024 00:48:53 GMT  
		Size: 5.8 MB (5774840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
