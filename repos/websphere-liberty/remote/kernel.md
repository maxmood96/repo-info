## `websphere-liberty:kernel`

```console
$ docker pull websphere-liberty@sha256:dd0f1b2ca2829b774f3ce2a290ef53224205369a4da47faf56ef2fb37017ba48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `websphere-liberty:kernel` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:b9d1a6cf4cff8952fdc7ca0a8291d546b1a1e1e9f3a0d0bec6fbce312b5dea3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191452364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9dc442b63a6bc457a9fe77b97115f86860e754094b9a1a24468a5334b8ef1d3`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:18:50 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 15 May 2026 21:18:50 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:18:50 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 15 May 2026 21:19:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f848631ac7f7e61aa26d1e648bc7a96e97da64c33cbc4f76627ea3b367c9a085';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='9fad050b730cf070b341e5f7b5353c6cdd0a5a6f2d2b150678bfdff1f94f2637';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c844b329e2161a7d0c5810b30085b5deeec28b911844220cb3b930f860b10884';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 15 May 2026 21:19:33 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 29 May 2026 23:05:46 GMT
USER root
# Fri, 29 May 2026 23:05:46 GMT
ARG VERBOSE=false
# Fri, 29 May 2026 23:05:46 GMT
ARG OPENJ9_SCC=true
# Fri, 29 May 2026 23:05:46 GMT
ARG LIBERTY_VERSION=26.0.0.5
# Fri, 29 May 2026 23:05:46 GMT
ARG LIBERTY_BUILD_LABEL=cl260520260430-1602
# Fri, 29 May 2026 23:05:46 GMT
ARG LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf
# Fri, 29 May 2026 23:05:46 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.5 org.opencontainers.image.revision=cl260520260430-1602 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.5 com.ibm.websphere.liberty.version=26.0.0.5
# Fri, 29 May 2026 23:05:46 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Fri, 29 May 2026 23:05:46 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.5 BuildLabel=cl260520260430-1602
# Fri, 29 May 2026 23:05:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 29 May 2026 23:05:46 GMT
ARG LIBERTY_URL
# Fri, 29 May 2026 23:05:46 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 29 May 2026 23:05:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 May 2026 23:05:59 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 29 May 2026 23:05:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 29 May 2026 23:05:59 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Fri, 29 May 2026 23:05:59 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Fri, 29 May 2026 23:05:59 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Fri, 29 May 2026 23:05:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 29 May 2026 23:06:04 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Fri, 29 May 2026 23:06:04 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 29 May 2026 23:06:04 GMT
USER 1001
# Fri, 29 May 2026 23:06:04 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 29 May 2026 23:06:04 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 29 May 2026 23:06:04 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2745aaec1f27f3ce64535cccd00ad568bf55bbe89df5b402c9d4e75e445ab0`  
		Last Modified: Fri, 15 May 2026 21:19:47 GMT  
		Size: 1.5 MB (1450194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3014eee4fc2ffbbc50d2bff5a7c48962701a29f1d1d64ab5d45495f3ddb8a16c`  
		Last Modified: Fri, 15 May 2026 21:19:51 GMT  
		Size: 136.2 MB (136233781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536b303803fdd23a012bd4a6a1bab2d1af9fe96c3076183b7d5c58cfccc6b197`  
		Last Modified: Fri, 29 May 2026 23:06:13 GMT  
		Size: 113.8 KB (113828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514003ec7696dbe432a3b9126ca001e68ac464e3bb709b922399d2fdfe0f961e`  
		Last Modified: Fri, 29 May 2026 23:06:14 GMT  
		Size: 18.1 MB (18109681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2949cf6466f7e2f5cf40cb34595a45a86221d844bc73fc45eda66e68eb008c`  
		Last Modified: Fri, 29 May 2026 23:06:13 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc317ec13592b3832a553e48b8baa06e39aadede959248a228fe02810573a644`  
		Last Modified: Fri, 29 May 2026 23:06:13 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d45f64528921799b5e9cd0698a034f79cf9b48c356eb53b0954654f862cc3e`  
		Last Modified: Fri, 29 May 2026 23:06:14 GMT  
		Size: 14.2 KB (14189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a7266d33c11adc925acc7447fabaf6c15d43e968143deb93c9d948dc4b0ae9`  
		Last Modified: Fri, 29 May 2026 23:06:14 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6f48051e865aca26e4e8b81de965a031de250f9f5a85fa8c8bfba2aa6cc247`  
		Last Modified: Fri, 29 May 2026 23:06:14 GMT  
		Size: 15.1 KB (15060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc03f62331f5e1ad353a2be66b1b272dc68537715fd0ef2ce084feaa3afe966b`  
		Last Modified: Fri, 29 May 2026 23:06:15 GMT  
		Size: 5.8 MB (5776594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:37712d36be088da339c9f4a1262a30add55b9ed0ab5ece74cd6e575e1cfa2f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2341255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0f5abd82107b9d4b34780863e7efd3c62b44427ab4552ecf5a2b16c5581e35`

```dockerfile
```

-	Layers:
	-	`sha256:84c9f77388042b6393ff06878b648fde7caec3eba665567363b5e8ebc759ba8a`  
		Last Modified: Fri, 29 May 2026 23:06:13 GMT  
		Size: 2.3 MB (2302641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc9630217ef753c6fda9cce8198532f0cb34a34b21f82c3617d3dfecda24e957`  
		Last Modified: Fri, 29 May 2026 23:06:13 GMT  
		Size: 38.6 KB (38614 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:adbaad5bc1b0ee6b5e99e909ae932acff3f542c9d0dbe401f8f13a9e2b9208d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.0 MB (196999994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f39d20035ddb2bc03c509e2dcf5509f7d64925267762f0582fc1a4116ca22a6`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 09 May 2026 04:51:05 GMT
ARG RELEASE
# Sat, 09 May 2026 04:51:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:51:05 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:51:11 GMT
ADD file:bd6823713e9d7c2f4ea7ca1d6d549e2bed56e8ce1fc6f98e14f6eb3a3371ebfa in / 
# Sat, 09 May 2026 04:51:12 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:28:40 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 15 May 2026 21:28:40 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:28:40 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 15 May 2026 21:29:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f848631ac7f7e61aa26d1e648bc7a96e97da64c33cbc4f76627ea3b367c9a085';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='9fad050b730cf070b341e5f7b5353c6cdd0a5a6f2d2b150678bfdff1f94f2637';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c844b329e2161a7d0c5810b30085b5deeec28b911844220cb3b930f860b10884';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 15 May 2026 21:29:20 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 29 May 2026 23:21:46 GMT
USER root
# Fri, 29 May 2026 23:21:46 GMT
ARG VERBOSE=false
# Fri, 29 May 2026 23:21:46 GMT
ARG OPENJ9_SCC=true
# Fri, 29 May 2026 23:21:46 GMT
ARG LIBERTY_VERSION=26.0.0.5
# Fri, 29 May 2026 23:21:46 GMT
ARG LIBERTY_BUILD_LABEL=cl260520260430-1602
# Fri, 29 May 2026 23:21:46 GMT
ARG LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf
# Fri, 29 May 2026 23:21:46 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.5 org.opencontainers.image.revision=cl260520260430-1602 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.5 com.ibm.websphere.liberty.version=26.0.0.5
# Fri, 29 May 2026 23:21:46 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Fri, 29 May 2026 23:21:46 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.5 BuildLabel=cl260520260430-1602
# Fri, 29 May 2026 23:21:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 29 May 2026 23:21:46 GMT
ARG LIBERTY_URL
# Fri, 29 May 2026 23:21:46 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 29 May 2026 23:22:00 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 May 2026 23:22:00 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 29 May 2026 23:22:01 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 29 May 2026 23:22:01 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Fri, 29 May 2026 23:22:02 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Fri, 29 May 2026 23:22:02 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Fri, 29 May 2026 23:22:03 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 29 May 2026 23:22:12 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Fri, 29 May 2026 23:22:12 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 29 May 2026 23:22:12 GMT
USER 1001
# Fri, 29 May 2026 23:22:12 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 29 May 2026 23:22:12 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 29 May 2026 23:22:12 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:6970bf2b5ef1698cb51975b1a652f6511f8fd9f88ae7b247e3ee32591d975e63`  
		Last Modified: Sat, 09 May 2026 05:25:11 GMT  
		Size: 34.6 MB (34646720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1d9502a29e5927b7c6acfcd4d85b9058b023b826aa21b29033ebc1aa0f839a`  
		Last Modified: Fri, 15 May 2026 21:29:48 GMT  
		Size: 1.5 MB (1536350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ea9fcf12bfe40ab2713b4d79b8765e828a093bdce0e8e57c4039e0ba7d83f7`  
		Last Modified: Fri, 15 May 2026 21:29:52 GMT  
		Size: 137.1 MB (137149789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5694362eb8bc0725bceb6ccbd77b34d9059cff07fe497b2d6dd7799d1e8cb28`  
		Last Modified: Fri, 29 May 2026 23:22:31 GMT  
		Size: 118.2 KB (118229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099a6ecb7d26c695cfae266fc3137f6206958ff87de159e898726fb5f984100d`  
		Last Modified: Fri, 29 May 2026 23:22:32 GMT  
		Size: 18.1 MB (18110042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17d2ef544989ded3e892cefa4996c5c26b6dff96275bd7185a2d15882ed7938`  
		Last Modified: Fri, 29 May 2026 23:22:31 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e693268d3ebd3d8185f7f25d2e7dcd29c2ddb0b229cc88aa2ffefdc2552657`  
		Last Modified: Fri, 29 May 2026 23:22:31 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29df268e3fad08535ad6792515947e4da1fea928e988af8bae5997734c85ad5a`  
		Last Modified: Fri, 29 May 2026 23:22:32 GMT  
		Size: 14.2 KB (14189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1098c901e12cc29660d9a728e9b788e421a52b55c9796b44e1385bab6d3ba3f0`  
		Last Modified: Fri, 29 May 2026 23:22:32 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76bb1d9fabfde9867e650c3f9ce5db0e2994148d53148aae7cb6d763cf3f9acb`  
		Last Modified: Fri, 29 May 2026 23:22:32 GMT  
		Size: 15.1 KB (15079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e9256d54056e368cce0bb29b5936d46d5fe2f6fbe74c47ad0cf97e2626167f`  
		Last Modified: Fri, 29 May 2026 23:22:33 GMT  
		Size: 5.4 MB (5407237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:d51361cf0c7b5eb5964805af87421e1b22f302cc7bb93f08912aed44d199d528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2344564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ab0c35224ca52b015084de744233e043977ea9a9908f54eb0c0b67280d0c64`

```dockerfile
```

-	Layers:
	-	`sha256:c100c4c01977e2cdb2f490b1081d76cec0ace6555f5f766ac6b77ab6b267b6e2`  
		Last Modified: Fri, 29 May 2026 23:22:31 GMT  
		Size: 2.3 MB (2305910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e23add2ef5b5d02bb8dc956957d80de240171de8b6a94fba013ed8cb891b4459`  
		Last Modified: Fri, 29 May 2026 23:22:31 GMT  
		Size: 38.7 KB (38654 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:d7f9ef00d8af431c53b56ed564c2fd53ab5099e15e5950c9eb576e16580a9d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 MB (188652644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22321f56e2f183763af7ee6071e4bf3bd29305a2ad8e8f7975f5a02d58fb7327`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 09 May 2026 04:50:49 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:51 GMT
ADD file:17ca3274b34edf79b2d4401a24984fb8dc339a8298f0e3703af025f51b67336b in / 
# Sat, 09 May 2026 04:50:51 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:25:40 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 15 May 2026 21:25:40 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:25:40 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 15 May 2026 21:26:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f848631ac7f7e61aa26d1e648bc7a96e97da64c33cbc4f76627ea3b367c9a085';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='9fad050b730cf070b341e5f7b5353c6cdd0a5a6f2d2b150678bfdff1f94f2637';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c844b329e2161a7d0c5810b30085b5deeec28b911844220cb3b930f860b10884';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 15 May 2026 21:26:26 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 29 May 2026 23:08:03 GMT
USER root
# Fri, 29 May 2026 23:08:03 GMT
ARG VERBOSE=false
# Fri, 29 May 2026 23:08:03 GMT
ARG OPENJ9_SCC=true
# Fri, 29 May 2026 23:08:03 GMT
ARG LIBERTY_VERSION=26.0.0.5
# Fri, 29 May 2026 23:08:03 GMT
ARG LIBERTY_BUILD_LABEL=cl260520260430-1602
# Fri, 29 May 2026 23:08:03 GMT
ARG LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf
# Fri, 29 May 2026 23:08:03 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.5 org.opencontainers.image.revision=cl260520260430-1602 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.5 com.ibm.websphere.liberty.version=26.0.0.5
# Fri, 29 May 2026 23:08:03 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Fri, 29 May 2026 23:08:03 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.5 BuildLabel=cl260520260430-1602
# Fri, 29 May 2026 23:08:03 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 29 May 2026 23:08:03 GMT
ARG LIBERTY_URL
# Fri, 29 May 2026 23:08:03 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 29 May 2026 23:08:15 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 May 2026 23:08:15 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 29 May 2026 23:08:16 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 29 May 2026 23:08:16 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Fri, 29 May 2026 23:08:16 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Fri, 29 May 2026 23:08:16 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Fri, 29 May 2026 23:08:16 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 29 May 2026 23:08:23 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Fri, 29 May 2026 23:08:23 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 29 May 2026 23:08:23 GMT
USER 1001
# Fri, 29 May 2026 23:08:23 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 29 May 2026 23:08:23 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 29 May 2026 23:08:23 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:c8acb84faa73cc102915433858f425bdd6749804de64fd2e27d5f491f005a91b`  
		Last Modified: Sat, 09 May 2026 05:25:25 GMT  
		Size: 28.2 MB (28202305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1931cfb90bc60ae24d6e589e0cba39f54353e12baecae083fef9e1dab4874f`  
		Last Modified: Fri, 15 May 2026 21:27:00 GMT  
		Size: 1.5 MB (1455939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d580608bb6b95870f23bd08c8ab108f7f19dd838c173a89887d6c80bba5b67a`  
		Last Modified: Fri, 15 May 2026 21:27:03 GMT  
		Size: 134.6 MB (134620694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5423b76e371fc537b01276035d620ef86b27028b7f69c3fd0a877c1d853d27`  
		Last Modified: Fri, 29 May 2026 23:08:41 GMT  
		Size: 114.8 KB (114828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe7f7cb14c1facb0ecdd0f9543435882af5c7ffdbc447ecc9358775a517fdb4`  
		Last Modified: Fri, 29 May 2026 23:08:42 GMT  
		Size: 18.1 MB (18109538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5127b12be7535885c66ae46502f89af80052b8cea03f3edb27047946bdc73fc1`  
		Last Modified: Fri, 29 May 2026 23:08:41 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df0a9271c586f289d6d93154aa52361370af41fc75ea63319ae3ccf84177ab9`  
		Last Modified: Fri, 29 May 2026 23:08:41 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b77951f5589526bcd9bc00dfc8dcf0952e0e63f9393d59888cafed1a364addf`  
		Last Modified: Fri, 29 May 2026 23:08:42 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838daa9512050b96bb07b57b10b82ded1467e693fd13768ec8a21f763bf713e9`  
		Last Modified: Fri, 29 May 2026 23:08:42 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71d8ba31d3472f2d18107dd4aa714345f0e576b6960a90f38964b9458ceb4f4`  
		Last Modified: Fri, 29 May 2026 23:08:42 GMT  
		Size: 15.1 KB (15056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afb98e941ce05698b56b8109d41dcafe0666732e02256ca9420f6a08c0f7790`  
		Last Modified: Fri, 29 May 2026 23:08:43 GMT  
		Size: 6.1 MB (6117742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:14a724b29f4b7cd46fb5183d9d18874cf822ea9d0e95cfc678f227522ff6387b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2340001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98334716096a2f9ac33eb2c90891ec5656057cd5ffb5e2b9e2afb96564592ef3`

```dockerfile
```

-	Layers:
	-	`sha256:c58d7e7a55d20a94e44a02cdef938f371884fdfe40a82babde44e1fdf7879dd5`  
		Last Modified: Fri, 29 May 2026 23:08:41 GMT  
		Size: 2.3 MB (2301388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f95e3a74881240c7b54e37a2b9daf7728814da980741e6acb3fe80682fb96808`  
		Last Modified: Fri, 29 May 2026 23:08:41 GMT  
		Size: 38.6 KB (38613 bytes)  
		MIME: application/vnd.in-toto+json
