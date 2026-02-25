## `websphere-liberty:kernel`

```console
$ docker pull websphere-liberty@sha256:fc2b3f6736afa708a33328889dd80c765262d404c7514de57113aa3f6b317b3b
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
$ docker pull websphere-liberty@sha256:4eb3c833be78455eac77d7542bafe36737a5bfb522af60b2fd548964742f753c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.9 MB (190902483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4711330228f547a117b023aa8f227ca9dbf113c4debdc31c18236a2104300d1`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:26:17 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Feb 2026 20:26:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:26:17 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Feb 2026 20:27:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0a965c513bb522004ddb195fbb3cda7124559b8c7c082fc8626b2f45b4ce9a94';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ebf5f90f77e524593cba310d9e73d993bc8d3357af0127ec4627b1ce8236f385';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8353fb367a56fd150bd5b1facb595bde690c9f9a1f3db7db3b7fb240399a6ae9';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Feb 2026 20:27:03 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 24 Feb 2026 23:08:23 GMT
USER root
# Tue, 24 Feb 2026 23:08:23 GMT
ARG VERBOSE=false
# Tue, 24 Feb 2026 23:08:23 GMT
ARG OPENJ9_SCC=true
# Tue, 24 Feb 2026 23:08:23 GMT
ARG LIBERTY_VERSION=26.0.0.2
# Tue, 24 Feb 2026 23:08:23 GMT
ARG LIBERTY_BUILD_LABEL=cl260220260207-1901
# Tue, 24 Feb 2026 23:08:23 GMT
ARG LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25
# Tue, 24 Feb 2026 23:08:23 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.2 org.opencontainers.image.revision=cl260220260207-1901 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.2 com.ibm.websphere.liberty.version=26.0.0.2
# Tue, 24 Feb 2026 23:08:23 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Tue, 24 Feb 2026 23:08:23 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.2 BuildLabel=cl260220260207-1901
# Tue, 24 Feb 2026 23:08:23 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 24 Feb 2026 23:08:23 GMT
ARG LIBERTY_URL
# Tue, 24 Feb 2026 23:08:23 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 24 Feb 2026 23:08:37 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 23:08:37 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 24 Feb 2026 23:08:37 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 24 Feb 2026 23:08:37 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 24 Feb 2026 23:08:37 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 24 Feb 2026 23:08:37 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 24 Feb 2026 23:08:37 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Tue, 24 Feb 2026 23:08:43 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 24 Feb 2026 23:08:43 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Tue, 24 Feb 2026 23:08:43 GMT
USER 1001
# Tue, 24 Feb 2026 23:08:43 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 24 Feb 2026 23:08:43 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 24 Feb 2026 23:08:43 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99bb9bdbc3b9f25a24f639272ca22bc1f61f8baa517fbf46406f73e10607c305`  
		Last Modified: Tue, 17 Feb 2026 20:27:17 GMT  
		Size: 1.5 MB (1450166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a584e976cd450bda63d593acbffc5d4dd42978f12be87073cc9d4b054f8cc85`  
		Last Modified: Tue, 17 Feb 2026 20:27:20 GMT  
		Size: 135.8 MB (135804369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5022f4080d202d1d5712693ed5bfa415b8d44b549e1cdd390eb77d1d1b77f18`  
		Last Modified: Tue, 24 Feb 2026 23:08:52 GMT  
		Size: 113.7 KB (113737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ff196bc7fdb58d8e6aebf68ea1a65f7551ff51dbf916ea49c3b41d94dede6e`  
		Last Modified: Tue, 24 Feb 2026 23:08:53 GMT  
		Size: 18.0 MB (18035710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb095d4fb795a7f229e6d7393dc6560f2f4e3e004d8f69068fd74cc9ad999c01`  
		Last Modified: Tue, 24 Feb 2026 23:08:52 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ef380c808ecc01fe16245875137a143fa9ba674bad2387acd7795424a928ba`  
		Last Modified: Tue, 24 Feb 2026 23:08:52 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533a8747175f4b57c99d2d32a70d9b641fbf1da5e5a0dea697fa7d28c3136ff4`  
		Last Modified: Tue, 24 Feb 2026 23:08:53 GMT  
		Size: 14.1 KB (14119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b8fddead453d39e77892d8a57627823947ab074765e93ebb978da6b845ea63`  
		Last Modified: Tue, 24 Feb 2026 23:08:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f289c86e9c1763ee67151d40888a4a95622220d250676d367052e7fc159fb2`  
		Last Modified: Tue, 24 Feb 2026 23:08:53 GMT  
		Size: 15.0 KB (14984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81be0264b18bff9ef16c5ea5f7fbadbe722ca828d69b62c011762bb104c76ccf`  
		Last Modified: Tue, 24 Feb 2026 23:08:54 GMT  
		Size: 5.9 MB (5929682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:925a43c66dd915c9119555317dc9640ef9e238cc13114f39bb908245cee5732e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2343308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:865b4590ec779da95b9cfd398c506131adf48f5afc08805a379afdb143ab4c11`

```dockerfile
```

-	Layers:
	-	`sha256:8108d2e5f4333477eddbc77d1600757ef772d881b80c184e5df1c337f6f4b56c`  
		Last Modified: Tue, 24 Feb 2026 23:08:52 GMT  
		Size: 2.3 MB (2304328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edb635e3b4c0b57f5d697c1e5f7829ff3595a09e55e33aa4dd9677ec954d50eb`  
		Last Modified: Tue, 24 Feb 2026 23:08:52 GMT  
		Size: 39.0 KB (38980 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:b2d1d2968a295c95e9c37029897f0d5863af3f970b83ca312f54f9d951172dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196403863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16810df8fec218ded6feab7bd7ac06d25162492a27a22f394c646d0055e32bf`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 10 Feb 2026 17:41:33 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:41:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:41:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:41:33 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:41:39 GMT
ADD file:0418bf4995f9b54380cc1e509e3f7d65bb07aed9a367528d0b1084f0a34f3bf3 in / 
# Tue, 10 Feb 2026 17:41:39 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:45:09 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Feb 2026 20:45:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:45:09 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Feb 2026 21:21:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0a965c513bb522004ddb195fbb3cda7124559b8c7c082fc8626b2f45b4ce9a94';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ebf5f90f77e524593cba310d9e73d993bc8d3357af0127ec4627b1ce8236f385';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8353fb367a56fd150bd5b1facb595bde690c9f9a1f3db7db3b7fb240399a6ae9';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Feb 2026 21:21:46 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 17 Feb 2026 23:14:15 GMT
USER root
# Tue, 17 Feb 2026 23:14:15 GMT
ARG VERBOSE=false
# Tue, 17 Feb 2026 23:14:15 GMT
ARG OPENJ9_SCC=true
# Tue, 17 Feb 2026 23:14:15 GMT
ARG LIBERTY_VERSION=26.0.0.1
# Tue, 17 Feb 2026 23:14:15 GMT
ARG LIBERTY_BUILD_LABEL=cl260120260112-1902
# Tue, 17 Feb 2026 23:14:15 GMT
ARG LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8
# Tue, 17 Feb 2026 23:14:15 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.1 org.opencontainers.image.revision=cl260120260112-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.1 com.ibm.websphere.liberty.version=26.0.0.1
# Tue, 17 Feb 2026 23:14:15 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Tue, 17 Feb 2026 23:14:15 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.1 BuildLabel=cl260120260112-1902
# Tue, 17 Feb 2026 23:14:15 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 17 Feb 2026 23:14:15 GMT
ARG LIBERTY_URL
# Tue, 17 Feb 2026 23:14:15 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 17 Feb 2026 23:14:29 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 23:14:29 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 17 Feb 2026 23:14:33 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 17 Feb 2026 23:14:35 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 17 Feb 2026 23:14:37 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 17 Feb 2026 23:14:38 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 17 Feb 2026 23:14:41 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Tue, 17 Feb 2026 23:14:52 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.1 LIBERTY_BUILD_LABEL=cl260120260112-1902 LIBERTY_SHA=060600dd0e7f6e4a3e102a31245b11cf069559e8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 17 Feb 2026 23:14:52 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Tue, 17 Feb 2026 23:14:52 GMT
USER 1001
# Tue, 17 Feb 2026 23:14:52 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 17 Feb 2026 23:14:52 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 17 Feb 2026 23:14:52 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:95401e425d899946469007a0ce4b02622cf84a67cdd684aa25d61d472fffc38f`  
		Last Modified: Tue, 10 Feb 2026 18:13:52 GMT  
		Size: 34.4 MB (34446102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7ba9d1b5a555762e1b63722491095f4d355bdcb4e2da1b884c931a246213b8`  
		Last Modified: Tue, 17 Feb 2026 20:45:40 GMT  
		Size: 1.5 MB (1536160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d44ee8635cbba8a480cc5afe52ee3f84cdc9521d2eecd6e04ec20444d16d0a`  
		Last Modified: Tue, 17 Feb 2026 21:22:20 GMT  
		Size: 136.7 MB (136749855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3facd3fd42e74d52703ba2522c4a8400ddc3724a001b31b2825098acee2e5b4`  
		Last Modified: Tue, 17 Feb 2026 23:15:18 GMT  
		Size: 118.1 KB (118081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf71a3ea6aea86aab09a218f5af15421a2c8be2baebc1b56a08798d8dab3b85`  
		Last Modified: Tue, 17 Feb 2026 23:15:19 GMT  
		Size: 18.0 MB (18039587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1188fd7f2031bf7a891533594a8e322b01ca6f5e4c7f152ec83cb232d32db848`  
		Last Modified: Tue, 17 Feb 2026 23:15:18 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7c9663cc812d8183c9eca22f1fdf2df4b055fb8086c3271c70dfd14aea6cf4`  
		Last Modified: Tue, 17 Feb 2026 23:15:18 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba51e465c9e8802557b35244e1c3cdac0b35566eed8167008f00b5de1126822`  
		Last Modified: Tue, 17 Feb 2026 23:15:19 GMT  
		Size: 14.1 KB (14121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e12b2fb0c2687ac602c054c4015a852d4455d177abfd956a0c305fe0d01ff0`  
		Last Modified: Tue, 17 Feb 2026 23:15:19 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fba444428e45cb50faf4cc2fba6c0e4205a79987cac5c07b914731d8d563da9`  
		Last Modified: Tue, 17 Feb 2026 23:15:19 GMT  
		Size: 15.0 KB (15005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086fe9ee1e49eb0cfadca934df16ae291cb2eaf5a62f17009b3ea901a9435cb5`  
		Last Modified: Tue, 17 Feb 2026 23:15:20 GMT  
		Size: 5.5 MB (5482589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:76c485deb9a0eee282eb8878313de3f7ba7d7a8fd70055c34e2569e64909b27a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2346629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c895d9319350786868b5c3d1491e337b39973fdb6c2fe223e9d22f1b621ea134`

```dockerfile
```

-	Layers:
	-	`sha256:368c0b83e40c1c62202ac6a6f1310d63c83e46e053c6e56435bd8cd910121a41`  
		Last Modified: Tue, 17 Feb 2026 23:15:18 GMT  
		Size: 2.3 MB (2307603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fd1d0b56b75f303b1d81ec10dbad8376506d950be7671f96f8662ffc4eb9f8c`  
		Last Modified: Tue, 17 Feb 2026 23:15:18 GMT  
		Size: 39.0 KB (39026 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:e0e59bbc46248bfb6d820b211e5c9ceb12d56224c1e8b05141f641cce102c57e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187134862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b207e5ce60152ffc6ee7bb149de056491fdaa8e1d28b0cd47be5cc36f1547f4f`
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
# Wed, 25 Feb 2026 01:08:57 GMT
USER root
# Wed, 25 Feb 2026 01:08:57 GMT
ARG VERBOSE=false
# Wed, 25 Feb 2026 01:08:57 GMT
ARG OPENJ9_SCC=true
# Wed, 25 Feb 2026 01:08:57 GMT
ARG LIBERTY_VERSION=26.0.0.2
# Wed, 25 Feb 2026 01:08:57 GMT
ARG LIBERTY_BUILD_LABEL=cl260220260207-1901
# Wed, 25 Feb 2026 01:08:57 GMT
ARG LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25
# Wed, 25 Feb 2026 01:08:57 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.2 org.opencontainers.image.revision=cl260220260207-1901 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.2 com.ibm.websphere.liberty.version=26.0.0.2
# Wed, 25 Feb 2026 01:08:57 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Wed, 25 Feb 2026 01:08:57 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.2 BuildLabel=cl260220260207-1901
# Wed, 25 Feb 2026 01:08:57 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 25 Feb 2026 01:08:57 GMT
ARG LIBERTY_URL
# Wed, 25 Feb 2026 01:08:57 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 25 Feb 2026 01:09:15 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 01:09:15 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 25 Feb 2026 01:09:17 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 25 Feb 2026 01:09:17 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 25 Feb 2026 01:09:18 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 25 Feb 2026 01:09:18 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 25 Feb 2026 01:09:21 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Wed, 25 Feb 2026 01:09:33 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 25 Feb 2026 01:09:33 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 25 Feb 2026 01:09:33 GMT
USER 1001
# Wed, 25 Feb 2026 01:09:33 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 25 Feb 2026 01:09:33 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 25 Feb 2026 01:09:33 GMT
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
	-	`sha256:efd566d1f28f6ab64983b3e36ab1c9996a0a502eea9765f8259bb364af038848`  
		Last Modified: Wed, 25 Feb 2026 01:10:13 GMT  
		Size: 114.8 KB (114773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c945991f658d6b545c372dc9faee443020f050556492cafb82a4bf424e534dcf`  
		Last Modified: Wed, 25 Feb 2026 01:10:13 GMT  
		Size: 18.0 MB (18035600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b49bf6a6ca28586418e06a94a582b4cabd81b4c2b0745e92fe540b691a0fe6`  
		Last Modified: Wed, 25 Feb 2026 01:10:13 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6474cc8ee4ab9e6c94549c967fb9f3f0fd8f7c6754c70ee8cc69a695645717de`  
		Last Modified: Wed, 25 Feb 2026 01:10:12 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04e2bd1d1335a297efedc2bc34676a1f58990c579e8e66de8d1efdac7fedfed`  
		Last Modified: Wed, 25 Feb 2026 01:10:13 GMT  
		Size: 14.1 KB (14122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023e80c10956ef08101f961ddee418b768b7d0ea94e15e3348b3dd240e117a1d`  
		Last Modified: Wed, 25 Feb 2026 01:10:14 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee060d92aee7d3d968ac4f939bd321b1e9beccdcd160e78f5acc1be16e30b03c`  
		Last Modified: Wed, 25 Feb 2026 01:10:14 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb22649ee742f9e37198b5f478811f06b07c5e83146de6e1246f4694017223d7`  
		Last Modified: Wed, 25 Feb 2026 01:10:14 GMT  
		Size: 6.2 MB (6222059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:f7f50b7a523d148748786a545ec2afed10bb49789c6cc38711579907d17ba4b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2342068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c22d7c8bcde3b4a39f5d0daed2a2973314513fe1c372fd48e65237e5a6dcac`

```dockerfile
```

-	Layers:
	-	`sha256:df06bdf0023e718ab288626fd228d4e091d1b0781ea55e56f37a8834146a0ed7`  
		Last Modified: Wed, 25 Feb 2026 01:10:12 GMT  
		Size: 2.3 MB (2303089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e668d6f1896374fb2d0206ae5db753bb12d548a61b54cac5b05fd0ef9768f02`  
		Last Modified: Wed, 25 Feb 2026 01:10:12 GMT  
		Size: 39.0 KB (38979 bytes)  
		MIME: application/vnd.in-toto+json
