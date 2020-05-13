## `websphere-liberty:kernel`

```console
$ docker pull websphere-liberty@sha256:d319d7331660734e602a4162c01e1887687b3f6da25cdc2840e9455eedd3dbf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:kernel` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:c4e4967dc9add09e1dc9168c2f3d2fccd6731bae5a28f48eefc0cee96b7aaaf5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179335624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5627435747f905d4176a02a88d1ea9a515badef1ac075ebea32be80c3c250ce9`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:00 GMT
ADD file:c3e6bb316dfa6b81dd4478aaa310df532883b1c0a14edeec3f63d641980c1789 in / 
# Fri, 24 Apr 2020 01:07:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 14:38:58 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 14:39:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 17:22:12 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 17:22:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 17:22:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 06 May 2020 18:58:38 GMT
ARG VERBOSE=false
# Wed, 06 May 2020 18:58:38 GMT
ARG OPENJ9_SCC=true
# Wed, 13 May 2020 01:40:48 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.5 org.opencontainers.image.revision=cl200520200429-1655 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 13 May 2020 01:40:48 GMT
ENV LIBERTY_VERSION=20.0.0_05
# Wed, 13 May 2020 01:40:49 GMT
ARG LIBERTY_URL
# Wed, 13 May 2020 01:40:49 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 13 May 2020 01:40:57 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 01:40:57 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 May 2020 01:40:58 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.5 BuildLabel=cl200520200429-1655
# Wed, 13 May 2020 01:40:58 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 13 May 2020 01:40:59 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 13 May 2020 01:40:59 GMT
COPY dir:bb23f4a336cfd1ff1404ca5678fffa89fb2b03183a93be37634e2c00eb179c47 in /opt/ibm/helpers/ 
# Wed, 13 May 2020 01:41:00 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 13 May 2020 01:41:00 GMT
COPY dir:666712edd8ef5cc75494f8a2dc944895b0c1ec9b80e66f7bb4de84169066792b in /licenses/ 
# Wed, 13 May 2020 01:41:01 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 13 May 2020 01:41:13 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 13 May 2020 01:41:13 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 13 May 2020 01:41:13 GMT
USER 1001
# Wed, 13 May 2020 01:41:13 GMT
EXPOSE 9080 9443
# Wed, 13 May 2020 01:41:14 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 13 May 2020 01:41:14 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:23884877105a7ff84a910895cd044061a4561385ff6c36480ee080b76ec0e771`  
		Last Modified: Sat, 04 Apr 2020 12:21:10 GMT  
		Size: 26.7 MB (26689802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc38caa0f5b94141276220daaf428892096e4afd24b05668cd188311e00a635f`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 35.4 KB (35367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2910811b6c4227c2f42aaea9a3dd5f53b1d469f67e2cf7e601f631b119b61ff7`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36505266dcc64eeb1010bd2112e6f73981e1a8246e4f6d4e287763b57f101b0b`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a528cffcbfa77f36f260d896e265cfb925555d14069b6cb510319dbe87d2e393`  
		Last Modified: Wed, 29 Apr 2020 03:27:55 GMT  
		Size: 3.0 MB (2965011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc65fe0ac24ec55f1cda0e25f07bba60ccd2ee3ff62f7355c9773cf51145e7e0`  
		Last Modified: Wed, 06 May 2020 17:27:06 GMT  
		Size: 130.3 MB (130335315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6d4ca5f8bb632c0e80975540d27cbd5093c3d88251220e0f669a6fce7c36ea`  
		Last Modified: Wed, 13 May 2020 01:49:53 GMT  
		Size: 13.6 MB (13597568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723394fd9b1bafaf15079181404a2ea004e0cc0232c2a9de7723e8e8b96e8ca2`  
		Last Modified: Wed, 13 May 2020 01:49:51 GMT  
		Size: 653.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4bc471ea1672f3bb39faa09fb14ba48c9170e262b409e902a88695394f786b0`  
		Last Modified: Wed, 13 May 2020 01:49:50 GMT  
		Size: 6.7 KB (6722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9c6d9083abad2a2df794fec61738a9c29fa783b4db7c4b92500f44ed6f2158`  
		Last Modified: Wed, 13 May 2020 01:49:50 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4518abc222a3a41ebb58c46a1fca9306bce1de9c0aa8af2b2ca364bede51ce`  
		Last Modified: Wed, 13 May 2020 01:49:50 GMT  
		Size: 57.4 KB (57423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2dedf70964323fdef7a448f65a9edbcbf762a6ba987e24174953b47cfec390`  
		Last Modified: Wed, 13 May 2020 01:49:50 GMT  
		Size: 7.6 KB (7561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0d3aa0717ec9b2b85d2fd203a2afceaee8c0dc9607bcdb90af6eb39dfdfb0e`  
		Last Modified: Wed, 13 May 2020 01:49:51 GMT  
		Size: 5.6 MB (5638946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel` - linux; 386

```console
$ docker pull websphere-liberty@sha256:21c2835a021b91c09268f12dc8f3c61f590c1b34d7669aeacf3792d83a7ef016
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162573580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e89243446a76e85ea4bf274dd0ad9e6fd0e763e50ced541577b62bee7dfcb74`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 20 Mar 2020 18:38:55 GMT
ADD file:d859d389e38b7ac70fd56f97e38d52a77b58e72b96237a4302d1984cdd912a55 in / 
# Fri, 20 Mar 2020 18:38:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 18:38:57 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 18:38:58 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 18:38:58 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 19:06:34 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 20 Mar 2020 19:06:41 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:06:42 GMT
ENV JAVA_VERSION=1.8.0_sr6fp6
# Fri, 20 Mar 2020 19:07:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='87f9d45b7e1fa65ec018479f3ca7da69a03b52b0da10b8d1555142eec8ab0093';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='b5f825047c9bb5d360fb83694f12e17b1a5a15abf94ac82cd0a3aea32c9a361c';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f3c04cd07ef269c24373840eae6f59c7db7a16d2e206d393ba93efa6dbb8d74f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2bbefda96f7d1a5f1694893961e92ccc59dfa50375ae5450675d7a4213d5812e';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d5b0508d53d1c7382c06f5bc1daf3d57c19c70d851e86e6b1162bcd93f616f7e';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 20 Mar 2020 19:07:26 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 20 Mar 2020 19:31:53 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.3 org.opencontainers.image.revision=cl200320200305-1433
# Fri, 20 Mar 2020 19:31:53 GMT
ENV LIBERTY_VERSION=20.0.0_03
# Fri, 20 Mar 2020 19:31:53 GMT
ARG LIBERTY_URL
# Fri, 20 Mar 2020 19:31:53 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 20 Mar 2020 19:32:02 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:32:03 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2020 19:32:03 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.3 BuildLabel=cl200320200305-1433
# Fri, 20 Mar 2020 19:32:03 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Fri, 20 Mar 2020 19:32:04 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 20 Mar 2020 19:32:04 GMT
COPY dir:0d0cedab2fbb7208b9d81afa78e9f15b12b71232224a2fe9753c00b7b72bd72e in /opt/ibm/helpers/ 
# Fri, 20 Mar 2020 19:32:05 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 20 Mar 2020 19:32:05 GMT
COPY dir:9277507d983008afcf8df6e0bfe2735bd4e92717515dbb3a7e268c830f213489 in /licenses/ 
# Fri, 20 Mar 2020 19:32:06 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 20 Mar 2020 19:32:06 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Fri, 20 Mar 2020 19:32:06 GMT
USER 1001
# Fri, 20 Mar 2020 19:32:06 GMT
EXPOSE 9080 9443
# Fri, 20 Mar 2020 19:32:07 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 20 Mar 2020 19:32:07 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:765ce743592771b94ad8ff27e281e66c13f6039962c7dde4dbe47123081e015b`  
		Last Modified: Mon, 16 Mar 2020 15:38:41 GMT  
		Size: 27.1 MB (27122453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59dc9c4739090a3d2f7265f1f8184b1cbd8ae133b863f8aa93ec5cf1761ee7a5`  
		Last Modified: Fri, 20 Mar 2020 18:39:35 GMT  
		Size: 34.6 KB (34625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a5b698281c077f48fc598e698f0619e4d00a2fedc1832fc95e9cf281408f63`  
		Last Modified: Fri, 20 Mar 2020 18:39:34 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaebe599891b1e1befc10d752a117cc5615ec2dd3913d399fd66e26e0cace3e5`  
		Last Modified: Fri, 20 Mar 2020 18:39:34 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f829150bc8a53a37ac17eb34838fa33c990881a4031bc650a9dae26b3f7880e`  
		Last Modified: Fri, 20 Mar 2020 19:09:23 GMT  
		Size: 3.0 MB (2992132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17b9ccc4baf3a1ffa517a03c7c3d01900136b128b36a83558c67c42e6c1cbaa`  
		Last Modified: Fri, 20 Mar 2020 19:09:35 GMT  
		Size: 118.8 MB (118756706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5011972f1876d464fb62206211a5b5e162ba2603bf20fc4cd0f2b4ffd311cd9`  
		Last Modified: Fri, 20 Mar 2020 19:39:16 GMT  
		Size: 13.6 MB (13600436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5395b713d5baa0917182ca82077b6fa2a0c51789907f96cbb12455586d9fa9b`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389324a3d9489b2fbcd5946f9d24285c0171c3218470e4a5e2d45c731cefc522`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 3.5 KB (3515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38ea596499e1f23ce426826250984869e92da50aec5845a6233a76d7764bfd1`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea3197b55235384f836e31a605c460f6cb7196f68dc29c65640738d8aa50188`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 57.4 KB (57426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683f76bf565cdb9e59c325f24357eb6b164555ed8629a4b8383448239608966d`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 4.4 KB (4358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:1c8e0b6667bc3601fdc8c43e5ea053aa1a72b40660f4491543216d5aaf87e5d0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 MB (191168210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7714c7550e477477ca52f770f359e80c66ee4e79debb6ac675a5f944c73f7252`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 23 Apr 2020 20:42:30 GMT
ADD file:726a32203fbcaae787c10740754e38dcb186778893e6d078db3cba0f49ee6b3c in / 
# Thu, 23 Apr 2020 20:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:42:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:42:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:42:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 11:49:15 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 11:50:06 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 18:16:50 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 18:17:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 18:18:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 06 May 2020 18:57:25 GMT
ARG VERBOSE=false
# Wed, 06 May 2020 18:57:29 GMT
ARG OPENJ9_SCC=true
# Wed, 13 May 2020 02:25:17 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.5 org.opencontainers.image.revision=cl200520200429-1655 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 13 May 2020 02:25:19 GMT
ENV LIBERTY_VERSION=20.0.0_05
# Wed, 13 May 2020 02:25:23 GMT
ARG LIBERTY_URL
# Wed, 13 May 2020 02:25:26 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 13 May 2020 02:25:54 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 02:25:57 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 May 2020 02:26:00 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.5 BuildLabel=cl200520200429-1655
# Wed, 13 May 2020 02:26:02 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 13 May 2020 02:26:08 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 13 May 2020 02:26:10 GMT
COPY dir:bb23f4a336cfd1ff1404ca5678fffa89fb2b03183a93be37634e2c00eb179c47 in /opt/ibm/helpers/ 
# Wed, 13 May 2020 02:26:11 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 13 May 2020 02:26:11 GMT
COPY dir:666712edd8ef5cc75494f8a2dc944895b0c1ec9b80e66f7bb4de84169066792b in /licenses/ 
# Wed, 13 May 2020 02:26:18 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 13 May 2020 02:26:37 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 13 May 2020 02:26:41 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 13 May 2020 02:26:42 GMT
USER 1001
# Wed, 13 May 2020 02:26:45 GMT
EXPOSE 9080 9443
# Wed, 13 May 2020 02:26:48 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 13 May 2020 02:26:50 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:beed3bd0a281cacead564771f079ed9ee8b272a2ed0e28f533e188f3d21fee6e`  
		Last Modified: Mon, 06 Apr 2020 15:40:20 GMT  
		Size: 30.4 MB (30400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae14d2411b83450b8afe92058b998540c56ec42f1ddd7581e8e9fe629c442f89`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82678240be3a5c783512ff7336f2b10837ae126958bc6bd1b476a8d039c08771`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307ad4f24078fd763b41ec7c1772f2fd5238fed1bae36c5d42d28ec9adbffb9`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df114b83a5a3444a39237d52fb0ddee6b46bc18624f26febb7c6a00effacdd4`  
		Last Modified: Fri, 24 Apr 2020 11:54:50 GMT  
		Size: 3.1 MB (3093321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a3df9e59dafede5e9e49376b8d92ca46f947103b310001473fb6ed575cc9c4`  
		Last Modified: Wed, 06 May 2020 18:21:07 GMT  
		Size: 138.8 MB (138811758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03009e7a193af76f04c5ba944a88b4dd9068c7043515fd05548e92f1267119b4`  
		Last Modified: Wed, 13 May 2020 02:43:17 GMT  
		Size: 13.6 MB (13598163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ba10b719d7dbe1418741db6d97d13495eb1806f80fbad1b090862cc7b1a27e`  
		Last Modified: Wed, 13 May 2020 02:43:10 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9ed01840c95fc2ae00ca4b04aa99eed46226c776b0bedd40664cab6892b9e3`  
		Last Modified: Wed, 13 May 2020 02:43:05 GMT  
		Size: 6.8 KB (6756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dcb38b1aafd6805891a5a2d91e97f67d927a1abc8d5eeb15ba0f73407db6028`  
		Last Modified: Wed, 13 May 2020 02:43:04 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7311255d391474821e6ff5aba8d6844bc5c9e2e40471b5dd96bf62ba2405d63`  
		Last Modified: Wed, 13 May 2020 02:43:05 GMT  
		Size: 57.4 KB (57423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4086b9a963efb5453b0fea08bcf7e2929b72c96b01c26a75e664c9f3afa08073`  
		Last Modified: Wed, 13 May 2020 02:43:05 GMT  
		Size: 7.7 KB (7667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10845d30a458cfbc46d86e2e1b648a37e2179fa8b3decaecb2ef008679f1811d`  
		Last Modified: Wed, 13 May 2020 02:43:09 GMT  
		Size: 5.2 MB (5155624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:17ad53f6e73154f07f7d62b27b65207e3dd08c181d788c62e15813be75ca9054
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.1 MB (175057327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff8cf332833514b77a40c245be412aa8e54ab2f2e7e6ee72a38333702324d69`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 23 Apr 2020 17:52:20 GMT
ADD file:ea66ef2a01c547f771866bfa221969f8a30489c28d2a81be8dde7f40e73da33b in / 
# Thu, 23 Apr 2020 17:52:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 17:52:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 17:52:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 17:52:31 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 07:57:51 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 07:57:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 19:01:14 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 19:02:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 19:02:18 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 06 May 2020 20:03:05 GMT
ARG VERBOSE=false
# Wed, 06 May 2020 20:03:06 GMT
ARG OPENJ9_SCC=true
# Wed, 13 May 2020 02:04:17 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.5 org.opencontainers.image.revision=cl200520200429-1655 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 13 May 2020 02:04:17 GMT
ENV LIBERTY_VERSION=20.0.0_05
# Wed, 13 May 2020 02:04:17 GMT
ARG LIBERTY_URL
# Wed, 13 May 2020 02:04:17 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 13 May 2020 02:04:28 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 02:04:29 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 May 2020 02:04:29 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.5 BuildLabel=cl200520200429-1655
# Wed, 13 May 2020 02:04:30 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 13 May 2020 02:04:31 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 13 May 2020 02:04:31 GMT
COPY dir:bb23f4a336cfd1ff1404ca5678fffa89fb2b03183a93be37634e2c00eb179c47 in /opt/ibm/helpers/ 
# Wed, 13 May 2020 02:04:31 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 13 May 2020 02:04:32 GMT
COPY dir:666712edd8ef5cc75494f8a2dc944895b0c1ec9b80e66f7bb4de84169066792b in /licenses/ 
# Wed, 13 May 2020 02:04:33 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 13 May 2020 02:04:42 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 13 May 2020 02:04:43 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 13 May 2020 02:04:43 GMT
USER 1001
# Wed, 13 May 2020 02:04:44 GMT
EXPOSE 9080 9443
# Wed, 13 May 2020 02:04:44 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 13 May 2020 02:04:44 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:13b4c2e4bb97a2a80bb0e557eeba41e4adea0f5e18352e359bca3f847193899c`  
		Last Modified: Mon, 06 Apr 2020 15:41:16 GMT  
		Size: 25.4 MB (25365338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471a80e39fb485b86610de915eaaad3d867cc97e460b6da3bb656e03520e8a63`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 36.2 KB (36171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0c128ddabc6a980ec71426ade04fc9bba2e1afcdc243e2d09c316b635f814`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678052ac148ee123df2f0773eb3a0f5f90490ada8b9a5705363b18a2f45fbe88`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcddcb26914bba3154202a6794cc606bb36373fd4a5954207d25c2acbb21027`  
		Last Modified: Fri, 24 Apr 2020 08:00:28 GMT  
		Size: 2.7 MB (2678829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c629705dbca4f2a1136866fdaec045c1f892fffb23cc1ccafc872548ab2f0f07`  
		Last Modified: Wed, 06 May 2020 19:04:43 GMT  
		Size: 127.6 MB (127581919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe801f2b89f9345aadeb354549d0292e450fb0dcb2f05114267dfa41dc17c7b`  
		Last Modified: Wed, 13 May 2020 02:14:07 GMT  
		Size: 13.6 MB (13597693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb074960db033d0fe77cb254530c8fb0f3165054fcd05cb25b48bf46709d934f`  
		Last Modified: Wed, 13 May 2020 02:14:06 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf8ce9ccdeef14be347d4eea0454804c26c05c937050bfe9acedadba6d8ed1d`  
		Last Modified: Wed, 13 May 2020 02:14:05 GMT  
		Size: 6.8 KB (6752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19aae72bbb91e65c36cc465befcbe663afa035418ebd33b67c0691d0045ddc6d`  
		Last Modified: Wed, 13 May 2020 02:14:05 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78cf06b5fdf737a91c52f4e8883e6c49264ca7d67ba4dc52921c740c0f860c5`  
		Last Modified: Wed, 13 May 2020 02:14:10 GMT  
		Size: 57.4 KB (57422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160e16fbd6a9b4d1f8234afbded3916eb1c7a390f1cfbc35bef8fd0795b4de25`  
		Last Modified: Wed, 13 May 2020 02:14:09 GMT  
		Size: 7.7 KB (7657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949d85f370790b38f9728f9bddcfca885a18f077b6f6661c4f70815574ac798a`  
		Last Modified: Wed, 13 May 2020 02:14:06 GMT  
		Size: 5.7 MB (5723545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
