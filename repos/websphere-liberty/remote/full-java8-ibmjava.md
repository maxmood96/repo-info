## `websphere-liberty:full-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:a7afbd3c9b380f4c5709b603d5f8497f34176601afe2d5dc54d4fb2b23a3132b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:full-java8-ibmjava` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:b9b8f0865c9f3eabf112e4bcb1d9e5120f252ff8f465a800e0408e8a3588d24e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.5 MB (555504925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e49996e944c46c4c2883478f03682008e5e56ad3ffebe59a7ceec6c356da89`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:02:50 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 16 Feb 2024 02:02:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:02:57 GMT
ENV JAVA_VERSION=8.0.8.20
# Fri, 16 Feb 2024 02:03:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a5245fa2b6c500d9ca470b1ca36c88b8968d8e80956e439f4b09cad6dd5be132';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='db0f736f644a137218a452a039160a57b752fa338eb78e131948950750a226dc';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='c2826f490be3b6e34d71e6e1e20e35c7afe200693bce2139873a78cdd00547f7';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='4270b39c020b3830d0cd8b42f8b7f066b781375fd907d88843fb53c980dfb431';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz;
# Fri, 16 Feb 2024 02:03:10 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 16 Feb 2024 06:54:30 GMT
USER root
# Fri, 16 Feb 2024 06:54:30 GMT
ARG VERBOSE=false
# Fri, 16 Feb 2024 06:54:30 GMT
ARG OPENJ9_SCC=true
# Fri, 01 Mar 2024 03:17:44 GMT
ARG LIBERTY_VERSION=24.0.0.2
# Fri, 01 Mar 2024 03:17:44 GMT
ARG LIBERTY_BUILD_LABEL=cl240220240212-1928
# Fri, 01 Mar 2024 03:17:44 GMT
ARG LIBERTY_SHA=bd9c64cbf086f03e81ee50e4a44acc6f05af191a
# Fri, 01 Mar 2024 03:17:44 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.2 org.opencontainers.image.revision=cl240220240212-1928 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 01 Mar 2024 03:17:44 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Fri, 01 Mar 2024 03:17:44 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.2 BuildLabel=cl240220240212-1928
# Fri, 01 Mar 2024 03:17:57 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240220240212-1928 LIBERTY_SHA=bd9c64cbf086f03e81ee50e4a44acc6f05af191a LIBERTY_VERSION=24.0.0.2 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*;
# Fri, 01 Mar 2024 03:17:57 GMT
ARG LIBERTY_URL
# Fri, 01 Mar 2024 03:17:58 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 01 Mar 2024 03:18:06 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240220240212-1928 LIBERTY_SHA=bd9c64cbf086f03e81ee50e4a44acc6f05af191a LIBERTY_VERSION=24.0.0.2 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Mar 2024 03:18:06 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 01 Mar 2024 03:18:07 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240220240212-1928 LIBERTY_SHA=bd9c64cbf086f03e81ee50e4a44acc6f05af191a LIBERTY_VERSION=24.0.0.2 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env
# Fri, 01 Mar 2024 03:18:08 GMT
COPY file:7278f8f20139aab77b5c9fa76ad85e8a92836053c3ecfb9f5925f1a19788ef47 in /opt/ibm/NOTICES 
# Fri, 01 Mar 2024 03:18:08 GMT
COPY dir:f656e580b7f8af010b78a1edbf92e39c72d0fe4747bc6b8d0d82a780dffe857c in /opt/ibm/helpers/ 
# Fri, 01 Mar 2024 03:18:08 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 01 Mar 2024 03:18:08 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240220240212-1928 LIBERTY_SHA=bd9c64cbf086f03e81ee50e4a44acc6f05af191a LIBERTY_VERSION=24.0.0.2 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 01 Mar 2024 03:18:16 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240220240212-1928 LIBERTY_SHA=bd9c64cbf086f03e81ee50e4a44acc6f05af191a LIBERTY_VERSION=24.0.0.2 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 01 Mar 2024 03:18:16 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 01 Mar 2024 03:18:16 GMT
USER 1001
# Fri, 01 Mar 2024 03:18:16 GMT
EXPOSE 9080 9443
# Fri, 01 Mar 2024 03:18:16 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 01 Mar 2024 03:18:16 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 01 Mar 2024 03:19:10 GMT
ARG VERBOSE=false
# Fri, 01 Mar 2024 03:19:10 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 01 Mar 2024 03:26:03 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw;
# Fri, 01 Mar 2024 03:26:04 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 01 Mar 2024 03:26:40 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b34d9babed1e235b702edd16d2859552f37fb9c958f8643ceda5687b3295cb`  
		Last Modified: Fri, 16 Feb 2024 02:03:52 GMT  
		Size: 1.5 MB (1469321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa91dbe07b1aa852137baa2ce0f09591434d6e6b638cd18d505f0ddeeeee2d1`  
		Last Modified: Fri, 16 Feb 2024 02:04:01 GMT  
		Size: 135.0 MB (134957047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d6961442fdcc1a8b3c2c704dfc2f6057bbd988172652e3daf0930be4efd8a32`  
		Last Modified: Fri, 01 Mar 2024 04:29:35 GMT  
		Size: 266.2 KB (266204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682d1b8db74bbb8eb224427431f367037da7c6976d1182420b033b7ea8a64cb2`  
		Last Modified: Fri, 01 Mar 2024 04:29:36 GMT  
		Size: 17.4 MB (17416488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850b694d8cdf814e043a4a0e77818c7a5e98732241ae5e1ffe4d8c27cda11bd1`  
		Last Modified: Fri, 01 Mar 2024 04:29:34 GMT  
		Size: 643.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e889eab3054da0fe6fc4ca7f60fbe6f7576510e670d6728f7b42a94807e5b0c`  
		Last Modified: Fri, 01 Mar 2024 04:29:33 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf6b9c2254aebcab5b614c4744bfbdba7f63c05176b62eb41f4cacc367edd5c`  
		Last Modified: Fri, 01 Mar 2024 04:29:32 GMT  
		Size: 11.7 KB (11734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008cbaa7201a1489c00a8ae3ba5dca1cbb13b92a896d8dc54bdec71714c997eb`  
		Last Modified: Fri, 01 Mar 2024 04:29:32 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6818f582722f830db1865bd4abc080b8d55c8964f5ec28554c1c74dcb882c29`  
		Last Modified: Fri, 01 Mar 2024 04:29:32 GMT  
		Size: 12.7 KB (12652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f85ee1e0fa8b14a11178e13ae50e9b385ddc6d8996cb11304685b1ea7b99943`  
		Last Modified: Fri, 01 Mar 2024 04:29:33 GMT  
		Size: 5.7 MB (5725843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75ea1029c8888535f929a93c75ecee1bcf27c8b9e665455dce67a051aa397d4`  
		Last Modified: Fri, 01 Mar 2024 04:30:23 GMT  
		Size: 349.4 MB (349358461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99dd00ced3f87be874e427353c634877886ec6905813da8b907738bfeed7b145`  
		Last Modified: Fri, 01 Mar 2024 04:30:07 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2e49d70f09937b36a3bb4f7cc9975e5375fd05ed6c239c2e8683029e95368a`  
		Last Modified: Fri, 01 Mar 2024 04:30:08 GMT  
		Size: 15.8 MB (15833710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:e77549b41d5af6d80681ebc46db50391d20c5629eaf89c1b318ff07bf782dcb0
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.7 MB (557741031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f679febbe408fb74a4b84f56f13e5b8bc73be03eae93d24b3abf1826f9b851`
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
# Wed, 06 Mar 2024 01:50:12 GMT
ENV JAVA_VERSION=8.0.8.20
# Wed, 06 Mar 2024 01:50:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a5245fa2b6c500d9ca470b1ca36c88b8968d8e80956e439f4b09cad6dd5be132';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='db0f736f644a137218a452a039160a57b752fa338eb78e131948950750a226dc';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='c2826f490be3b6e34d71e6e1e20e35c7afe200693bce2139873a78cdd00547f7';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='4270b39c020b3830d0cd8b42f8b7f066b781375fd907d88843fb53c980dfb431';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz;
# Wed, 06 Mar 2024 01:50:28 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 06 Mar 2024 05:46:30 GMT
USER root
# Wed, 06 Mar 2024 05:46:31 GMT
ARG VERBOSE=false
# Wed, 06 Mar 2024 05:46:32 GMT
ARG OPENJ9_SCC=true
# Wed, 06 Mar 2024 05:46:33 GMT
ARG LIBERTY_VERSION=24.0.0.2
# Wed, 06 Mar 2024 05:46:34 GMT
ARG LIBERTY_BUILD_LABEL=cl240220240212-1928
# Wed, 06 Mar 2024 05:46:34 GMT
ARG LIBERTY_SHA=bd9c64cbf086f03e81ee50e4a44acc6f05af191a
# Wed, 06 Mar 2024 05:46:35 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.2 org.opencontainers.image.revision=cl240220240212-1928 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 06 Mar 2024 05:46:35 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 06 Mar 2024 05:46:36 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.2 BuildLabel=cl240220240212-1928
# Wed, 06 Mar 2024 05:46:57 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240220240212-1928 LIBERTY_SHA=bd9c64cbf086f03e81ee50e4a44acc6f05af191a LIBERTY_VERSION=24.0.0.2 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*;
# Wed, 06 Mar 2024 05:46:58 GMT
ARG LIBERTY_URL
# Wed, 06 Mar 2024 05:46:59 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 06 Mar 2024 05:47:20 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240220240212-1928 LIBERTY_SHA=bd9c64cbf086f03e81ee50e4a44acc6f05af191a LIBERTY_VERSION=24.0.0.2 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 05:47:23 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 06 Mar 2024 05:47:29 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240220240212-1928 LIBERTY_SHA=bd9c64cbf086f03e81ee50e4a44acc6f05af191a LIBERTY_VERSION=24.0.0.2 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env
# Wed, 06 Mar 2024 05:47:30 GMT
COPY file:7278f8f20139aab77b5c9fa76ad85e8a92836053c3ecfb9f5925f1a19788ef47 in /opt/ibm/NOTICES 
# Wed, 06 Mar 2024 05:47:30 GMT
COPY dir:f656e580b7f8af010b78a1edbf92e39c72d0fe4747bc6b8d0d82a780dffe857c in /opt/ibm/helpers/ 
# Wed, 06 Mar 2024 05:47:31 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 06 Mar 2024 05:47:35 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240220240212-1928 LIBERTY_SHA=bd9c64cbf086f03e81ee50e4a44acc6f05af191a LIBERTY_VERSION=24.0.0.2 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 06 Mar 2024 05:47:46 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240220240212-1928 LIBERTY_SHA=bd9c64cbf086f03e81ee50e4a44acc6f05af191a LIBERTY_VERSION=24.0.0.2 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 06 Mar 2024 05:47:48 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 06 Mar 2024 05:47:49 GMT
USER 1001
# Wed, 06 Mar 2024 05:47:50 GMT
EXPOSE 9080 9443
# Wed, 06 Mar 2024 05:47:52 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 06 Mar 2024 05:47:54 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 06 Mar 2024 05:50:09 GMT
ARG VERBOSE=false
# Wed, 06 Mar 2024 05:50:09 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 06 Mar 2024 05:58:07 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw;
# Wed, 06 Mar 2024 05:58:16 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 06 Mar 2024 05:59:08 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
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
	-	`sha256:28c5f237b434a323065c2fec50062fa18a422795d3d601cc29c2a4772a5cf80f`  
		Last Modified: Wed, 06 Mar 2024 01:51:36 GMT  
		Size: 135.4 MB (135410345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93d29617f6d03181e37c7b3f162f1e7b130eb393ebe98a1e807af68e8ebdddf`  
		Last Modified: Wed, 06 Mar 2024 07:16:58 GMT  
		Size: 270.7 KB (270653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b4f33e7cf6f0256a314a910b5397c2c550ef382ef7e477bf12d87f0955e5d6`  
		Last Modified: Wed, 06 Mar 2024 07:17:00 GMT  
		Size: 17.0 MB (17013604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f98307acd0a486c8ecafa8cb4a80ea00e527073fe18e9fb0087e22d5934cc1`  
		Last Modified: Wed, 06 Mar 2024 07:16:57 GMT  
		Size: 641.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2712ce7b71d38db7c1ac42517de975c4f49310ecdce20094fe21fb3fbeb8f890`  
		Last Modified: Wed, 06 Mar 2024 07:16:55 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61798bdf301df9df6edaf8e3e6e6ccaca9730d86b5a1e96b23d73ecba9dc5e9`  
		Last Modified: Wed, 06 Mar 2024 07:16:55 GMT  
		Size: 11.7 KB (11732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b7d602926157a42cca0816b5c4bf53bf7740d23f09a8544da8477238cf0cc8`  
		Last Modified: Wed, 06 Mar 2024 07:16:55 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd28c41f1e77fe0e42d5d7d09d62ac1752f3ce2312287ad1995efed4b4dbc8c`  
		Last Modified: Wed, 06 Mar 2024 07:16:55 GMT  
		Size: 12.7 KB (12662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c397663884c3b384e845b1962e9662675fd6b38eaaa47ecc500c594a1826347c`  
		Last Modified: Wed, 06 Mar 2024 07:16:56 GMT  
		Size: 5.2 MB (5240600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5e8379efc90fffd4b4656632ae5fc6b002204fad6b470225ed2c703e19d9d5`  
		Last Modified: Wed, 06 Mar 2024 07:17:50 GMT  
		Size: 349.4 MB (349358595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f93f1fe9e1ef2c16d88da1d456348e44b257e4af1d2855dfb9a6b710094354`  
		Last Modified: Wed, 06 Mar 2024 07:17:30 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3e575b0040c36fbb5d4c115dccc637c9d6349f72dcfb2140a8f89b6c31e7c2`  
		Last Modified: Wed, 06 Mar 2024 07:17:32 GMT  
		Size: 13.2 MB (13222296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:ff68743a9c94e7c59b58f31e6d35f33cb7896197b84073bc427bceb8f778d720
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **550.6 MB (550630742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3f3e63f3d383a81c429b3bb9b7930d0263523139742d26868290327b488d35`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Feb 2024 10:05:41 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:05:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:05:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:05:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:05:43 GMT
ADD file:0903319c85e93418ab3b2652f358f9269f6605e20b1c6bd55a810d75e48d901d in / 
# Tue, 13 Feb 2024 10:05:43 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 07:10:23 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 16 Feb 2024 07:10:28 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 07:10:28 GMT
ENV JAVA_VERSION=8.0.8.20
# Fri, 16 Feb 2024 07:10:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a5245fa2b6c500d9ca470b1ca36c88b8968d8e80956e439f4b09cad6dd5be132';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='db0f736f644a137218a452a039160a57b752fa338eb78e131948950750a226dc';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='c2826f490be3b6e34d71e6e1e20e35c7afe200693bce2139873a78cdd00547f7';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='4270b39c020b3830d0cd8b42f8b7f066b781375fd907d88843fb53c980dfb431';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz;
# Fri, 16 Feb 2024 07:10:40 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 16 Feb 2024 11:51:05 GMT
USER root
# Fri, 16 Feb 2024 11:51:05 GMT
ARG VERBOSE=false
# Fri, 16 Feb 2024 11:51:05 GMT
ARG OPENJ9_SCC=true
# Fri, 01 Mar 2024 07:04:17 GMT
ARG LIBERTY_VERSION=24.0.0.2
# Fri, 01 Mar 2024 07:04:17 GMT
ARG LIBERTY_BUILD_LABEL=cl240220240212-1928
# Fri, 01 Mar 2024 07:04:17 GMT
ARG LIBERTY_SHA=bd9c64cbf086f03e81ee50e4a44acc6f05af191a
# Fri, 01 Mar 2024 07:04:17 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.2 org.opencontainers.image.revision=cl240220240212-1928 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 01 Mar 2024 07:04:17 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Fri, 01 Mar 2024 07:04:18 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.2 BuildLabel=cl240220240212-1928
# Fri, 01 Mar 2024 07:04:27 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240220240212-1928 LIBERTY_SHA=bd9c64cbf086f03e81ee50e4a44acc6f05af191a LIBERTY_VERSION=24.0.0.2 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*;
# Fri, 01 Mar 2024 07:04:27 GMT
ARG LIBERTY_URL
# Fri, 01 Mar 2024 07:04:27 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 01 Mar 2024 07:04:33 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240220240212-1928 LIBERTY_SHA=bd9c64cbf086f03e81ee50e4a44acc6f05af191a LIBERTY_VERSION=24.0.0.2 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Mar 2024 07:04:34 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 01 Mar 2024 07:04:35 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240220240212-1928 LIBERTY_SHA=bd9c64cbf086f03e81ee50e4a44acc6f05af191a LIBERTY_VERSION=24.0.0.2 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env
# Fri, 01 Mar 2024 07:04:36 GMT
COPY file:7278f8f20139aab77b5c9fa76ad85e8a92836053c3ecfb9f5925f1a19788ef47 in /opt/ibm/NOTICES 
# Fri, 01 Mar 2024 07:04:36 GMT
COPY dir:f656e580b7f8af010b78a1edbf92e39c72d0fe4747bc6b8d0d82a780dffe857c in /opt/ibm/helpers/ 
# Fri, 01 Mar 2024 07:04:36 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 01 Mar 2024 07:04:36 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240220240212-1928 LIBERTY_SHA=bd9c64cbf086f03e81ee50e4a44acc6f05af191a LIBERTY_VERSION=24.0.0.2 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 01 Mar 2024 07:04:42 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240220240212-1928 LIBERTY_SHA=bd9c64cbf086f03e81ee50e4a44acc6f05af191a LIBERTY_VERSION=24.0.0.2 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 01 Mar 2024 07:04:42 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 01 Mar 2024 07:04:43 GMT
USER 1001
# Fri, 01 Mar 2024 07:04:43 GMT
EXPOSE 9080 9443
# Fri, 01 Mar 2024 07:04:43 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 01 Mar 2024 07:04:43 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 01 Mar 2024 07:08:26 GMT
ARG VERBOSE=false
# Fri, 01 Mar 2024 07:08:26 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 01 Mar 2024 07:14:47 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw;
# Fri, 01 Mar 2024 07:14:53 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 01 Mar 2024 07:15:25 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:d1d8eb67dcb980dd20128629fc5978b1e44a91f745560a173227c42f99d34f1b`  
		Last Modified: Fri, 16 Feb 2024 06:33:37 GMT  
		Size: 28.6 MB (28638724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d011260d842a132666ed6a753532572f74149d7ea1c704faba9c28f331cf08af`  
		Last Modified: Fri, 16 Feb 2024 07:14:31 GMT  
		Size: 1.5 MB (1477197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f79fd7cedc6827b92ec763f7e2d0863f4865d71678048d12dacae20f47a5327`  
		Last Modified: Fri, 16 Feb 2024 07:14:39 GMT  
		Size: 131.9 MB (131939014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed8f5e38f515bae4de1eafc1edd3d2a18b8bd673ef747db0c45eb84e1ffac2f`  
		Last Modified: Fri, 01 Mar 2024 08:35:32 GMT  
		Size: 267.5 KB (267532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c20116707b6079cad1bc0e9ef144d2a8bf0ff16ec1a7de8df50c146cc83256b`  
		Last Modified: Fri, 01 Mar 2024 08:35:33 GMT  
		Size: 17.4 MB (17418421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f378e92fcea941680caa5b458c1cd1e271efaaa6948481c64f697c553e6159`  
		Last Modified: Fri, 01 Mar 2024 08:35:31 GMT  
		Size: 641.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5057b61265c02b785978c951eaf95fc3a290c77601976c7fa9ad4d09265e5e6e`  
		Last Modified: Fri, 01 Mar 2024 08:35:30 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf99d053f5f87c956393b77169f6474bc32e6705c74c0c5c680ea15dc7b66ab`  
		Last Modified: Fri, 01 Mar 2024 08:35:30 GMT  
		Size: 11.7 KB (11739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d6d09c5b6c69962bdc1dca87447d6c5251827af51caa339f792db81ad78159`  
		Last Modified: Fri, 01 Mar 2024 08:35:30 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa059eb5cbc0ecdc3609eb6cbf077e137606db07b4d23ca5624e4b49379341f`  
		Last Modified: Fri, 01 Mar 2024 08:35:30 GMT  
		Size: 12.7 KB (12654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9831b5d4a90ca85a61fd04248a3317323580f3599496b34b4b1e5406891a81ae`  
		Last Modified: Fri, 01 Mar 2024 08:35:31 GMT  
		Size: 5.8 MB (5800935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25d5b47c65d71f86ea71622f791d7ec166cb71515c6979ccdb5d47ec4e2e0d0`  
		Last Modified: Fri, 01 Mar 2024 08:36:09 GMT  
		Size: 349.4 MB (349359080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813a6173fa19fa8686c18e95bb6d92a75def8c6f0beb8308b2d7e8e803d993d0`  
		Last Modified: Fri, 01 Mar 2024 08:35:55 GMT  
		Size: 952.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd78906a9aaeb7dbf10b72b0418f522ca7d147ab8c73e640bfe4ecf56981dd1`  
		Last Modified: Fri, 01 Mar 2024 08:35:57 GMT  
		Size: 15.7 MB (15702052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
