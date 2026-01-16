## `websphere-liberty:latest`

```console
$ docker pull websphere-liberty@sha256:f09c1ee9f300d170cea6324eb5d4b233e8a5576162ddc654612df20109ad4ce1
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
$ docker pull websphere-liberty@sha256:7de5abf675eaff7f3f0a7dc9c7946b0ec9bc70ce1145853f30e0f597bb7fdb40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.5 MB (573485264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27f7374c12e15191522a6702b46070ef783a536fcece690b89a7b8a722c075e`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:29:01 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Jan 2026 22:29:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:29:01 GMT
ENV JAVA_VERSION=8.0.8.55
# Thu, 15 Jan 2026 22:29:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a6095b036bda7d4344607de6b91823d7704d2bf8b1c4c4cb4b01aa87e9ac0e1f';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a1d3984e2f6971117f950bcc6ac88ea5e4772e687b41af95ceb569cc47b82c73';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='37d9a6cbdd5ce45605d8b05843770151f857efc1280071bdc293cab4dc967c6d';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Jan 2026 22:29:10 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 16 Jan 2026 01:32:43 GMT
USER root
# Fri, 16 Jan 2026 01:32:43 GMT
ARG VERBOSE=false
# Fri, 16 Jan 2026 01:32:43 GMT
ARG OPENJ9_SCC=true
# Fri, 16 Jan 2026 01:32:43 GMT
ARG LIBERTY_VERSION=25.0.0.12
# Fri, 16 Jan 2026 01:32:43 GMT
ARG LIBERTY_BUILD_LABEL=cl251220251117-0302
# Fri, 16 Jan 2026 01:32:43 GMT
ARG LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840
# Fri, 16 Jan 2026 01:32:43 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.12 org.opencontainers.image.revision=cl251220251117-0302 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.12 com.ibm.websphere.liberty.version=25.0.0.12
# Fri, 16 Jan 2026 01:32:43 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Fri, 16 Jan 2026 01:32:43 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.12 BuildLabel=cl251220251117-0302
# Fri, 16 Jan 2026 01:32:43 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 16 Jan 2026 01:32:43 GMT
ARG LIBERTY_URL
# Fri, 16 Jan 2026 01:32:43 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 16 Jan 2026 01:32:53 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:32:53 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 16 Jan 2026 01:32:54 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 16 Jan 2026 01:32:54 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Fri, 16 Jan 2026 01:32:54 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Fri, 16 Jan 2026 01:32:54 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Fri, 16 Jan 2026 01:32:54 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 16 Jan 2026 01:32:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Fri, 16 Jan 2026 01:32:59 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 16 Jan 2026 01:32:59 GMT
USER 1001
# Fri, 16 Jan 2026 01:32:59 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 16 Jan 2026 01:32:59 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 16 Jan 2026 01:32:59 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 16 Jan 2026 02:38:34 GMT
ARG VERBOSE=false
# Fri, 16 Jan 2026 02:38:34 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 16 Jan 2026 02:38:34 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Fri, 16 Jan 2026 02:38:34 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Fri, 16 Jan 2026 02:38:56 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c4406d5893ae4c70fd8f934cac2641d64f220fc723533ac69c7934710e8a57`  
		Last Modified: Thu, 15 Jan 2026 22:29:31 GMT  
		Size: 1.5 MB (1450130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09f3b9d3ed4e1110e1009a5cf4d6615eb35450e3b3ff1e1b559ef266dd4aac8`  
		Last Modified: Thu, 15 Jan 2026 22:30:20 GMT  
		Size: 135.5 MB (135541122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f44a78ba8451223c0fb75616500bc51fd840d0bb4f79fb9031e12ac00c844f7`  
		Last Modified: Fri, 16 Jan 2026 01:33:17 GMT  
		Size: 113.8 KB (113750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18cd76d2535d2e32fdad6a7e8dcd69592b955c8f1e3c4e5ea6bd92ecf894e1b4`  
		Last Modified: Fri, 16 Jan 2026 01:33:21 GMT  
		Size: 18.0 MB (18022685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca4aa0904091a1f79a36a776e9192823980f4b600aa2f576571b98c76d7d674`  
		Last Modified: Fri, 16 Jan 2026 01:33:17 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21183071b99de5c358387036b751674326a9511cc81577d237aa8aa52367521c`  
		Last Modified: Fri, 16 Jan 2026 01:33:17 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1db386795d6da849a68e7fe7eacf925a7c4e23a0309a246b84b212297d34b7`  
		Last Modified: Fri, 16 Jan 2026 01:33:17 GMT  
		Size: 14.1 KB (14125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b609fc5db0ea3ed6d932ba4cb5d123bf6088e8d0ab12b312b5d4a9c6c937343b`  
		Last Modified: Fri, 16 Jan 2026 01:33:17 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78728a2d8953001dda02e0133e1f585174923311695387da60c45fc2d63c151`  
		Last Modified: Fri, 16 Jan 2026 01:33:17 GMT  
		Size: 15.0 KB (14994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ab22c4d883b379fc9a6aca0d41a499fa6f3b6ec95053f623e2e5eeb4e98386`  
		Last Modified: Fri, 16 Jan 2026 01:33:17 GMT  
		Size: 5.9 MB (5888415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87aa00afe11f7525519f2f0df2a8d3744f0fe0565b34455285b57cb25fee3df8`  
		Last Modified: Fri, 16 Jan 2026 02:39:54 GMT  
		Size: 367.2 MB (367203596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386cdc1b10642253ab33c67ef365a4d6980aed63dc7dc0a9b581b8c9d7a7e974`  
		Last Modified: Fri, 16 Jan 2026 02:39:36 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc6360281d01c756c06eb28472a0cba4bddd251d1b459760ba1166e4c94146c`  
		Last Modified: Fri, 16 Jan 2026 02:39:39 GMT  
		Size: 15.7 MB (15696480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:latest` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:9ec3495d6d55b366314d270df7957ff3f2c2f0d1b368db368ebc26cb4f33a546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b400b989c63f15d04b95ca746f0d33b131829b9396bc4b78930d7c11dff5150`

```dockerfile
```

-	Layers:
	-	`sha256:77c3abf05e53e7dca39bf7610225c2aa8e6d99c284a0dc7e7f71975df0c2f153`  
		Last Modified: Fri, 16 Jan 2026 04:24:07 GMT  
		Size: 4.4 MB (4362159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8722993bde364ec59f37b2760a076142ccc6175835e39b666a2d733bba7a8c4e`  
		Last Modified: Fri, 16 Jan 2026 04:24:08 GMT  
		Size: 19.1 KB (19095 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:latest` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:f2800c4b87a67d14956bc7762aad9b063861318ad8bfd2fe7456bc997c5b7c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.0 MB (576973031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471043c03505850aab251adce13d2cc6b87ec4030f235b9d4d44460aa3103f1a`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 00:09:25 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 14 Nov 2025 00:09:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:09:25 GMT
ENV JAVA_VERSION=8.0.8.55
# Fri, 14 Nov 2025 00:09:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a6095b036bda7d4344607de6b91823d7704d2bf8b1c4c4cb4b01aa87e9ac0e1f';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a1d3984e2f6971117f950bcc6ac88ea5e4772e687b41af95ceb569cc47b82c73';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='37d9a6cbdd5ce45605d8b05843770151f857efc1280071bdc293cab4dc967c6d';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Nov 2025 00:09:38 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 03 Dec 2025 21:58:05 GMT
USER root
# Wed, 03 Dec 2025 21:58:05 GMT
ARG VERBOSE=false
# Wed, 03 Dec 2025 21:58:05 GMT
ARG OPENJ9_SCC=true
# Wed, 03 Dec 2025 21:58:05 GMT
ARG LIBERTY_VERSION=25.0.0.12
# Wed, 03 Dec 2025 21:58:05 GMT
ARG LIBERTY_BUILD_LABEL=cl251220251117-0302
# Wed, 03 Dec 2025 21:58:05 GMT
ARG LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840
# Wed, 03 Dec 2025 21:58:05 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.12 org.opencontainers.image.revision=cl251220251117-0302 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.12 com.ibm.websphere.liberty.version=25.0.0.12
# Wed, 03 Dec 2025 21:58:05 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Wed, 03 Dec 2025 21:58:05 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.12 BuildLabel=cl251220251117-0302
# Wed, 03 Dec 2025 21:58:05 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 03 Dec 2025 21:58:05 GMT
ARG LIBERTY_URL
# Wed, 03 Dec 2025 21:58:05 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 03 Dec 2025 21:58:16 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Dec 2025 21:58:16 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 03 Dec 2025 21:58:17 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 03 Dec 2025 21:58:17 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 03 Dec 2025 21:58:18 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 03 Dec 2025 21:58:18 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 03 Dec 2025 21:58:20 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Wed, 03 Dec 2025 21:58:33 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 03 Dec 2025 21:58:33 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 03 Dec 2025 21:58:33 GMT
USER 1001
# Wed, 03 Dec 2025 21:58:33 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 03 Dec 2025 21:58:33 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 03 Dec 2025 21:58:33 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 03 Dec 2025 22:20:06 GMT
ARG VERBOSE=false
# Wed, 03 Dec 2025 22:20:06 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 03 Dec 2025 22:20:06 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Wed, 03 Dec 2025 22:20:07 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Wed, 03 Dec 2025 22:20:48 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Tue, 13 Jan 2026 01:30:07 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76270b161ad8aaab04f9d34ed9a759cb51f3badfe1e68d38e0d4b16506a51c2a`  
		Last Modified: Fri, 14 Nov 2025 00:10:10 GMT  
		Size: 1.5 MB (1536370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e7e1d3389415400ac0426941c10b503c7973749305c39086324736e8f0f96f`  
		Last Modified: Fri, 14 Nov 2025 00:10:14 GMT  
		Size: 136.5 MB (136486934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3dd2ab3dd4b27e59a87eaa211bb40fd330a2329bf967d77bbba27e0ef3e55b7`  
		Last Modified: Wed, 03 Dec 2025 21:59:08 GMT  
		Size: 118.3 KB (118296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483cef0b6bb991bbff895c67ee29fb7f9ee2e9b1b93cffbfdb2202d3404ea467`  
		Last Modified: Wed, 03 Dec 2025 21:59:09 GMT  
		Size: 18.0 MB (18023161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693403e3bdbe1bddfb8e2f8cbf8563722842e07851736582f906dbfb9aa0f5eb`  
		Last Modified: Wed, 03 Dec 2025 21:59:08 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4f79e4a3a32ff030ed3bc7395f86c0cc088d056cf63de38eeb87eaf36dbaac`  
		Last Modified: Wed, 03 Dec 2025 21:59:08 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b3c48f02aa0f3db42ec68f2937b9cd508996345998f0c3c97c26b230764154`  
		Last Modified: Wed, 03 Dec 2025 21:59:08 GMT  
		Size: 14.1 KB (14125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e983744474505941a44d704b34380f9979ca22f5c4c7e5ccd07070771d0785`  
		Last Modified: Wed, 03 Dec 2025 21:59:08 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76f81a16b2fd1822a7c05388788199e783409dc3e041230105c94f5e223794b`  
		Last Modified: Wed, 03 Dec 2025 21:59:08 GMT  
		Size: 15.0 KB (15014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d451faf7825113a2b0bedf610139a323f6cb59eb5ebee97165f52eb822a35d2`  
		Last Modified: Wed, 03 Dec 2025 21:59:09 GMT  
		Size: 5.5 MB (5454578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f858422c5b877e6602b554f618fbc9e40c231473b04142e23e19eeb86057fa9e`  
		Last Modified: Thu, 04 Dec 2025 11:15:47 GMT  
		Size: 367.2 MB (367202566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48ddef7d5e5e8fec13c0ae94eb152aab8e4a9c14173a1685290e2dac7b71338`  
		Last Modified: Wed, 03 Dec 2025 22:22:17 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b799646a1a7fb85b14f4d5781d69fcbf345587f6b7e2760341ab674090c04da`  
		Last Modified: Wed, 03 Dec 2025 22:22:19 GMT  
		Size: 13.7 MB (13671953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:latest` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:58a5ea9c641ec24673d522112e734febfa4067ebcc7f2dbee0f05dc1fc084b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4384568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:962bff98a25a7b9511aaab3ad4cc2cf3a5781c87048cea08543fd9e08c3bdfe3`

```dockerfile
```

-	Layers:
	-	`sha256:e80e1b18b0f143a5b83017196ee4dea17804a4a7247a1eef957595dbd1a59f1f`  
		Last Modified: Thu, 04 Dec 2025 01:21:32 GMT  
		Size: 4.4 MB (4365434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4df3b5a76edf3296a58af5a89ea618db5f108d73a4ba8a10f748e2df1ecb26c3`  
		Last Modified: Thu, 04 Dec 2025 01:21:35 GMT  
		Size: 19.1 KB (19134 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:latest` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:2d08b13824beddece8650f1b6c9729cced382d5de7314794741ffe3fd6aa8c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.6 MB (569622952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39bc0c9f21598668d51c02efb680ccc01677d6e64e63a6ca22b6ec110e6f1ea1`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 09 Jan 2026 07:05:09 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:05:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:05:11 GMT
ADD file:03078bbac5343c8831dae57f317f9a6ced24a6c8b7192435e81027780f524a3a in / 
# Fri, 09 Jan 2026 07:05:11 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:42 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Jan 2026 22:19:42 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:42 GMT
ENV JAVA_VERSION=8.0.8.55
# Thu, 15 Jan 2026 22:19:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a6095b036bda7d4344607de6b91823d7704d2bf8b1c4c4cb4b01aa87e9ac0e1f';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a1d3984e2f6971117f950bcc6ac88ea5e4772e687b41af95ceb569cc47b82c73';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='37d9a6cbdd5ce45605d8b05843770151f857efc1280071bdc293cab4dc967c6d';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Jan 2026 22:19:48 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Thu, 15 Jan 2026 23:58:09 GMT
USER root
# Thu, 15 Jan 2026 23:58:09 GMT
ARG VERBOSE=false
# Thu, 15 Jan 2026 23:58:09 GMT
ARG OPENJ9_SCC=true
# Thu, 15 Jan 2026 23:58:09 GMT
ARG LIBERTY_VERSION=25.0.0.12
# Thu, 15 Jan 2026 23:58:09 GMT
ARG LIBERTY_BUILD_LABEL=cl251220251117-0302
# Thu, 15 Jan 2026 23:58:09 GMT
ARG LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840
# Thu, 15 Jan 2026 23:58:09 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.12 org.opencontainers.image.revision=cl251220251117-0302 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.12 com.ibm.websphere.liberty.version=25.0.0.12
# Thu, 15 Jan 2026 23:58:09 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Thu, 15 Jan 2026 23:58:09 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.12 BuildLabel=cl251220251117-0302
# Thu, 15 Jan 2026 23:58:09 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 15 Jan 2026 23:58:09 GMT
ARG LIBERTY_URL
# Thu, 15 Jan 2026 23:58:09 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 15 Jan 2026 23:58:28 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:58:28 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 15 Jan 2026 23:58:28 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 15 Jan 2026 23:58:28 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Thu, 15 Jan 2026 23:58:28 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Thu, 15 Jan 2026 23:58:29 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Thu, 15 Jan 2026 23:58:29 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Thu, 15 Jan 2026 23:58:35 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Thu, 15 Jan 2026 23:58:35 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Thu, 15 Jan 2026 23:58:35 GMT
USER 1001
# Thu, 15 Jan 2026 23:58:35 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 15 Jan 2026 23:58:35 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 15 Jan 2026 23:58:35 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 16 Jan 2026 00:28:22 GMT
ARG VERBOSE=false
# Fri, 16 Jan 2026 00:28:22 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 16 Jan 2026 00:28:22 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Fri, 16 Jan 2026 00:28:22 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Fri, 16 Jan 2026 00:28:48 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:a0be7aa393c334078596b27f39dc3946551a30dd1cad58fe06cce6be05b244b2`  
		Last Modified: Thu, 15 Jan 2026 21:43:58 GMT  
		Size: 28.0 MB (28003138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a8baf68ff6ceca7a3109d1906b368df74b25f5077d58fdc8fa7113727f6bef`  
		Last Modified: Thu, 15 Jan 2026 22:20:16 GMT  
		Size: 1.5 MB (1455722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224e385c336aa13d7e4fe0581fadca8003d2d31333648d7b7b8f55934bd12cb6`  
		Last Modified: Thu, 15 Jan 2026 22:20:33 GMT  
		Size: 133.0 MB (132950494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60e988dbe4e1c579dc2a952b1844431482a57c5ed4d66b68fa899120e888bf1`  
		Last Modified: Thu, 15 Jan 2026 23:58:57 GMT  
		Size: 114.6 KB (114589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e398d1a326c7c0ea3cdebc2124237bd31573fc7d4b7be0bc7fdaf1b4bb5be565`  
		Last Modified: Thu, 15 Jan 2026 23:58:58 GMT  
		Size: 18.0 MB (18022354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2e0504274033668291add703708f38ac89eb11dc879d8f0f4c9a52c007238e`  
		Last Modified: Thu, 15 Jan 2026 23:58:57 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b66bcce37b3bcd7f7a7bd40959f7c6f727cbfbc264da85d05e641331eb1fdb8`  
		Last Modified: Thu, 15 Jan 2026 23:58:57 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e251e05710a615e3b3cb53d52adb103e4fb1fea9be3ce8241c95bb293a1e663`  
		Last Modified: Thu, 15 Jan 2026 23:58:57 GMT  
		Size: 14.1 KB (14118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09800dc03435967f136796279a45737f04f4e2fe75564b026bb248d8c7ea88e`  
		Last Modified: Thu, 15 Jan 2026 23:58:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f4ab76ff11a3965de20ff4ad6fb315b151fae1e84a09d7235d982e354ec89d`  
		Last Modified: Thu, 15 Jan 2026 23:58:57 GMT  
		Size: 15.0 KB (14997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542d2ee8df5329cff59de935d6b580af10fd57699abbf905dcacad60b58c531d`  
		Last Modified: Thu, 15 Jan 2026 23:58:57 GMT  
		Size: 6.1 MB (6071443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e29c595ec20f771ce126445264fa83144521d756bc1b507ba4293c0d7d85b14`  
		Last Modified: Fri, 16 Jan 2026 00:31:03 GMT  
		Size: 367.2 MB (367201444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39936ec15d193e907368f2ce05d42316a7b708b719ca80dcc97e736b01c38980`  
		Last Modified: Fri, 16 Jan 2026 00:29:56 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c53da430f079fe6bf10dde0880a5b6576a16ade865c277c96b3ca70aac3fe4d`  
		Last Modified: Fri, 16 Jan 2026 00:29:55 GMT  
		Size: 15.8 MB (15771360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:latest` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:0a71282f5f161cacf4a30977df8c419fc881af20f3e4310ea67b8f45acd12a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1694a99165316578bc932302e385611435f062dc09eb40201f85b3b47a740f05`

```dockerfile
```

-	Layers:
	-	`sha256:9ac1555abfe6872774ab6ea166e85efd9699c81a8adee954849d87ef6fdcbddd`  
		Last Modified: Fri, 16 Jan 2026 01:23:53 GMT  
		Size: 4.4 MB (4360920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19729ef3b98b588aa777734aa93caa671dea2250953fa32d9bd9782a2d4284b2`  
		Last Modified: Fri, 16 Jan 2026 01:23:54 GMT  
		Size: 19.1 KB (19095 bytes)  
		MIME: application/vnd.in-toto+json
