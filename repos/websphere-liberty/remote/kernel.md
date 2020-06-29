## `websphere-liberty:kernel`

```console
$ docker pull websphere-liberty@sha256:18fe22e99e168752b068810c7a2e04e32538ca7277be52703264be66174b4837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:kernel` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:888d4e48c5a046cb193b146e517558d7ca923ed958aad7004b56a1153a609bf5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.4 MB (179412566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:244cbb0d09a73512caf528e44179654392876694fa951dd851c15f31014c4839`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 17 Jun 2020 01:20:29 GMT
ADD file:1e8d02626176dc8141df3c0a1365774ce73d79934654fe24a4b1e7f173108232 in / 
# Wed, 17 Jun 2020 01:20:30 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:20:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:20:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:20:32 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:37:25 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 17 Jun 2020 03:37:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Mon, 29 Jun 2020 20:25:14 GMT
ENV JAVA_VERSION=1.8.0_sr6fp11
# Mon, 29 Jun 2020 20:25:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='e318577a2c807fd515129c96b10e86c9ea2f8318a74d2ac54d53ff9fd85450cc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='708960c09d456e1b84b7caf0000995fc266af90cbcb6ca053bee0d19c625d5a6';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='43a40e8d1164e0904ef0a91100d4a6579e4075f6ea503a417d4122c4c1321f22';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='570cec9a573a1b849db8b8f5485813fce7a384c6de6090eec93e4427244aa5af';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='c9f43396f318f73bcb40f652a40debbb1cef83f36c3f3fc7cf03d5fcbdfd48c2';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Mon, 29 Jun 2020 20:25:57 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Mon, 29 Jun 2020 20:47:35 GMT
ARG VERBOSE=false
# Mon, 29 Jun 2020 20:47:35 GMT
ARG OPENJ9_SCC=true
# Mon, 29 Jun 2020 20:47:35 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.6 org.opencontainers.image.revision=cl200620200528-0414 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Mon, 29 Jun 2020 20:47:35 GMT
ENV LIBERTY_VERSION=20.0.0_06
# Mon, 29 Jun 2020 20:47:35 GMT
ARG LIBERTY_URL
# Mon, 29 Jun 2020 20:47:36 GMT
ARG DOWNLOAD_OPTIONS=
# Mon, 29 Jun 2020 20:47:45 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Mon, 29 Jun 2020 20:47:45 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jun 2020 20:47:46 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.6 BuildLabel=cl200620200528-0414
# Mon, 29 Jun 2020 20:47:46 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Mon, 29 Jun 2020 20:47:48 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Mon, 29 Jun 2020 20:47:48 GMT
COPY dir:eea9bd687cda20807296939d3f98c70b1d48a11ffe1e23ee8f0c373a62cce55b in /opt/ibm/helpers/ 
# Mon, 29 Jun 2020 20:47:49 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Mon, 29 Jun 2020 20:47:49 GMT
COPY dir:f50ec19c0b3217fa3d6d42c3ce4a254879f817de03e99e13f96ba6b66fb6862e in /licenses/ 
# Mon, 29 Jun 2020 20:47:50 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Mon, 29 Jun 2020 20:48:04 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Mon, 29 Jun 2020 20:48:04 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Mon, 29 Jun 2020 20:48:04 GMT
USER 1001
# Mon, 29 Jun 2020 20:48:05 GMT
EXPOSE 9080 9443
# Mon, 29 Jun 2020 20:48:05 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Mon, 29 Jun 2020 20:48:05 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:d7c3167c320d7a820935f54cf4290890ea19567da496ecf774e8773b35d5f065`  
		Last Modified: Wed, 27 May 2020 12:21:15 GMT  
		Size: 26.7 MB (26688718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131f805ec7fd68d45a887e2ef82de61de0247b4eb934ab03b7c933650e854baa`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 35.4 KB (35369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322ed380e680a77f30528ba013e3a802a7b44948a0609c7d1d732dd46a9a310d`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac240b130982ad1c3ba3188abbf18ba4e54bdd9e504ce2d5c2eff6d3e86b8dd`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2dd26a7c29d4b098cb319e4d86fd1639d057db338e91ef60d9f530f357f4f4`  
		Last Modified: Wed, 17 Jun 2020 03:40:09 GMT  
		Size: 3.0 MB (2957174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f35af379ec5c6dd81c589e15dacc5d147d598033f9b0f4f8e4756b7395a521`  
		Last Modified: Mon, 29 Jun 2020 20:30:06 GMT  
		Size: 130.3 MB (130341804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9f33b102947429416b3895c5df654323688db7b34bcba0360337881132b7b6`  
		Last Modified: Mon, 29 Jun 2020 20:57:32 GMT  
		Size: 13.8 MB (13764534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420d418db8c82ce671946e5462b5fa2eb7c0223cce0747a8748d6199980e5891`  
		Last Modified: Mon, 29 Jun 2020 20:57:31 GMT  
		Size: 652.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e78a44fb70de12d76c3c85cff542884466a4a1c1df82231e44fc56026dd179d`  
		Last Modified: Mon, 29 Jun 2020 20:57:30 GMT  
		Size: 9.0 KB (9033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3761e3782317848a488cd26dd74321fe7cb7ac94b5bc30dcc88dc6fb621d37f`  
		Last Modified: Mon, 29 Jun 2020 20:57:30 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c87877b4aef247770ca2cb897bbfb37729b8409865277078bc26830b86040ef`  
		Last Modified: Mon, 29 Jun 2020 20:57:30 GMT  
		Size: 57.2 KB (57208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d22a0a1d6efb4f67d49110031bb9a5cff4ae211bf19ad2bf9689cfc86d2b78`  
		Last Modified: Mon, 29 Jun 2020 20:57:30 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7337fabcdbbc0098001569bc195b43b67d8c81b7708a082f19a81c7978a563`  
		Last Modified: Mon, 29 Jun 2020 20:57:31 GMT  
		Size: 5.5 MB (5546899 bytes)  
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
$ docker pull websphere-liberty@sha256:104f27849dde04637bf638ca9857c4fec8fceaa4014ecd2bf65d5507e294960b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191326570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad117d90e08c5b5611ef13be2c9f2a594e63ff90919ecf00f03b1441a81a342`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 17 Jun 2020 01:23:28 GMT
ADD file:3d8a4167931b708419d8f212295ee2e69c2e17523d93de0f36af7c8b7adaf6b0 in / 
# Wed, 17 Jun 2020 01:23:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:23:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:23:53 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:23:59 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 01:45:15 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 17 Jun 2020 01:45:48 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:45:51 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 17 Jun 2020 01:46:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 17 Jun 2020 01:46:59 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 17 Jun 2020 04:15:55 GMT
ARG VERBOSE=false
# Wed, 17 Jun 2020 04:15:59 GMT
ARG OPENJ9_SCC=true
# Wed, 17 Jun 2020 04:16:03 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.6 org.opencontainers.image.revision=cl200620200528-0414 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 17 Jun 2020 04:16:05 GMT
ENV LIBERTY_VERSION=20.0.0_06
# Wed, 17 Jun 2020 04:16:08 GMT
ARG LIBERTY_URL
# Wed, 17 Jun 2020 04:16:11 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 17 Jun 2020 04:16:34 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 04:16:36 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2020 04:16:38 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.6 BuildLabel=cl200620200528-0414
# Wed, 17 Jun 2020 04:16:40 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 17 Jun 2020 04:16:46 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 17 Jun 2020 04:16:47 GMT
COPY dir:eea9bd687cda20807296939d3f98c70b1d48a11ffe1e23ee8f0c373a62cce55b in /opt/ibm/helpers/ 
# Wed, 17 Jun 2020 04:16:48 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 17 Jun 2020 04:16:49 GMT
COPY dir:f50ec19c0b3217fa3d6d42c3ce4a254879f817de03e99e13f96ba6b66fb6862e in /licenses/ 
# Wed, 17 Jun 2020 04:16:58 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 17 Jun 2020 04:17:21 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 17 Jun 2020 04:17:24 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 17 Jun 2020 04:17:27 GMT
USER 1001
# Wed, 17 Jun 2020 04:17:31 GMT
EXPOSE 9080 9443
# Wed, 17 Jun 2020 04:17:34 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 17 Jun 2020 04:17:38 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:c82758296165adcddbc1b265a621d9938f9c807decd8469ae7f939d875188bf5`  
		Last Modified: Sat, 30 May 2020 05:26:15 GMT  
		Size: 30.4 MB (30400411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740d34e8b0154512b13d50a28cb641b322092ef53e5681dd77102035104fbffe`  
		Last Modified: Wed, 17 Jun 2020 01:28:15 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e49637d96cd01435b847808eee898f2f13837bf3034497154962bb88ef0416b`  
		Last Modified: Wed, 17 Jun 2020 01:28:15 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042abc2d98a7172c5b211cb1f6be22813334814c096e94c8fbf0a7972587d765`  
		Last Modified: Wed, 17 Jun 2020 01:28:15 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a446a0d6a4df1037ac078e6bed2513a28de7be35a380a2b5db170b6b23d6d68d`  
		Last Modified: Wed, 17 Jun 2020 01:49:49 GMT  
		Size: 3.1 MB (3075370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a14b5e9a97244abf41ab9e0e76726c599ae775742054d82d6891eb990bd1a3`  
		Last Modified: Wed, 17 Jun 2020 01:50:06 GMT  
		Size: 138.8 MB (138811860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3264b55099c95348e7ebf7e70c1bc40b0b54360f9f733f8d520d98ffe673aac8`  
		Last Modified: Wed, 17 Jun 2020 04:37:32 GMT  
		Size: 13.8 MB (13765371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc0b1812c111bdb2741d8513a9ac41eb48785c0a9315003847548411a3a9361`  
		Last Modified: Wed, 17 Jun 2020 04:37:27 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f6cab65ec6163c51989a4463878631656f159b10d39f05e5dda63008e5fd00`  
		Last Modified: Wed, 17 Jun 2020 04:37:23 GMT  
		Size: 9.1 KB (9063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ab4b5f2bebdd4670689818104d208a119296deae96b3d3ae315cca0e6b95e5`  
		Last Modified: Wed, 17 Jun 2020 04:37:22 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffb074fbd5825aa21140f55448460cdb966612e517a02383a545dd41d02cbc7`  
		Last Modified: Wed, 17 Jun 2020 04:37:24 GMT  
		Size: 57.2 KB (57206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9b447e3bd7b994606d4fa9934a71aff6d889c4398c3953c6048d53d6fbb4ef`  
		Last Modified: Wed, 17 Jun 2020 04:37:22 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ffe6fe628517edc6255c0748be2c12a191db041b0abad59a6efcc6fb87ef57`  
		Last Modified: Wed, 17 Jun 2020 04:37:25 GMT  
		Size: 5.2 MB (5160049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:ffc63288c973be8d4c747326322b010bf1030ba2cea08ef9e8fd843b4f80778a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.2 MB (175214440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173558a659f66c4e795c15482a3b5625199ee6a7065a4bcf8699b5b9d24688c4`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 17 Jun 2020 01:41:48 GMT
ADD file:8708e93980b416070ba0bb024a7858748129059a85d2c771a4489c31710a9df1 in / 
# Wed, 17 Jun 2020 01:41:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:41:52 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:41:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:41:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:08:01 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 17 Jun 2020 03:08:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Mon, 29 Jun 2020 19:43:19 GMT
ENV JAVA_VERSION=1.8.0_sr6fp11
# Mon, 29 Jun 2020 19:43:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='e318577a2c807fd515129c96b10e86c9ea2f8318a74d2ac54d53ff9fd85450cc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='708960c09d456e1b84b7caf0000995fc266af90cbcb6ca053bee0d19c625d5a6';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='43a40e8d1164e0904ef0a91100d4a6579e4075f6ea503a417d4122c4c1321f22';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='570cec9a573a1b849db8b8f5485813fce7a384c6de6090eec93e4427244aa5af';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='c9f43396f318f73bcb40f652a40debbb1cef83f36c3f3fc7cf03d5fcbdfd48c2';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Mon, 29 Jun 2020 19:44:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Mon, 29 Jun 2020 20:02:24 GMT
ARG VERBOSE=false
# Mon, 29 Jun 2020 20:02:24 GMT
ARG OPENJ9_SCC=true
# Mon, 29 Jun 2020 20:02:24 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.6 org.opencontainers.image.revision=cl200620200528-0414 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Mon, 29 Jun 2020 20:02:25 GMT
ENV LIBERTY_VERSION=20.0.0_06
# Mon, 29 Jun 2020 20:02:25 GMT
ARG LIBERTY_URL
# Mon, 29 Jun 2020 20:02:25 GMT
ARG DOWNLOAD_OPTIONS=
# Mon, 29 Jun 2020 20:02:33 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Mon, 29 Jun 2020 20:02:34 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jun 2020 20:02:34 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.6 BuildLabel=cl200620200528-0414
# Mon, 29 Jun 2020 20:02:34 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Mon, 29 Jun 2020 20:02:35 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Mon, 29 Jun 2020 20:02:35 GMT
COPY dir:eea9bd687cda20807296939d3f98c70b1d48a11ffe1e23ee8f0c373a62cce55b in /opt/ibm/helpers/ 
# Mon, 29 Jun 2020 20:02:36 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Mon, 29 Jun 2020 20:02:36 GMT
COPY dir:f50ec19c0b3217fa3d6d42c3ce4a254879f817de03e99e13f96ba6b66fb6862e in /licenses/ 
# Mon, 29 Jun 2020 20:02:37 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Mon, 29 Jun 2020 20:02:44 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Mon, 29 Jun 2020 20:02:44 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Mon, 29 Jun 2020 20:02:44 GMT
USER 1001
# Mon, 29 Jun 2020 20:02:44 GMT
EXPOSE 9080 9443
# Mon, 29 Jun 2020 20:02:45 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Mon, 29 Jun 2020 20:02:45 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:f3c26641772baa3348c0cce190edb38690a41f1824570c5c65cc363b42e5a5b5`  
		Last Modified: Sat, 30 May 2020 09:30:29 GMT  
		Size: 25.4 MB (25365846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf76fcee55454304ffbf9e321dda388a7e8de8a3916f854e1e588bc6c19b088`  
		Last Modified: Wed, 17 Jun 2020 01:42:56 GMT  
		Size: 36.2 KB (36165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5173e4f9f1868daa26021e1e701a000b0aadb2b611a487d089e7de4b728a7424`  
		Last Modified: Wed, 17 Jun 2020 01:42:56 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13da9fe451bd0f377d042d4bebef4ffd19163113e3e66dcd718fe187149a0dbd`  
		Last Modified: Wed, 17 Jun 2020 01:42:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8908dfd089a209d6a736f884da9f1560a4986e7f0d7fd9b7b3c6afb25d7824dc`  
		Last Modified: Wed, 17 Jun 2020 03:10:38 GMT  
		Size: 2.7 MB (2672156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540d84d9245cdf2e35ef7090b4becf1b081e7e31c97539e14b9fdf5f39dc3c11`  
		Last Modified: Mon, 29 Jun 2020 19:45:52 GMT  
		Size: 127.6 MB (127601323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d732ccf9b335c5f83d891d623bb780ee8ffdd87edd975ae2b9b1d2796209814`  
		Last Modified: Mon, 29 Jun 2020 20:13:49 GMT  
		Size: 13.8 MB (13764681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d70749ec91a1d354002207c31b3cc9f45f12f882068e23b00f3cdb901ba0f39`  
		Last Modified: Mon, 29 Jun 2020 20:13:48 GMT  
		Size: 691.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce0ff5b631e23edbd0d69dcd46c75de98b6c20013b2061380086e8151ac3e6f5`  
		Last Modified: Mon, 29 Jun 2020 20:13:47 GMT  
		Size: 9.1 KB (9060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365d49180d91dac33d2c6bb5d25b7fd409dd22bca348b7b7060886db90e9c077`  
		Last Modified: Mon, 29 Jun 2020 20:13:47 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1bf9cae86d12af535f55f9f8518e5e1f0e7de0ccf7f66aff51d8bc1b6dd48aa`  
		Last Modified: Mon, 29 Jun 2020 20:13:52 GMT  
		Size: 57.2 KB (57207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768ba578b6b7598554f3ed4961b52c5ed75e169237a7383b2f623b108b0253bc`  
		Last Modified: Mon, 29 Jun 2020 20:13:46 GMT  
		Size: 10.0 KB (10017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffc105b03d90111f83cf73de0f8d699026ca7114ae0f6fdba7d2c322070ac91`  
		Last Modified: Mon, 29 Jun 2020 20:13:47 GMT  
		Size: 5.7 MB (5695988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
