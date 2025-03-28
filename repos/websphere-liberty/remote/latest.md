## `websphere-liberty:latest`

```console
$ docker pull websphere-liberty@sha256:339875067096226fd7edfd82ef88007be34cd392aa61f6ccc2a366e2ed15de77
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
$ docker pull websphere-liberty@sha256:3339ff06fee73fc8e7c76ce30395057f023068071bc9acbbbf5d77fd90d4436b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.1 MB (565143561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6311fb0a6a3ed55b023430f70a14ec0a83ff52b9a028c0c73f9114babd49a6f`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 09:27:08 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 14 Feb 2025 09:27:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_VERSION=8.0.8.40
# Fri, 14 Feb 2025 09:27:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='20797bfcc79f9a5db0b83469f9d2dc90179ca8ef69d300d1a9f461f2e0ad49e2';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cd5b5435261af9a88e900b7780b79da4faf4b5b5dc573b3eb1106eec11a5f741';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1c112c7be92f201b0ec010d23d6b590744c3435b0b0f5398e7db1a23119fd590';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='6583c6e0bb859988ac10a2135c4700aaf069181d98b0a6d80414a17a6810e6e1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 25 Mar 2025 15:38:11 GMT
USER root
# Tue, 25 Mar 2025 15:38:11 GMT
ARG VERBOSE=false
# Tue, 25 Mar 2025 15:38:11 GMT
ARG OPENJ9_SCC=true
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_VERSION=25.0.0.3
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
# Tue, 25 Mar 2025 15:38:11 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.3 org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.3 com.ibm.websphere.liberty.version=25.0.0.3
# Tue, 25 Mar 2025 15:38:11 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Tue, 25 Mar 2025 15:38:11 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.3 BuildLabel=cl250320250310-1902
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_URL
# Tue, 25 Mar 2025 15:38:11 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Tue, 25 Mar 2025 15:38:11 GMT
USER 1001
# Tue, 25 Mar 2025 15:38:11 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 25 Mar 2025 15:38:11 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 25 Mar 2025 15:38:11 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 25 Mar 2025 15:38:11 GMT
ARG VERBOSE=false
# Tue, 25 Mar 2025 15:38:11 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216d2e3db6dcd0a26f34986ce22173eb5b9d914a38b00cd3a3a15fc67ce7501b`  
		Last Modified: Tue, 18 Feb 2025 21:29:40 GMT  
		Size: 1.5 MB (1450067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693eda7ffc53cac3deec3030ccd5dc4d3f7d5b12def99b48a6a1cbb7ab072bcf`  
		Last Modified: Tue, 18 Feb 2025 21:29:42 GMT  
		Size: 135.5 MB (135522461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81020f1d9b885fec81bc5dcb11f6c0c104eace4decfd3ec3ad11efdeac823289`  
		Last Modified: Thu, 27 Mar 2025 23:35:13 GMT  
		Size: 113.7 KB (113708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a16b2659ff8c48605603ca153901e645e54cac5ec24bf23e571bee6c9308296`  
		Last Modified: Thu, 27 Mar 2025 23:35:14 GMT  
		Size: 17.9 MB (17937496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf67e00dc9872172a1f96070d4144bcee0f312e651b59f1e3915b5d5b9af7a5`  
		Last Modified: Thu, 27 Mar 2025 23:35:13 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6cc4964937dee6f81f22ad491255dd82690b943b0b25ff021c7d9ff4262209`  
		Last Modified: Thu, 27 Mar 2025 23:35:13 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e58be5dde5741f484f559c772c0ce53582686836f396564bb6054c6f9a90a21`  
		Last Modified: Thu, 27 Mar 2025 23:35:14 GMT  
		Size: 12.2 KB (12233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0518844236e04e2d923217b3ab8f223d43b5ede7aa8063fcb7c937e70aa0ff71`  
		Last Modified: Thu, 27 Mar 2025 23:35:14 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0866708eddab459aaa4f8720ac1501ac96cd34fc10aca94a264fcdd857e2210a`  
		Last Modified: Thu, 27 Mar 2025 23:35:14 GMT  
		Size: 13.0 KB (13042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d75476f73dea1a69fc724bdfa3685645495b736da2524cbd1d630359969478`  
		Last Modified: Thu, 27 Mar 2025 23:35:15 GMT  
		Size: 5.9 MB (5916913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0dd79582fc01a6832bca6267bd5ac07204dd6baa05d2f389be01e9b78cafae`  
		Last Modified: Thu, 27 Mar 2025 23:53:40 GMT  
		Size: 358.7 MB (358662279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb4a6ec79321e765601658e4d249012e594db45b8a22a2a4941ec3bbb37f657`  
		Last Modified: Thu, 27 Mar 2025 23:53:28 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14957c0c5a5d6784734a50656b7e6242ff138039643a955461a2a15ccffcd89d`  
		Last Modified: Thu, 27 Mar 2025 23:53:33 GMT  
		Size: 16.0 MB (15976109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:latest` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:4f666c699eb52850662dd695503afd868aee928e9e640270dcb5c79baf54740f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4213799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f841a70a49fdd24544b5276ee9f23262e9ed2907050ac69e8d0ec5d864f730d0`

```dockerfile
```

-	Layers:
	-	`sha256:6aa9367e85602178c5eeb753b2fe3fe078c01957562b4267d05b8d91af1f7065`  
		Last Modified: Thu, 27 Mar 2025 23:53:30 GMT  
		Size: 4.2 MB (4194727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8f22d53427bb8c36a163a3c73a2dba43d9501a0dbb456b45299e53a9ba5f33a`  
		Last Modified: Thu, 27 Mar 2025 23:53:28 GMT  
		Size: 19.1 KB (19072 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:latest` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:3e88d70489faf7e440f369e4826dd0435dab56c685ef6ac04d8ae36d72647084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.9 MB (567873131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79140ba9a61457af90a55130b4107d74b005343f441da88f9fdd8299af33083`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:49 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:54 GMT
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Sun, 26 Jan 2025 05:31:54 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 09:27:08 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 14 Feb 2025 09:27:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_VERSION=8.0.8.40
# Fri, 14 Feb 2025 09:27:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='20797bfcc79f9a5db0b83469f9d2dc90179ca8ef69d300d1a9f461f2e0ad49e2';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cd5b5435261af9a88e900b7780b79da4faf4b5b5dc573b3eb1106eec11a5f741';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1c112c7be92f201b0ec010d23d6b590744c3435b0b0f5398e7db1a23119fd590';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='6583c6e0bb859988ac10a2135c4700aaf069181d98b0a6d80414a17a6810e6e1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 25 Mar 2025 15:38:11 GMT
USER root
# Tue, 25 Mar 2025 15:38:11 GMT
ARG VERBOSE=false
# Tue, 25 Mar 2025 15:38:11 GMT
ARG OPENJ9_SCC=true
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_VERSION=25.0.0.3
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
# Tue, 25 Mar 2025 15:38:11 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.3 org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.3 com.ibm.websphere.liberty.version=25.0.0.3
# Tue, 25 Mar 2025 15:38:11 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Tue, 25 Mar 2025 15:38:11 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.3 BuildLabel=cl250320250310-1902
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_URL
# Tue, 25 Mar 2025 15:38:11 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Tue, 25 Mar 2025 15:38:11 GMT
USER 1001
# Tue, 25 Mar 2025 15:38:11 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 25 Mar 2025 15:38:11 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 25 Mar 2025 15:38:11 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 25 Mar 2025 15:38:11 GMT
ARG VERBOSE=false
# Tue, 25 Mar 2025 15:38:11 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549562dbb9f45949b79117ad60c4bbdb1ae9a0fd0a32b6119b57bf804e7f1c77`  
		Last Modified: Tue, 04 Feb 2025 08:22:06 GMT  
		Size: 1.5 MB (1536037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5355d1509fcce51f292ca434a3a68692e5ec8e50218c8dc3ed6712bb03d06c09`  
		Last Modified: Tue, 18 Feb 2025 21:29:57 GMT  
		Size: 136.4 MB (136354222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20b230679c162143a5fdf96156a1aa7e69fa04b4669a2c8687f6f94c8a8dfdc`  
		Last Modified: Fri, 28 Mar 2025 00:00:03 GMT  
		Size: 117.9 KB (117911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d519d4252c251f05b9aaa6862a7ce9f34a002b17edda76ff1838d3bede46ed95`  
		Last Modified: Fri, 28 Mar 2025 00:00:04 GMT  
		Size: 18.0 MB (17965185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f11dbf8be1091f22560ace46a291835a66f20a7e2893d0e538462d666c8901`  
		Last Modified: Fri, 28 Mar 2025 00:00:02 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7c79d9a28cb3bd7fc26fe2d81d2518f117348b862d792aeebcf1cb687ee104`  
		Last Modified: Fri, 28 Mar 2025 00:00:06 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546406216e3d05cae0d5f2f896875c51c8c039caee85c2f307795bf20920b722`  
		Last Modified: Fri, 28 Mar 2025 00:00:04 GMT  
		Size: 12.2 KB (12238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f10dbc74eb75c59b395177f1c0ed5a8925175263945074f58d48df61bdd0c04`  
		Last Modified: Fri, 28 Mar 2025 00:00:05 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea8680c028df27ab796e9d84ef600172e5d1504567093dd9451509e29da619d`  
		Last Modified: Fri, 28 Mar 2025 00:00:05 GMT  
		Size: 13.0 KB (13047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcce27b0848f78000219f293b7c97f9321c86f8930abeef71cf986c36a4a191d`  
		Last Modified: Fri, 28 Mar 2025 00:00:06 GMT  
		Size: 5.4 MB (5362862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242873ebba9d56780119c35f67c30b842cdb889c76589128e6b018e99804c728`  
		Last Modified: Fri, 28 Mar 2025 00:26:23 GMT  
		Size: 358.7 MB (358661844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5710bebce364474cf955f1af5473ce0bf3ca5e19900d63861a09290059bbfa26`  
		Last Modified: Fri, 28 Mar 2025 00:25:55 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee78e8e235f8d04a8685d94f334428e603289fe3b3ad4980dc146586bdad1e4d`  
		Last Modified: Fri, 28 Mar 2025 00:25:57 GMT  
		Size: 13.4 MB (13398534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:latest` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:870df767081046252963fe67ae062dae2084ccb647f8057180e3d0bdfa72b735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4217002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5416b75e090a57db2fe20c3d84edc081036d83e262f4a53727fc0b253b090766`

```dockerfile
```

-	Layers:
	-	`sha256:1536db3f51d71cf93b6b6c5d8627bee7c1e4e1d1602dd095f4c447ff2ff7cfda`  
		Last Modified: Fri, 28 Mar 2025 00:25:55 GMT  
		Size: 4.2 MB (4197890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebf32f3df3358faffce093b9b09015b5b6cfd001fc69c013181ff666aa575ac7`  
		Last Modified: Fri, 28 Mar 2025 00:25:54 GMT  
		Size: 19.1 KB (19112 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:latest` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:9a5fbec63501a10bcff6c6f5a5913c5d8704adf390ad76c74bf459a323152523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.4 MB (560363148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87707ba848b7af40f9ec6c6eff9a2d51f24dd493eccb95efe6ce21b7abb5dc44`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:03 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:03 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:05 GMT
ADD file:39a6583c8b71c00e0ea7562cadb2b343caf5c0c274178520c7476e53faed2e3e in / 
# Sun, 26 Jan 2025 05:32:05 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 09:27:08 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 14 Feb 2025 09:27:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_VERSION=8.0.8.40
# Fri, 14 Feb 2025 09:27:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='20797bfcc79f9a5db0b83469f9d2dc90179ca8ef69d300d1a9f461f2e0ad49e2';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cd5b5435261af9a88e900b7780b79da4faf4b5b5dc573b3eb1106eec11a5f741';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1c112c7be92f201b0ec010d23d6b590744c3435b0b0f5398e7db1a23119fd590';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='6583c6e0bb859988ac10a2135c4700aaf069181d98b0a6d80414a17a6810e6e1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 25 Mar 2025 15:38:11 GMT
USER root
# Tue, 25 Mar 2025 15:38:11 GMT
ARG VERBOSE=false
# Tue, 25 Mar 2025 15:38:11 GMT
ARG OPENJ9_SCC=true
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_VERSION=25.0.0.3
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
# Tue, 25 Mar 2025 15:38:11 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.3 org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.3 com.ibm.websphere.liberty.version=25.0.0.3
# Tue, 25 Mar 2025 15:38:11 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Tue, 25 Mar 2025 15:38:11 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.3 BuildLabel=cl250320250310-1902
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_URL
# Tue, 25 Mar 2025 15:38:11 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Tue, 25 Mar 2025 15:38:11 GMT
USER 1001
# Tue, 25 Mar 2025 15:38:11 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 25 Mar 2025 15:38:11 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 25 Mar 2025 15:38:11 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 25 Mar 2025 15:38:11 GMT
ARG VERBOSE=false
# Tue, 25 Mar 2025 15:38:11 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:7ed94a91c4e77c2e320a028b45fcefc9419c4df2b3d6494bf92ab5d08bba4d77`  
		Last Modified: Sun, 26 Jan 2025 07:02:32 GMT  
		Size: 28.0 MB (28000931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f4ed4c83fd203a93b2e2d3afc549f52d4e75a4e9c4ecade96808e6a2fe3ebb`  
		Last Modified: Tue, 18 Feb 2025 21:29:44 GMT  
		Size: 1.5 MB (1455567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb4869d82527216d9f7895bf7380fd529d09d816d9127b4d85ad359511f1e41`  
		Last Modified: Tue, 18 Feb 2025 21:29:46 GMT  
		Size: 132.5 MB (132539572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103a14d800a4e4badb4765f942512babe0c8b235febcbaa0ec244ddc0dd06ac5`  
		Last Modified: Thu, 27 Mar 2025 23:52:28 GMT  
		Size: 114.5 KB (114485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fda637de6efb1582e975677bb67cafc2b1e2e937bc2672afa01ffbe5da85ab5`  
		Last Modified: Thu, 27 Mar 2025 23:52:28 GMT  
		Size: 17.9 MB (17939068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77f97b0131a27c2b9639d8b86afab7937f84bf199e3643b86531fc63ab0e602`  
		Last Modified: Thu, 27 Mar 2025 23:52:27 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f48a4bd3bc3e821e186261a068ba5559b7cbbf8dd67b97011fdd3fbdd0eaa3`  
		Last Modified: Thu, 27 Mar 2025 23:52:27 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a3e58e4e5e7e71dc583c5ff86d389ab0b5b34fda67c1211954d288becf0d5c`  
		Last Modified: Thu, 27 Mar 2025 23:52:28 GMT  
		Size: 12.2 KB (12234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd872b575e481114d48f5a75fbb92d4fc6ee03b4a583775a3c3dc21d1228ca9`  
		Last Modified: Thu, 27 Mar 2025 23:52:28 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384335d038910ddf78b1daf33b44c4e63c5a8c73568f89c27228aaa17078daa7`  
		Last Modified: Thu, 27 Mar 2025 23:52:28 GMT  
		Size: 13.0 KB (13038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e23fa43635081352b00d7fecdf197eb2ae3740e69bdac318716751bdde9c89`  
		Last Modified: Thu, 27 Mar 2025 23:52:29 GMT  
		Size: 6.0 MB (5982782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077a123de82b413282b9ace9dac5263b81f29cd0bb0f01648c2a5fb1f6c816cd`  
		Last Modified: Fri, 28 Mar 2025 00:19:27 GMT  
		Size: 358.7 MB (358662106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74018ee07aff20454491da2fe94989a25f1e0d5cc94db95317d714cc4d57d3c`  
		Last Modified: Fri, 28 Mar 2025 00:19:20 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9b78258c66dbe0fd0205023551ebd08a500ffe20ae290353cb7cc2aed8f847`  
		Last Modified: Fri, 28 Mar 2025 00:19:21 GMT  
		Size: 15.6 MB (15640052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:latest` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:d3ded1fcc6e16d1ab66738b471fb84f672312893e79d4eb364688a15a4c1e54c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc40757ed9755c246ae6dcdd30dad667fe81b6b1fc56625c5308b8536248765`

```dockerfile
```

-	Layers:
	-	`sha256:8695a14bdbd10aa13de8517dcb64feb772a6f29601664d0c7f9d01e8af9d2194`  
		Last Modified: Fri, 28 Mar 2025 00:19:20 GMT  
		Size: 4.2 MB (4193478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d036c53d3dffe37ecbf510ab2477d1051b09eaabf1ed3444e8ac2c21cb0026da`  
		Last Modified: Fri, 28 Mar 2025 00:19:19 GMT  
		Size: 19.1 KB (19071 bytes)  
		MIME: application/vnd.in-toto+json
