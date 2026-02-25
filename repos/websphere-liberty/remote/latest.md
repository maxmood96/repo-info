## `websphere-liberty:latest`

```console
$ docker pull websphere-liberty@sha256:f088fe2ec8f70cdcc264e2c3a15633dbea955c780c35fec7174dba5b77f4ce3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `websphere-liberty:latest` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:ae3d03f9448df820c761c61d43790857bb72cb757fb374672631fd19e180357a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.0 MB (574041273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb5bb9ba152c54a2ca4a073389f5837e639be03397ebcbfcfccf05cfce4f2821`
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
# Tue, 24 Feb 2026 23:57:35 GMT
ARG VERBOSE=false
# Tue, 24 Feb 2026 23:57:35 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 24 Feb 2026 23:57:35 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Tue, 24 Feb 2026 23:57:35 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Tue, 24 Feb 2026 23:57:57 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
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
	-	`sha256:d723e722f2a0efda566480ff755150adeefb190bfcde3ee6b19a3c029eb167c6`  
		Last Modified: Tue, 24 Feb 2026 23:58:31 GMT  
		Size: 367.8 MB (367825077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c02e3ea420b2d4661d2f04c73e9f0bf60911fbecbc71a55feb93b83b6cb8857`  
		Last Modified: Tue, 24 Feb 2026 23:58:24 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6d93bbe07daf25acf60788e42c69690b8aee1bee21f0aa605cd3a1e8cd55d4`  
		Last Modified: Tue, 24 Feb 2026 23:58:24 GMT  
		Size: 15.3 MB (15312770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:latest` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:c9a42fc8ab0ec5c3132fa7fb45b893eb09497756832c6b891b6da8c4360b8c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4382598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42033e27d2710e345506973b10f08d2bd4e5510fba3f3816d8c7d30ca3ecc1a8`

```dockerfile
```

-	Layers:
	-	`sha256:f93da6f35d72dde1db0da64e5ef0e741968d15a396842d5ef40463860da985ee`  
		Last Modified: Tue, 24 Feb 2026 23:58:24 GMT  
		Size: 4.4 MB (4363505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c47ed9e7437717c4a2f9ee45e79ceac69d1a412b5d9cab913a27ce274bf772fa`  
		Last Modified: Tue, 24 Feb 2026 23:58:24 GMT  
		Size: 19.1 KB (19093 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:latest` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:176951cd1d38140e79611bfa2061e4d8db854677f2882b82869765e6354ddb3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.5 MB (577474052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366e331ac463cfe8d8ba36fa9d3f53f135cd5632fdb8559fabe581bf914f9b2e`
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
# Wed, 18 Feb 2026 01:26:25 GMT
ARG VERBOSE=false
# Wed, 18 Feb 2026 01:26:25 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 18 Feb 2026 01:26:25 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Wed, 18 Feb 2026 01:26:26 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Wed, 18 Feb 2026 01:27:14 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
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
	-	`sha256:07f4b682349cd56eaeabcf0172778a879710872e12d6b6ac1de31bed68367773`  
		Last Modified: Wed, 18 Feb 2026 01:28:45 GMT  
		Size: 367.8 MB (367758785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e9dc34aca270c184fa7b423cf29e68634be361f8127f6fd19091bf5ce89383`  
		Last Modified: Wed, 18 Feb 2026 01:28:37 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d9043fb09e355bbb502c9cb6bd79b6b98ff032bed8590ced3dea963ee56127`  
		Last Modified: Wed, 18 Feb 2026 01:28:37 GMT  
		Size: 13.3 MB (13310453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:latest` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:4d0f8be262916769e6ed7a3a48aabe799acbe68c6294b7a107ec5d62f1db25e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4385915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61f5d67aed8fc1bca3dd5f7ca167bad49e46383619af838790dc5b8f884c4130`

```dockerfile
```

-	Layers:
	-	`sha256:473acb02f0bebeac57b2eb456e594606c44e1abc4f0baaa8773185aa2ba9b490`  
		Last Modified: Wed, 18 Feb 2026 01:28:37 GMT  
		Size: 4.4 MB (4366780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dee6d83158d025e252586dc151ca5dcf0282e573e354d5e08a0b63499f40f858`  
		Last Modified: Wed, 18 Feb 2026 01:28:36 GMT  
		Size: 19.1 KB (19135 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:latest` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:5fab6943be6e687a79fe4e3442fa0e6235ba8a87abde51d5d06a3ad0a8ba7bd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.5 MB (570474298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8413a38fba5ee02e2d7d9afc655488ab84df0358931becc7dacaa0861728da7`
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
# Wed, 25 Feb 2026 02:30:13 GMT
ARG VERBOSE=false
# Wed, 25 Feb 2026 02:30:13 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 25 Feb 2026 02:30:13 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Wed, 25 Feb 2026 02:30:14 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Wed, 25 Feb 2026 02:30:44 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
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
	-	`sha256:fa5873dcec2ef85b0785b118ac4515086a3ede0b2115a4c0f477493256df59cc`  
		Last Modified: Wed, 25 Feb 2026 02:31:45 GMT  
		Size: 367.8 MB (367826699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e94ddff31861e25a2fc95e05d39875b5529b10fb3739b33f22047084877f2f`  
		Last Modified: Wed, 25 Feb 2026 02:31:39 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5724ea7e7ab45ffcf6898c7b75a0a9fa712072c2de68266f12e395e619d85a`  
		Last Modified: Wed, 25 Feb 2026 02:31:39 GMT  
		Size: 15.5 MB (15511789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:latest` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:f5fb99d45cc15f46761a1187c1997c0be9ac817c1d9c7363fb2a8b04f397c624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f15447f6d4abf9d0f189e015591c7b973f608fd563b8889fde7d942f35141c`

```dockerfile
```

-	Layers:
	-	`sha256:73a17915e330cacbab2dd29fa065962c5f9f95da18147a2cb37d5dafcf13c793`  
		Last Modified: Wed, 25 Feb 2026 02:31:39 GMT  
		Size: 4.4 MB (4362266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f1359a0b05c4072041b602a5f48a77c7588c13183ef45798761e62b1f3a7627`  
		Last Modified: Wed, 25 Feb 2026 02:31:39 GMT  
		Size: 19.1 KB (19094 bytes)  
		MIME: application/vnd.in-toto+json
