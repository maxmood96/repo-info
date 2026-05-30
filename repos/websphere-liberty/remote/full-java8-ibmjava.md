## `websphere-liberty:full-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:63bf3f682b4d4002beb25f576555c25cfab21c4ca3e83dd3c4c9b456c04b7050
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `websphere-liberty:full-java8-ibmjava` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:7c5044a2db05870b7b78c3d89d0f6a51a3253db686a291f6feef5fa33f838bea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.1 MB (596123387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c7a475112e87c0768163ed0560f6f7c8732f027a8bec6adee4f4a280dd60e7a`
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
# Sat, 30 May 2026 00:23:43 GMT
ARG VERBOSE=false
# Sat, 30 May 2026 00:23:43 GMT
ARG REPOSITORIES_PROPERTIES=
# Sat, 30 May 2026 00:23:43 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Sat, 30 May 2026 00:23:44 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Sat, 30 May 2026 00:24:06 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
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
	-	`sha256:0ca83255f68cde578615bafa7a8675abbd9d373b20aa44654627cd4ccbb3d826`  
		Last Modified: Sat, 30 May 2026 00:24:42 GMT  
		Size: 389.7 MB (389675905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589a36038c50b37786b0ce30c76919c3235d5564a407b4c291db6e82033e6642`  
		Last Modified: Sat, 30 May 2026 00:24:34 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5aa237372c552361513902f16796f39f8c22e188d13781339af5093c46c646c`  
		Last Modified: Sat, 30 May 2026 00:24:34 GMT  
		Size: 15.0 MB (14994169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:21edf0d9876d92e45ddf09fd4cdb4e4185baf5280b35de73987fbd1378541521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4433343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b113a5720528144aa2d371c5840fe67d4b68524e331b05c7a5f339b358dfff3c`

```dockerfile
```

-	Layers:
	-	`sha256:2b00c1d188a150f880a3aa837bcfab8b9e346d5725ff70c24ad9a2b1bb0de8be`  
		Last Modified: Sat, 30 May 2026 00:24:34 GMT  
		Size: 4.4 MB (4414248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42cf927803e343c1594f3d364e120c97fa1b89e54c42b3bd1bebe6170e7439c6`  
		Last Modified: Sat, 30 May 2026 00:24:34 GMT  
		Size: 19.1 KB (19095 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:c4e1a419f2e491da0bbe880a6ff6b1943ea2a846fc9763b1d309476340017cd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.1 MB (578095340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d69810775a32a72b4255a19b128b36af7cb118bec0faf4c3ffbb61e75b21399e`
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
# Fri, 15 May 2026 22:25:23 GMT
USER root
# Fri, 15 May 2026 22:25:23 GMT
ARG VERBOSE=false
# Fri, 15 May 2026 22:25:23 GMT
ARG OPENJ9_SCC=true
# Fri, 15 May 2026 22:25:23 GMT
ARG LIBERTY_VERSION=26.0.0.3
# Fri, 15 May 2026 22:25:23 GMT
ARG LIBERTY_BUILD_LABEL=cl260320260309-1102
# Fri, 15 May 2026 22:25:23 GMT
ARG LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4
# Fri, 15 May 2026 22:25:23 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.3 org.opencontainers.image.revision=cl260320260309-1102 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.3 com.ibm.websphere.liberty.version=26.0.0.3
# Fri, 15 May 2026 22:25:23 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Fri, 15 May 2026 22:25:23 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.3 BuildLabel=cl260320260309-1102
# Fri, 15 May 2026 22:25:23 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 15 May 2026 22:25:23 GMT
ARG LIBERTY_URL
# Fri, 15 May 2026 22:25:23 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 15 May 2026 22:25:39 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 22:25:39 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 15 May 2026 22:25:41 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 15 May 2026 22:25:41 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Fri, 15 May 2026 22:25:42 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Fri, 15 May 2026 22:25:42 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Fri, 15 May 2026 22:25:43 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 15 May 2026 22:25:55 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Fri, 15 May 2026 22:25:55 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 15 May 2026 22:25:55 GMT
USER 1001
# Fri, 15 May 2026 22:25:55 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 15 May 2026 22:25:55 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 15 May 2026 22:25:55 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Sat, 16 May 2026 00:31:16 GMT
ARG VERBOSE=false
# Sat, 16 May 2026 00:31:16 GMT
ARG REPOSITORIES_PROPERTIES=
# Sat, 16 May 2026 00:31:16 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Sat, 16 May 2026 00:31:17 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Sat, 16 May 2026 00:32:01 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
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
	-	`sha256:5d8d3f9145d14b52ccf8349b79c4445742abe07daf6ac780850652bfef3aed3f`  
		Last Modified: Fri, 15 May 2026 22:26:15 GMT  
		Size: 118.3 KB (118255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c2554794be050f435a1182f3eba85d513356482084bf36c1296c8803b36d9d`  
		Last Modified: Fri, 15 May 2026 22:26:16 GMT  
		Size: 17.8 MB (17835087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79b686eafc66e825c7dba61763e97ebea0e927acc79e673629b28bee055b985`  
		Last Modified: Fri, 15 May 2026 22:26:15 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694524d2e2a246d3d013ee97766fc27f570fa820525c43e13f117e8da3d36d93`  
		Last Modified: Fri, 15 May 2026 22:26:15 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05632fb72e0e885b6625b747b7d271cfb671f81bed8fb126e8071fb15da21de4`  
		Last Modified: Fri, 15 May 2026 22:26:16 GMT  
		Size: 14.1 KB (14115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50e8b636d41f9b87ad5d69edce8355fe4d73b3d017f1850264bf722df283d78`  
		Last Modified: Fri, 15 May 2026 22:26:16 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029f27031917df145038b1d14a89aeba1b0be74402ea3c413a7a2ace7818b32c`  
		Last Modified: Fri, 15 May 2026 22:26:16 GMT  
		Size: 15.0 KB (14996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94e19d920bd582cb3fca3958066b7480c8c276c050f2ca17340b96832d6a2c2`  
		Last Modified: Fri, 15 May 2026 22:26:17 GMT  
		Size: 5.4 MB (5409569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4233d521d0de8e20da514e3eee58483ca2b25b0ddf9062f3301954af6a563745`  
		Last Modified: Sat, 16 May 2026 00:33:01 GMT  
		Size: 368.0 MB (367993561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218eb99d5edb8ec160515b8f8b14ed792dfb32955c36f7119dc74154b3522707`  
		Last Modified: Sat, 16 May 2026 00:32:52 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10a5bb65290aa11b84f058d80ad1c9be6efcaa39dc953c65b19725285d0cceb`  
		Last Modified: Sat, 16 May 2026 00:32:53 GMT  
		Size: 13.4 MB (13373604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:ccc717aa8e2c2b7fe22b04ad6890759fd102f058ea7acceb2891c3199288b565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4385918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8959862a390dd9cd0508d1fedcbfe37d396f39483b4006462441bb30ffa4b964`

```dockerfile
```

-	Layers:
	-	`sha256:1dfba8c1364dba21f1485fe76c5e2383b412bf226ef5b91d4ce3fc0295b5960d`  
		Last Modified: Sat, 16 May 2026 00:32:52 GMT  
		Size: 4.4 MB (4366784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e630f171ce4c2d7cc6f6135b55715e74667c52ef9f7cf6e84d775ba9cf81dbc`  
		Last Modified: Sat, 16 May 2026 00:32:51 GMT  
		Size: 19.1 KB (19134 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:fad249dfe1b376d4b35c8a3cc951b949bbadad153b152c49f78ced4c6b0feedc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.4 MB (593442641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ae629819d06771897efd8f4248e4feccaab0d0ac1dc20e17c4f45a9e463276`
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
# Sat, 30 May 2026 00:21:38 GMT
ARG VERBOSE=false
# Sat, 30 May 2026 00:21:38 GMT
ARG REPOSITORIES_PROPERTIES=
# Sat, 30 May 2026 00:21:38 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Sat, 30 May 2026 00:21:38 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Sat, 30 May 2026 00:22:03 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
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
	-	`sha256:ef84301bfb42a57480adc3f2c0015f12363311d594f14e785bdd0e27203a349a`  
		Last Modified: Sat, 30 May 2026 00:22:56 GMT  
		Size: 389.7 MB (389674931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df313ffba5abe6f4e80a46322c33a11cea7c6e384f2962150a95e7fefbd7a0b3`  
		Last Modified: Sat, 30 May 2026 00:22:49 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46be75ba719fe693c1e30775a6cad4e7c7c7433dc032dd6dffdeb6e357c64211`  
		Last Modified: Sat, 30 May 2026 00:22:49 GMT  
		Size: 15.1 MB (15114120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:5844c1f8f4e4108a55c74eb96dced691985f150d18dc996b83fb539379fc19f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4432089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68c5a6b410538fc0bff505e9994ee1b7da357340b0950a15539677e05a5b62ad`

```dockerfile
```

-	Layers:
	-	`sha256:92235428b634f0b873d2e5f60c161877c1851bdd52f54f65ea28a60857cfa981`  
		Last Modified: Sat, 30 May 2026 00:22:49 GMT  
		Size: 4.4 MB (4412995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2e07a859fe5a6e28fb7e3b2786332eb6ea85afcf8852d200d63284baa4ead03`  
		Last Modified: Sat, 30 May 2026 00:22:49 GMT  
		Size: 19.1 KB (19094 bytes)  
		MIME: application/vnd.in-toto+json
