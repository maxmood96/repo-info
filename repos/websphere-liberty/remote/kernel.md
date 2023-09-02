## `websphere-liberty:kernel`

```console
$ docker pull websphere-liberty@sha256:e59e2656b1cb243013e1f451edaeaaccac2dd90e6fe3fd1ee2028aa393f23d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:kernel` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:15e10070261d95b0257d0928d997d271d67959333a08c03348c7c77116f329dd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.9 MB (188876747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66624f719c89aea71498d7ed482addf059c42bab9749e28ef31e2bbb23f422dc`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 04 Aug 2023 04:52:57 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:52:59 GMT
ADD file:bb1fa1d9d012ae826908afdce8c9fa2feebf221b2ab032e1535255905144411a in / 
# Fri, 04 Aug 2023 04:53:00 GMT
CMD ["/bin/bash"]
# Thu, 17 Aug 2023 06:43:31 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 17 Aug 2023 06:43:41 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Mon, 21 Aug 2023 19:22:59 GMT
ENV JAVA_VERSION=8.0.8.10
# Mon, 21 Aug 2023 19:24:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0ba3f228adc03c78d620a9d79a01d681a81dade244834b53d8f5456947b0e74b';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='8793ed949c728ebf5c28db8c6d43e17e0580ad95173a51624c9dc74d2b154680';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='f4209abc6de52de6366ea771999eb0f420bb7132709455ca16438e0d4c3d4550';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='b84ce990439243beba14c3430a4072a8eab58bc9e41ca58f74efebdc64bc785c';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Mon, 21 Aug 2023 19:24:06 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Mon, 21 Aug 2023 22:34:49 GMT
USER root
# Mon, 21 Aug 2023 22:34:49 GMT
ARG VERBOSE=false
# Mon, 21 Aug 2023 22:34:49 GMT
ARG OPENJ9_SCC=true
# Wed, 23 Aug 2023 23:52:43 GMT
ARG LIBERTY_VERSION=23.0.0.8
# Wed, 23 Aug 2023 23:52:43 GMT
ARG LIBERTY_BUILD_LABEL=cl230820230807-0401
# Wed, 23 Aug 2023 23:52:43 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=23.0.0.8 org.opencontainers.image.revision=cl230820230807-0401 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 23 Aug 2023 23:52:43 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 23 Aug 2023 23:52:44 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=23.0.0.8 BuildLabel=cl230820230807-0401
# Wed, 23 Aug 2023 23:52:51 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_VERSION=23.0.0.8 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*;
# Wed, 23 Aug 2023 23:52:51 GMT
ARG LIBERTY_URL
# Wed, 23 Aug 2023 23:52:52 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 23 Aug 2023 23:53:03 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_VERSION=23.0.0.8 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 23 Aug 2023 23:53:03 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 23 Aug 2023 23:53:04 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env
# Wed, 23 Aug 2023 23:53:04 GMT
COPY file:7278f8f20139aab77b5c9fa76ad85e8a92836053c3ecfb9f5925f1a19788ef47 in /opt/ibm/NOTICES 
# Wed, 23 Aug 2023 23:53:04 GMT
COPY dir:9172a78a02626bf06a9783bc065253393e37161c6beb27c7b44b89f4d54a4a69 in /opt/ibm/helpers/ 
# Wed, 23 Aug 2023 23:53:04 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 23 Aug 2023 23:53:05 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 23 Aug 2023 23:53:11 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 23 Aug 2023 23:53:12 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 23 Aug 2023 23:53:12 GMT
USER 1001
# Wed, 23 Aug 2023 23:53:12 GMT
EXPOSE 9080 9443
# Wed, 23 Aug 2023 23:53:12 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 23 Aug 2023 23:53:12 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:99de9192b4afd13ed65aeae58d55b38e5231eb97a743921357b7d5b4c0c903c4`  
		Last Modified: Fri, 04 Aug 2023 09:25:19 GMT  
		Size: 30.4 MB (30437960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d80cb2eef8352f8d51cee0579d0d7e53c9b3089f0aedb190b60897ae6b2e9c9`  
		Last Modified: Thu, 17 Aug 2023 06:47:15 GMT  
		Size: 1.5 MB (1469099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c362fdbb5a459b13ed19a97e848dfdc64e14ce1c72ff7494e56ef8913411d293`  
		Last Modified: Mon, 21 Aug 2023 19:26:41 GMT  
		Size: 134.2 MB (134152601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113ded1b9b8e9287d07b7ab65d5f3f503b41a172f3494815a7c328a12235e5ca`  
		Last Modified: Thu, 24 Aug 2023 00:22:36 GMT  
		Size: 266.0 KB (265952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f677accc9254cdafb9fa8f52455e34ad895d2676ff5d05d6e2691e9d2448754e`  
		Last Modified: Thu, 24 Aug 2023 00:22:37 GMT  
		Size: 17.0 MB (17010171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e8db33cf332d19f5ccf07ce02a6ebe6d1dfaa98f0be3c8155862e1ae806fce9`  
		Last Modified: Thu, 24 Aug 2023 00:22:36 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b238a40f0c7cc386f4f995ab2686c03579de2f522696a04b808a04dadd5ad51f`  
		Last Modified: Thu, 24 Aug 2023 00:22:34 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8224341fcb710de14a444bf728fdf747d42eec0cf3289137d259fd83afc0ef`  
		Last Modified: Thu, 24 Aug 2023 00:22:34 GMT  
		Size: 11.3 KB (11255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e838718e76f6863fe850f4c85c11fa297c2c7de17ee0ba63fcfe3495482c8ea`  
		Last Modified: Thu, 24 Aug 2023 00:22:34 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03e606d316abf78e0a1da9d3293a269cf55511a1f0ab65b62e887c57426fee2`  
		Last Modified: Thu, 24 Aug 2023 00:22:34 GMT  
		Size: 12.2 KB (12192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ac76937981f36ad968711781207efa706b776a300063e1c247345a9f22a5c9`  
		Last Modified: Thu, 24 Aug 2023 00:22:35 GMT  
		Size: 5.5 MB (5515102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:65051af1fa85b38700267ba4abeed0d0d4f26dbad2c3a16122f69cefdacc199f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193624216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d5c28209a680d69262f8b666958d66f4042bdd9ada326dafb81da1a94ca95f`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 04 Aug 2023 04:56:16 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:56:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:56:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:56:17 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:56:20 GMT
ADD file:0e9b840e6824ee009acbddc2d337fd5083ebe606393cf7532cdca4f108813ca3 in / 
# Fri, 04 Aug 2023 04:56:20 GMT
CMD ["/bin/bash"]
# Thu, 17 Aug 2023 07:14:37 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 17 Aug 2023 07:15:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Mon, 21 Aug 2023 19:16:43 GMT
ENV JAVA_VERSION=8.0.8.10
# Mon, 21 Aug 2023 19:18:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0ba3f228adc03c78d620a9d79a01d681a81dade244834b53d8f5456947b0e74b';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='8793ed949c728ebf5c28db8c6d43e17e0580ad95173a51624c9dc74d2b154680';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='f4209abc6de52de6366ea771999eb0f420bb7132709455ca16438e0d4c3d4550';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='b84ce990439243beba14c3430a4072a8eab58bc9e41ca58f74efebdc64bc785c';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Mon, 21 Aug 2023 19:18:03 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Mon, 21 Aug 2023 23:19:29 GMT
USER root
# Mon, 21 Aug 2023 23:19:29 GMT
ARG VERBOSE=false
# Mon, 21 Aug 2023 23:19:30 GMT
ARG OPENJ9_SCC=true
# Thu, 24 Aug 2023 00:00:45 GMT
ARG LIBERTY_VERSION=23.0.0.8
# Thu, 24 Aug 2023 00:00:46 GMT
ARG LIBERTY_BUILD_LABEL=cl230820230807-0401
# Thu, 24 Aug 2023 00:00:46 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=23.0.0.8 org.opencontainers.image.revision=cl230820230807-0401 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 24 Aug 2023 00:00:47 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Thu, 24 Aug 2023 00:00:48 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=23.0.0.8 BuildLabel=cl230820230807-0401
# Thu, 24 Aug 2023 00:01:13 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_VERSION=23.0.0.8 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*;
# Thu, 24 Aug 2023 00:01:14 GMT
ARG LIBERTY_URL
# Thu, 24 Aug 2023 00:01:14 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 24 Aug 2023 00:01:33 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_VERSION=23.0.0.8 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 24 Aug 2023 00:01:34 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 24 Aug 2023 00:01:40 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env
# Thu, 24 Aug 2023 00:01:40 GMT
COPY file:7278f8f20139aab77b5c9fa76ad85e8a92836053c3ecfb9f5925f1a19788ef47 in /opt/ibm/NOTICES 
# Thu, 24 Aug 2023 00:01:40 GMT
COPY dir:9172a78a02626bf06a9783bc065253393e37161c6beb27c7b44b89f4d54a4a69 in /opt/ibm/helpers/ 
# Thu, 24 Aug 2023 00:01:41 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 24 Aug 2023 00:01:43 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 24 Aug 2023 00:01:57 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 24 Aug 2023 00:01:58 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Thu, 24 Aug 2023 00:01:58 GMT
USER 1001
# Thu, 24 Aug 2023 00:01:58 GMT
EXPOSE 9080 9443
# Thu, 24 Aug 2023 00:01:59 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 24 Aug 2023 00:01:59 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:09f4821f68917c7929419fff8bc583c406640180ea7d58eea03a95e463b8fb21`  
		Last Modified: Wed, 16 Aug 2023 02:15:01 GMT  
		Size: 35.7 MB (35712693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178c6af71882c03cbea1c4a79fb71458fc3e42c0589327d53c7ab2045de5bb83`  
		Last Modified: Thu, 17 Aug 2023 07:19:38 GMT  
		Size: 1.6 MB (1576539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d618244e05ea3bfd2945aa29181a9c5de3b9cd7dec32e296fc2b98a40d15b270`  
		Last Modified: Mon, 21 Aug 2023 19:21:44 GMT  
		Size: 133.8 MB (133845181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e50fcfebf1ac5104dfe3dc92682fad6acdd086a94be66fe2552565f477823b7`  
		Last Modified: Thu, 24 Aug 2023 00:38:06 GMT  
		Size: 270.4 KB (270429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:965cddee385b4a287d6d3ff33910c3917a21de5eb066b93612537efa52e9cf47`  
		Last Modified: Thu, 24 Aug 2023 00:38:09 GMT  
		Size: 17.0 MB (17010530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5621136af21e7f145b0fe775beadf19519c072c566e9a927d2b27b7fbc761f`  
		Last Modified: Thu, 24 Aug 2023 00:38:06 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d05529ef5f7411c3d658de8f413cac2de9f9a5587dc9b9e1d6f1ff40caed716`  
		Last Modified: Thu, 24 Aug 2023 00:38:04 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7dfeb21055e27d829a4d975643462a743119e527a48334286aabc0952d6f688`  
		Last Modified: Thu, 24 Aug 2023 00:38:04 GMT  
		Size: 11.2 KB (11250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180064c246a3d78209ee7e023d7a0781e83038cc1f959a61f797247d2be362b3`  
		Last Modified: Thu, 24 Aug 2023 00:38:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b015962b6c4b9800d821dfee8a96d3e8cef8a62bb1a271bb2dd789850bab9794`  
		Last Modified: Thu, 24 Aug 2023 00:38:04 GMT  
		Size: 12.2 KB (12189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:272a6c3124e2703e75a3714fc82c9f1624732a5547a0767d1ff4a7e00400a8bd`  
		Last Modified: Thu, 24 Aug 2023 00:38:05 GMT  
		Size: 5.2 MB (5182994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:dcaddcd1f64e3eadd55455da632eb81a4d9386a0331a9b5434bcd1a5007555df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183663210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8206acf02d9ae3c6ea88d2587c975832f4852f9e6eade01b2ffbab94b00cd0`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 16 Aug 2023 06:05:03 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:05:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:05:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:05:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:05:05 GMT
ADD file:58eccd685d73ff80ea235016d6e33d093e1063800d869935b67b59a1b8891344 in / 
# Wed, 16 Aug 2023 06:05:05 GMT
CMD ["/bin/bash"]
# Fri, 01 Sep 2023 23:30:39 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 01 Sep 2023 23:30:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Sep 2023 23:30:44 GMT
ENV JAVA_VERSION=8.0.8.10
# Fri, 01 Sep 2023 23:31:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0ba3f228adc03c78d620a9d79a01d681a81dade244834b53d8f5456947b0e74b';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='8793ed949c728ebf5c28db8c6d43e17e0580ad95173a51624c9dc74d2b154680';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='f4209abc6de52de6366ea771999eb0f420bb7132709455ca16438e0d4c3d4550';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='b84ce990439243beba14c3430a4072a8eab58bc9e41ca58f74efebdc64bc785c';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 01 Sep 2023 23:31:17 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Sat, 02 Sep 2023 00:49:17 GMT
USER root
# Sat, 02 Sep 2023 00:49:17 GMT
ARG VERBOSE=false
# Sat, 02 Sep 2023 00:49:17 GMT
ARG OPENJ9_SCC=true
# Sat, 02 Sep 2023 00:49:17 GMT
ARG LIBERTY_VERSION=23.0.0.8
# Sat, 02 Sep 2023 00:49:17 GMT
ARG LIBERTY_BUILD_LABEL=cl230820230807-0401
# Sat, 02 Sep 2023 00:49:17 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=23.0.0.8 org.opencontainers.image.revision=cl230820230807-0401 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Sat, 02 Sep 2023 00:49:18 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Sat, 02 Sep 2023 00:49:18 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=23.0.0.8 BuildLabel=cl230820230807-0401
# Sat, 02 Sep 2023 00:49:23 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_VERSION=23.0.0.8 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*;
# Sat, 02 Sep 2023 00:49:23 GMT
ARG LIBERTY_URL
# Sat, 02 Sep 2023 00:49:23 GMT
ARG DOWNLOAD_OPTIONS=
# Sat, 02 Sep 2023 00:49:28 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_VERSION=23.0.0.8 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 00:49:29 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Sat, 02 Sep 2023 00:49:30 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env
# Sat, 02 Sep 2023 00:49:30 GMT
COPY file:7278f8f20139aab77b5c9fa76ad85e8a92836053c3ecfb9f5925f1a19788ef47 in /opt/ibm/NOTICES 
# Sat, 02 Sep 2023 00:49:30 GMT
COPY dir:9172a78a02626bf06a9783bc065253393e37161c6beb27c7b44b89f4d54a4a69 in /opt/ibm/helpers/ 
# Sat, 02 Sep 2023 00:49:30 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Sat, 02 Sep 2023 00:49:31 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Sat, 02 Sep 2023 00:49:36 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Sat, 02 Sep 2023 00:49:37 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Sat, 02 Sep 2023 00:49:37 GMT
USER 1001
# Sat, 02 Sep 2023 00:49:37 GMT
EXPOSE 9080 9443
# Sat, 02 Sep 2023 00:49:37 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Sat, 02 Sep 2023 00:49:37 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:e19a32372cc8a39496c7cbc80d6c7213997c1b24d50309e770a59738f35c719d`  
		Last Modified: Fri, 01 Sep 2023 23:23:30 GMT  
		Size: 28.6 MB (28645834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082bfcb3965d1b3b304dbd9d3dece2a186f7a234747b8ba053e8fa9d206c3310`  
		Last Modified: Fri, 01 Sep 2023 23:34:58 GMT  
		Size: 1.5 MB (1477088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da84c8c756fa4d93c931978b103b3ebdb62be5e24c1cf90dcf7985cc90f6f32b`  
		Last Modified: Fri, 01 Sep 2023 23:35:07 GMT  
		Size: 130.7 MB (130706273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6324f34e4f6607af64de3e1445e1be38a1fea4aa6640c6507bac1babfc13ea9`  
		Last Modified: Sat, 02 Sep 2023 01:38:13 GMT  
		Size: 267.4 KB (267365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82191b72fe6d984143e159edad18215b94c7f625050f73c44d0d00d26e09c6b2`  
		Last Modified: Sat, 02 Sep 2023 01:38:14 GMT  
		Size: 17.0 MB (17010320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e935b1f06f7cf133f7bfe809ed4939b6249b3322b6920ce589c56517c2324db`  
		Last Modified: Sat, 02 Sep 2023 01:38:12 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a39e55d73a9562964af2e2feb9f5530ed03e1c33311f2c26aa368b34f49d2118`  
		Last Modified: Sat, 02 Sep 2023 01:38:11 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95203b77d16ea71d8d83fac6c87938745f79f0bab2a14bc2beef6d60719a67e`  
		Last Modified: Sat, 02 Sep 2023 01:38:11 GMT  
		Size: 11.3 KB (11253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f2b05362ceca2e83decfba5f3095603366270f77be8d60ea314f3face039ec`  
		Last Modified: Sat, 02 Sep 2023 01:38:11 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f6f742b9bc1ab3ee949766cab9bef57b402ac54887a25a397971827a867a6c`  
		Last Modified: Sat, 02 Sep 2023 01:38:11 GMT  
		Size: 12.2 KB (12173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3adb51fb6cb21daae96925257a9e1b4b6126723e73c71725792725425e66eb75`  
		Last Modified: Sat, 02 Sep 2023 01:38:12 GMT  
		Size: 5.5 MB (5530495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
