## `websphere-liberty:kernel-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:a5ea7d40b3d6d32f4a564e265fadeb760c60358a373d55b0cd93d5feb85ab0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:kernel-java8-ibmjava` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:cdd6afc44016571202fe1d7b219c96f3df1d71e57b81b2e75f89f703a2742605
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190275562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31d1fff14f1f304d147cc19efb5d7d53df7093483006491342880b38fc008aa`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:00:40 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 25 Apr 2024 23:00:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:00:47 GMT
ENV JAVA_VERSION=8.0.8.21
# Thu, 25 Apr 2024 23:01:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a381d174001bbc558c8911b952c30c2a4fe6dea78a9ff6a25a2db9ac5e7fd952';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='7e1ee0174aea6cd2a41a561beb4e9b61b7b1d73bc3b8bf68a7d47c2f6ba7e555';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='80aed9b6510c2cdc2484435d44d7a50fb744ce4f2ae673fa090eddb222cf66fc';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='e7f5d2623a6932095deb2320b3eaa8fd70cf4131653113eb7ff950e276af1cfb';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz;
# Thu, 25 Apr 2024 23:01:01 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 26 Apr 2024 05:43:07 GMT
USER root
# Fri, 26 Apr 2024 05:43:08 GMT
ARG VERBOSE=false
# Fri, 26 Apr 2024 05:43:08 GMT
ARG OPENJ9_SCC=true
# Sat, 27 Apr 2024 01:17:00 GMT
ARG LIBERTY_VERSION=24.0.0.4
# Sat, 27 Apr 2024 01:17:00 GMT
ARG LIBERTY_BUILD_LABEL=cl240420240408-2000
# Sat, 27 Apr 2024 01:17:00 GMT
ARG LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3
# Sat, 27 Apr 2024 01:17:00 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.4 org.opencontainers.image.revision=cl240420240408-2000 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Sat, 27 Apr 2024 01:17:01 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Sat, 27 Apr 2024 01:17:01 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.4 BuildLabel=cl240420240408-2000
# Sat, 27 Apr 2024 01:17:17 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*;
# Sat, 27 Apr 2024 01:17:17 GMT
ARG LIBERTY_URL
# Sat, 27 Apr 2024 01:17:17 GMT
ARG DOWNLOAD_OPTIONS=
# Sat, 27 Apr 2024 01:17:25 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Apr 2024 01:17:25 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Sat, 27 Apr 2024 01:17:27 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env
# Sat, 27 Apr 2024 01:17:27 GMT
COPY file:7278f8f20139aab77b5c9fa76ad85e8a92836053c3ecfb9f5925f1a19788ef47 in /opt/ibm/NOTICES 
# Sat, 27 Apr 2024 01:17:27 GMT
COPY dir:9bc2ef96ad4f191171bf4612e561c64bae28466984c4742002b7dba3b9ffb3ad in /opt/ibm/helpers/ 
# Sat, 27 Apr 2024 01:17:27 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Sat, 27 Apr 2024 01:17:28 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Sat, 27 Apr 2024 01:17:35 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Sat, 27 Apr 2024 01:17:35 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Sat, 27 Apr 2024 01:17:35 GMT
USER 1001
# Sat, 27 Apr 2024 01:17:36 GMT
EXPOSE 9080 9443
# Sat, 27 Apr 2024 01:17:36 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Sat, 27 Apr 2024 01:17:36 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3066bb336ddeade3e29eac1b48ce34f7ff3f10b32bea015f60e84d42e08c51`  
		Last Modified: Thu, 25 Apr 2024 23:01:41 GMT  
		Size: 1.5 MB (1469827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d971fe79f2b59111abc7c1e4d5f3f20220b796afc5bcfcbc501be627b6c9a2f`  
		Last Modified: Thu, 25 Apr 2024 23:01:50 GMT  
		Size: 135.0 MB (134973373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13d9f63d0a49f3ddcd7b7b5ed214da56e42a94ac661fed21b56f27db467d145`  
		Last Modified: Sat, 27 Apr 2024 02:30:57 GMT  
		Size: 266.6 KB (266632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835b3b1877489d035c8a4fa062df2e64f25438a0f09c4ccf46e240c673e8990d`  
		Last Modified: Sat, 27 Apr 2024 02:30:59 GMT  
		Size: 17.4 MB (17365998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481c15581648ed0e4d811d830a6474a0ecd5b156a972232d9620d32ff687badd`  
		Last Modified: Sat, 27 Apr 2024 02:30:57 GMT  
		Size: 646.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9453d1091643d812c66812085c95b2e079fe93711b2e1a064cd00510fb7a79a1`  
		Last Modified: Sat, 27 Apr 2024 02:30:55 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c6869874019d37cc1c2f0c6a96bb4550cf1e3dd11707166b191e9c6904df16`  
		Last Modified: Sat, 27 Apr 2024 02:30:55 GMT  
		Size: 11.9 KB (11871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2484c4cde77e9bea5c513844d49bed49f586708e14d19708d3cdc4775090b6a2`  
		Last Modified: Sat, 27 Apr 2024 02:30:55 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e41da66e94fe938d6ec48f104c086672e920761b7d6e5b281bc6b363cd9edd`  
		Last Modified: Sat, 27 Apr 2024 02:30:55 GMT  
		Size: 12.8 KB (12795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5312611162810a681f6574f50603b10c5e87d456049575a57c56f10b3a24bf60`  
		Last Modified: Sat, 27 Apr 2024 02:30:56 GMT  
		Size: 5.7 MB (5732896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:5a7fdb4a94f3c2b50f23001be57b2ae1dd4736cb324d60fdd8b33e024787d4f9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195504008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9b8d418b3b169213227660e69aa227440c79afd81748807e07da43a2767701b`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:13 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:17 GMT
ADD file:3ab2760f4e449111dcca3f0816583c72999e1ce2ec20beac068dccfd6c9d8b81 in / 
# Sat, 27 Apr 2024 13:18:17 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:38:39 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 02 May 2024 01:38:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:38:58 GMT
ENV JAVA_VERSION=8.0.8.21
# Thu, 02 May 2024 01:39:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a381d174001bbc558c8911b952c30c2a4fe6dea78a9ff6a25a2db9ac5e7fd952';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='7e1ee0174aea6cd2a41a561beb4e9b61b7b1d73bc3b8bf68a7d47c2f6ba7e555';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='80aed9b6510c2cdc2484435d44d7a50fb744ce4f2ae673fa090eddb222cf66fc';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='e7f5d2623a6932095deb2320b3eaa8fd70cf4131653113eb7ff950e276af1cfb';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz;
# Thu, 02 May 2024 01:39:14 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Thu, 02 May 2024 03:48:41 GMT
USER root
# Thu, 02 May 2024 03:48:41 GMT
ARG VERBOSE=false
# Thu, 02 May 2024 03:48:42 GMT
ARG OPENJ9_SCC=true
# Thu, 02 May 2024 03:48:42 GMT
ARG LIBERTY_VERSION=24.0.0.4
# Thu, 02 May 2024 03:48:43 GMT
ARG LIBERTY_BUILD_LABEL=cl240420240408-2000
# Thu, 02 May 2024 03:48:43 GMT
ARG LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3
# Thu, 02 May 2024 03:48:44 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.4 org.opencontainers.image.revision=cl240420240408-2000 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 02 May 2024 03:48:45 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Thu, 02 May 2024 03:48:46 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.4 BuildLabel=cl240420240408-2000
# Thu, 02 May 2024 03:49:06 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*;
# Thu, 02 May 2024 03:49:07 GMT
ARG LIBERTY_URL
# Thu, 02 May 2024 03:49:07 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 02 May 2024 03:49:25 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:49:26 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 02 May 2024 03:49:32 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env
# Thu, 02 May 2024 03:49:32 GMT
COPY file:7278f8f20139aab77b5c9fa76ad85e8a92836053c3ecfb9f5925f1a19788ef47 in /opt/ibm/NOTICES 
# Thu, 02 May 2024 03:49:32 GMT
COPY dir:9bc2ef96ad4f191171bf4612e561c64bae28466984c4742002b7dba3b9ffb3ad in /opt/ibm/helpers/ 
# Thu, 02 May 2024 03:49:33 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 02 May 2024 03:49:36 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 02 May 2024 03:49:50 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 02 May 2024 03:49:51 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Thu, 02 May 2024 03:49:52 GMT
USER 1001
# Thu, 02 May 2024 03:49:53 GMT
EXPOSE 9080 9443
# Thu, 02 May 2024 03:49:54 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 02 May 2024 03:49:55 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:ef1313ed517c6def5644ab70e25cc66f1c4cd52b1e81c07fb33bfb8850b39c25`  
		Last Modified: Thu, 02 May 2024 01:40:15 GMT  
		Size: 35.6 MB (35588524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d160f4318a88a056643db72fa03a8b4f47253fd4510ad83ce855372df5d000c4`  
		Last Modified: Thu, 02 May 2024 01:40:10 GMT  
		Size: 1.6 MB (1574876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652c37f70e74c81bb3fe7fc7503829554be956098a00f4944fc6722049cd6c70`  
		Last Modified: Thu, 02 May 2024 01:40:21 GMT  
		Size: 135.4 MB (135415281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a8602e5058dc54fb5593d85340a04c75bdad8062d25f8804f309e05ae1f208`  
		Last Modified: Thu, 02 May 2024 04:19:53 GMT  
		Size: 271.1 KB (271086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72036ae681f1d460c76a3d0a26781fe630fccc7d0d00336f9cc3ee77ceac80f3`  
		Last Modified: Thu, 02 May 2024 04:19:54 GMT  
		Size: 17.4 MB (17366716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533562bf024fef400b1e54dd426664a0d852f08aeb75663ecc122fb1e4e4085f`  
		Last Modified: Thu, 02 May 2024 04:19:53 GMT  
		Size: 641.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef2ad9142028242e2c19751c202903c863dc38c0a18e43ebc62ffb9c11acfb2`  
		Last Modified: Thu, 02 May 2024 04:19:50 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71b98e2680c5e0b0f277f8471e9f4afe5f8a027365d0c584b82179bfc2f6b71`  
		Last Modified: Thu, 02 May 2024 04:19:51 GMT  
		Size: 11.9 KB (11868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8697b8652c092191c2adbc251970b3f1025ac45b1589b06fefa38c5019e81b5`  
		Last Modified: Thu, 02 May 2024 04:19:50 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2524c605e39cf90d2925b9e488c9e7cc75e1c1f94962245f78afe4402cdb04`  
		Last Modified: Thu, 02 May 2024 04:19:50 GMT  
		Size: 12.8 KB (12798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a5162906625b48362ca00e14d5aa1925aeb2948ca420e0fb786dc41c8c5ed2`  
		Last Modified: Thu, 02 May 2024 04:19:51 GMT  
		Size: 5.3 MB (5260425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:226d12f03ae95f71319ba44ff9bf5f9fa94d78fd163cf458982d999fffb93e4c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.5 MB (185548822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38960db8f23f0b1f04fd780c49f9c2ad3db8a25dd132c2dae197bc3af77fc16`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 27 Apr 2024 13:52:56 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:52:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:52:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:52:56 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:52:58 GMT
ADD file:7d693ab3b1f45d4992a119ec94444efc96c176ad954375f3bc1299ab813a46a0 in / 
# Sat, 27 Apr 2024 13:52:58 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:12:28 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 02 May 2024 01:12:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:12:34 GMT
ENV JAVA_VERSION=8.0.8.21
# Thu, 02 May 2024 01:12:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a381d174001bbc558c8911b952c30c2a4fe6dea78a9ff6a25a2db9ac5e7fd952';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='7e1ee0174aea6cd2a41a561beb4e9b61b7b1d73bc3b8bf68a7d47c2f6ba7e555';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='80aed9b6510c2cdc2484435d44d7a50fb744ce4f2ae673fa090eddb222cf66fc';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='e7f5d2623a6932095deb2320b3eaa8fd70cf4131653113eb7ff950e276af1cfb';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz;
# Thu, 02 May 2024 01:12:45 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Thu, 02 May 2024 01:56:05 GMT
USER root
# Thu, 02 May 2024 01:56:05 GMT
ARG VERBOSE=false
# Thu, 02 May 2024 01:56:05 GMT
ARG OPENJ9_SCC=true
# Thu, 02 May 2024 01:56:06 GMT
ARG LIBERTY_VERSION=24.0.0.4
# Thu, 02 May 2024 01:56:06 GMT
ARG LIBERTY_BUILD_LABEL=cl240420240408-2000
# Thu, 02 May 2024 01:56:06 GMT
ARG LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3
# Thu, 02 May 2024 01:56:06 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.4 org.opencontainers.image.revision=cl240420240408-2000 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 02 May 2024 01:56:06 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Thu, 02 May 2024 01:56:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.4 BuildLabel=cl240420240408-2000
# Thu, 02 May 2024 01:56:12 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*;
# Thu, 02 May 2024 01:56:12 GMT
ARG LIBERTY_URL
# Thu, 02 May 2024 01:56:12 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 02 May 2024 01:56:18 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:56:19 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 02 May 2024 01:56:19 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env
# Thu, 02 May 2024 01:56:20 GMT
COPY file:7278f8f20139aab77b5c9fa76ad85e8a92836053c3ecfb9f5925f1a19788ef47 in /opt/ibm/NOTICES 
# Thu, 02 May 2024 01:56:20 GMT
COPY dir:9bc2ef96ad4f191171bf4612e561c64bae28466984c4742002b7dba3b9ffb3ad in /opt/ibm/helpers/ 
# Thu, 02 May 2024 01:56:20 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 02 May 2024 01:56:20 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 02 May 2024 01:56:27 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 02 May 2024 01:56:28 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Thu, 02 May 2024 01:56:28 GMT
USER 1001
# Thu, 02 May 2024 01:56:28 GMT
EXPOSE 9080 9443
# Thu, 02 May 2024 01:56:28 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 02 May 2024 01:56:28 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:ffda8878ec88daab976ebae63a8dc770c7ff669cb06828bf12b1a5acca67f1f8`  
		Last Modified: Thu, 02 May 2024 01:13:50 GMT  
		Size: 28.6 MB (28637522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ddcae10b4f44029844c59ada01f332a62187c487a21182c2b4143cc0c7db95`  
		Last Modified: Thu, 02 May 2024 01:13:46 GMT  
		Size: 1.5 MB (1477663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f427c19ea7cb57eb7d7067a9ce08f65db2424d32c3ae665f2b21e9013b1e447`  
		Last Modified: Thu, 02 May 2024 01:13:56 GMT  
		Size: 132.0 MB (131955405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe8c53e140cdefa4fb24b876c564728b24f9e021de0d794d391fde78fd4987b`  
		Last Modified: Thu, 02 May 2024 02:24:21 GMT  
		Size: 268.0 KB (267970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e9c0e573d1bac182f92766919a27b37e08c102760365fcbba923ee68bfddae`  
		Last Modified: Thu, 02 May 2024 02:24:22 GMT  
		Size: 17.4 MB (17366179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5158b5f096171eea7a81b576aae5a607b808f1c0af4768b2ac71faeb6a99c730`  
		Last Modified: Thu, 02 May 2024 02:24:21 GMT  
		Size: 639.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ff630ebe4c019a4dbc3998af1c687ffe9d7dc62bab11846b76d9aec0e1205c`  
		Last Modified: Thu, 02 May 2024 02:24:20 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a972396352ef590f15ea86f10713c9b381a30e5172d8403ce5ec098873a5fcf`  
		Last Modified: Thu, 02 May 2024 02:24:20 GMT  
		Size: 11.9 KB (11868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507c9b1f5607b18dc5ed698d945999bfa4a5fd9bd3860f90c431da3a0b108e9f`  
		Last Modified: Thu, 02 May 2024 02:24:20 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a075bce32ad365f4933196778c84e10e914bc2377e6a95a2a154e8a70a012494`  
		Last Modified: Thu, 02 May 2024 02:24:20 GMT  
		Size: 12.8 KB (12790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37eccd02712a805a23c95626293d417537b81e6cf23c08bcd51f2435acb9b70`  
		Last Modified: Thu, 02 May 2024 02:24:21 GMT  
		Size: 5.8 MB (5816992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
