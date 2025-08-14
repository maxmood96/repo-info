## `websphere-liberty:latest`

```console
$ docker pull websphere-liberty@sha256:6b2c95bef49e74a7b64c23cc8260d395b9fc273e2260d2d8df774f5a50eb3583
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
$ docker pull websphere-liberty@sha256:f929e0dbb331aa1d81b6769bd1925c6af7708eefcb51f761ea1a67f2d9e02b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.8 MB (570800527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c3189d8da7d52436391f2a0ff869e0096d646fe4417e16af88f88c9db3fe0d4`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 06:32:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Aug 2025 06:32:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_VERSION=8.0.8.50
# Tue, 05 Aug 2025 06:32:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ad3486554724df92b79d08ac15460631e2ef3ff44dabb50a1b8c3a3ad7e645f4';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='55de3054399a593a8561a9a6a8d4ebb3820acd0309da1974a51db184f4ab88f2';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8094b571b52e9a77a693ca7130fa1267187bced19fcb1ba7a20bf33bb30eca41';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 12 Aug 2025 13:27:51 GMT
USER root
# Tue, 12 Aug 2025 13:27:51 GMT
ARG VERBOSE=false
# Tue, 12 Aug 2025 13:27:51 GMT
ARG OPENJ9_SCC=true
# Tue, 12 Aug 2025 13:27:51 GMT
ARG LIBERTY_VERSION=25.0.0.8
# Tue, 12 Aug 2025 13:27:51 GMT
ARG LIBERTY_BUILD_LABEL=cl250420250407-1902
# Tue, 12 Aug 2025 13:27:51 GMT
ARG LIBERTY_SHA=27abac812660d4dba368044ba969b29c27e23f85
# Tue, 12 Aug 2025 13:27:51 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.8 org.opencontainers.image.revision=cl250420250407-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.8 com.ibm.websphere.liberty.version=25.0.0.8
# Tue, 12 Aug 2025 13:27:51 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Tue, 12 Aug 2025 13:27:51 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.8 BuildLabel=cl250420250407-1902
# Tue, 12 Aug 2025 13:27:51 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.8 LIBERTY_BUILD_LABEL=cl250420250407-1902 LIBERTY_SHA=27abac812660d4dba368044ba969b29c27e23f85
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 12 Aug 2025 13:27:51 GMT
ARG LIBERTY_URL
# Tue, 12 Aug 2025 13:27:51 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 12 Aug 2025 13:27:51 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.8 LIBERTY_BUILD_LABEL=cl250420250407-1902 LIBERTY_SHA=27abac812660d4dba368044ba969b29c27e23f85 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 13:27:51 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 12 Aug 2025 13:27:51 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.8 LIBERTY_BUILD_LABEL=cl250420250407-1902 LIBERTY_SHA=27abac812660d4dba368044ba969b29c27e23f85 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 12 Aug 2025 13:27:51 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 12 Aug 2025 13:27:51 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 12 Aug 2025 13:27:51 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 12 Aug 2025 13:27:51 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.8 LIBERTY_BUILD_LABEL=cl250420250407-1902 LIBERTY_SHA=27abac812660d4dba368044ba969b29c27e23f85 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Tue, 12 Aug 2025 13:27:51 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.8 LIBERTY_BUILD_LABEL=cl250420250407-1902 LIBERTY_SHA=27abac812660d4dba368044ba969b29c27e23f85 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 12 Aug 2025 13:27:51 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Tue, 12 Aug 2025 13:27:51 GMT
USER 1001
# Tue, 12 Aug 2025 13:27:51 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 12 Aug 2025 13:27:51 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 12 Aug 2025 13:27:51 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 12 Aug 2025 13:27:51 GMT
ARG VERBOSE=false
# Tue, 12 Aug 2025 13:27:51 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 12 Aug 2025 13:27:51 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Tue, 12 Aug 2025 13:27:51 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Tue, 12 Aug 2025 13:27:51 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f2eec3d528eb5b5110c2bb9812d5a2c27a080f85b313e063387bfdb6166e8e`  
		Last Modified: Tue, 12 Aug 2025 17:26:04 GMT  
		Size: 1.5 MB (1450029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395ad216cec582a4c9420675953629f4cdc5046ba2fecc126a371479369d618a`  
		Last Modified: Tue, 12 Aug 2025 17:59:13 GMT  
		Size: 135.4 MB (135419090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c549e6a10b25ccabf4600c8556b26c87f8f070c425329b3fb50bd81553f70d21`  
		Last Modified: Tue, 12 Aug 2025 20:19:54 GMT  
		Size: 113.7 KB (113697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcaf0d9045b355ddd37ed1fd36623327a68a4ff83353469a5c56d4780554c71`  
		Last Modified: Tue, 12 Aug 2025 20:19:57 GMT  
		Size: 17.7 MB (17650182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7729c40110ec6cb8a7681195ac669366b969ac6a88b728d3d433407acff864`  
		Last Modified: Tue, 12 Aug 2025 20:19:55 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85428187fd6e955fe470aee97918cce7b737ed39751cb15b193d613727f289e`  
		Last Modified: Tue, 12 Aug 2025 20:19:56 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bafb1f475922963bea923e4cfd89de437e309352e93369c0f61f20c23a3acd5`  
		Last Modified: Tue, 12 Aug 2025 20:19:59 GMT  
		Size: 14.3 KB (14283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c0afcd01bbe4fddf3e95d5eabc935d5161e2f9fdad37810b6075049c45d707`  
		Last Modified: Tue, 12 Aug 2025 20:19:59 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c195e4e15bf080e5fc96565f47ec2ec8ea8e82dcbd9411ca8658e17f7746603c`  
		Last Modified: Tue, 12 Aug 2025 20:20:00 GMT  
		Size: 15.1 KB (15110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb03c6fd42d3093d1f7156f56fef499e4322a8d648dd6de338539dc2b21c71bc`  
		Last Modified: Tue, 12 Aug 2025 20:20:01 GMT  
		Size: 5.8 MB (5771747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433f087261648b8a8de7e2ca19dd04fa3105738fb84f3964d328733731ccb60a`  
		Last Modified: Tue, 12 Aug 2025 23:16:51 GMT  
		Size: 364.8 MB (364811146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302d5ad24acd781f63e677ac5dfdb6c848d5b57a2481001255bc83c60f5b5e6c`  
		Last Modified: Tue, 12 Aug 2025 20:40:16 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee1e32293793367888c1547eaf215d684b428337f41b4c7108dba553ea74d4c`  
		Last Modified: Tue, 12 Aug 2025 23:16:44 GMT  
		Size: 16.0 MB (16014959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:latest` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:ad71ecb278e3731ff651d859dead870771ce589ac8448d225ce93338e2dadb71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4376617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3551279e3c15e8be656c72c3e531c26881a880dca9e7bdda7026d5dffcc3148`

```dockerfile
```

-	Layers:
	-	`sha256:982a7a6c31534770df1b1030e7cb89e8fc901e92bab0dbfcd9a90b6d893bbdf2`  
		Last Modified: Tue, 12 Aug 2025 21:22:31 GMT  
		Size: 4.4 MB (4357495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:280f66ff30055dc18ac4030e94932936277466bde66651a5102b7c72996a7545`  
		Last Modified: Tue, 12 Aug 2025 21:22:32 GMT  
		Size: 19.1 KB (19122 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:latest` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:1bc53c86ac704c5916f4c8ebcb14d2ba0776c5bd455dd47674444a65486b6437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.7 MB (573692562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0244c9fa2492eab8d8fe5f9ccfc5799b5c844223b9b2fc4066ff03d8ce818511`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:03 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:06 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Wed, 30 Jul 2025 05:34:06 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 06:32:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Aug 2025 06:32:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_VERSION=8.0.8.50
# Tue, 05 Aug 2025 06:32:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ad3486554724df92b79d08ac15460631e2ef3ff44dabb50a1b8c3a3ad7e645f4';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='55de3054399a593a8561a9a6a8d4ebb3820acd0309da1974a51db184f4ab88f2';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8094b571b52e9a77a693ca7130fa1267187bced19fcb1ba7a20bf33bb30eca41';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 12 Aug 2025 13:27:51 GMT
USER root
# Tue, 12 Aug 2025 13:27:51 GMT
ARG VERBOSE=false
# Tue, 12 Aug 2025 13:27:51 GMT
ARG OPENJ9_SCC=true
# Tue, 12 Aug 2025 13:27:51 GMT
ARG LIBERTY_VERSION=25.0.0.8
# Tue, 12 Aug 2025 13:27:51 GMT
ARG LIBERTY_BUILD_LABEL=cl250420250407-1902
# Tue, 12 Aug 2025 13:27:51 GMT
ARG LIBERTY_SHA=27abac812660d4dba368044ba969b29c27e23f85
# Tue, 12 Aug 2025 13:27:51 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.8 org.opencontainers.image.revision=cl250420250407-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.8 com.ibm.websphere.liberty.version=25.0.0.8
# Tue, 12 Aug 2025 13:27:51 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Tue, 12 Aug 2025 13:27:51 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.8 BuildLabel=cl250420250407-1902
# Tue, 12 Aug 2025 13:27:51 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.8 LIBERTY_BUILD_LABEL=cl250420250407-1902 LIBERTY_SHA=27abac812660d4dba368044ba969b29c27e23f85
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 12 Aug 2025 13:27:51 GMT
ARG LIBERTY_URL
# Tue, 12 Aug 2025 13:27:51 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 12 Aug 2025 13:27:51 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.8 LIBERTY_BUILD_LABEL=cl250420250407-1902 LIBERTY_SHA=27abac812660d4dba368044ba969b29c27e23f85 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 13:27:51 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 12 Aug 2025 13:27:51 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.8 LIBERTY_BUILD_LABEL=cl250420250407-1902 LIBERTY_SHA=27abac812660d4dba368044ba969b29c27e23f85 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 12 Aug 2025 13:27:51 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 12 Aug 2025 13:27:51 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 12 Aug 2025 13:27:51 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 12 Aug 2025 13:27:51 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.8 LIBERTY_BUILD_LABEL=cl250420250407-1902 LIBERTY_SHA=27abac812660d4dba368044ba969b29c27e23f85 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Tue, 12 Aug 2025 13:27:51 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.8 LIBERTY_BUILD_LABEL=cl250420250407-1902 LIBERTY_SHA=27abac812660d4dba368044ba969b29c27e23f85 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 12 Aug 2025 13:27:51 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Tue, 12 Aug 2025 13:27:51 GMT
USER 1001
# Tue, 12 Aug 2025 13:27:51 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 12 Aug 2025 13:27:51 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 12 Aug 2025 13:27:51 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 12 Aug 2025 13:27:51 GMT
ARG VERBOSE=false
# Tue, 12 Aug 2025 13:27:51 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 12 Aug 2025 13:27:51 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Tue, 12 Aug 2025 13:27:51 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Tue, 12 Aug 2025 13:27:51 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2927a1e71e8665a0426e9c87b474fb1e405fba2f397cd65dfa47740d2204a7b`  
		Last Modified: Tue, 12 Aug 2025 18:23:37 GMT  
		Size: 1.5 MB (1536169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38acb531b224a8c9fbff4a5b8df38d3d05236be9b6ece3c83de72a8e11e1997`  
		Last Modified: Tue, 12 Aug 2025 20:18:48 GMT  
		Size: 136.4 MB (136367647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b69df700ac0608e5869f9c8d9658a5ca0b255cbc629fae46a72e0e6242ccd1`  
		Last Modified: Wed, 13 Aug 2025 03:46:02 GMT  
		Size: 118.0 KB (118020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d714d26ab2e31ae1400578a563311e4a9dc52823daa671722bfa06ad4565109f`  
		Last Modified: Wed, 13 Aug 2025 03:46:04 GMT  
		Size: 17.7 MB (17650473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf6cc241dc29cf072cbee7f6bff2cb5765f3b931a2fdec9ae6b307b06148e4e`  
		Last Modified: Wed, 13 Aug 2025 03:46:04 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430ddc73fa98f0a488480828b5d6e9d4f45b412bcf46d53caa0e85a8ed077ebc`  
		Last Modified: Wed, 13 Aug 2025 03:46:02 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4cbd5061b62de9dad39bb5caf869ca0b55c9de5c25ddcb0921a3092d9c259e`  
		Last Modified: Wed, 13 Aug 2025 03:46:04 GMT  
		Size: 14.3 KB (14287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7ef4ca5b3b903da05f2b9ac95e95097a73cc5f43278e022f4819653db5cd56`  
		Last Modified: Wed, 13 Aug 2025 03:46:02 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b3572a5847f666edec8968521bee50ce6bad20aa88cdba178711dca1d05576`  
		Last Modified: Wed, 13 Aug 2025 03:46:02 GMT  
		Size: 15.1 KB (15122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3905a632ed6e32b0bf4268428591f03014ed106646dddedbaf275f71bbf102e8`  
		Last Modified: Wed, 13 Aug 2025 03:46:05 GMT  
		Size: 5.4 MB (5361620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cee0a6b570630c355c74c6e40a61f8f1af12f49f73c076dc9170eeaf1a9c98b`  
		Last Modified: Wed, 13 Aug 2025 19:38:19 GMT  
		Size: 364.8 MB (364812577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0168a720a85158feb07000fdad2351cf598191d879659f1da9f300a845050ba9`  
		Last Modified: Wed, 13 Aug 2025 18:16:29 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcaf9fbc0d0c4dee71b26603815ff548c57894587cd07138407f22c990abba3c`  
		Last Modified: Wed, 13 Aug 2025 18:16:30 GMT  
		Size: 13.4 MB (13370192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:latest` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:c4a7296a786a8b3a8c46f8986491b058bcfac991af5e2efb2163235fd2efe514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4379932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e3bac16ad8a14d4580cc363b067d6af560db82b4969c25368d6bf41bd9ad7f`

```dockerfile
```

-	Layers:
	-	`sha256:e8ff386003a6ff74f2e2fea031c40a7c341f53ebd247f13daaa8702a65a137dd`  
		Last Modified: Wed, 13 Aug 2025 21:21:55 GMT  
		Size: 4.4 MB (4360770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43af7456b2174185f957ac6cc8272fd04954d2c0eddfa97a05a0fe652b03c66b`  
		Last Modified: Wed, 13 Aug 2025 21:21:56 GMT  
		Size: 19.2 KB (19162 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:latest` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:da417a6c09c25dc54d662e966b9d203577016af7cf3f5d6be7d967f9d24a499c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **566.5 MB (566505834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb5c867616d69e6652c3fa6775bbda6ef64db7e3f14d7e3905fcdfb25ee884e`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 30 Jul 2025 05:33:01 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:33:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:33:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:33:01 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:33:02 GMT
ADD file:e0994d65dd44d220b4a55ce1033f7309688125fc54c99056866a92caff4bce78 in / 
# Wed, 30 Jul 2025 05:33:02 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 06:32:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Aug 2025 06:32:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_VERSION=8.0.8.50
# Tue, 05 Aug 2025 06:32:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ad3486554724df92b79d08ac15460631e2ef3ff44dabb50a1b8c3a3ad7e645f4';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='55de3054399a593a8561a9a6a8d4ebb3820acd0309da1974a51db184f4ab88f2';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8094b571b52e9a77a693ca7130fa1267187bced19fcb1ba7a20bf33bb30eca41';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 12 Aug 2025 13:27:51 GMT
USER root
# Tue, 12 Aug 2025 13:27:51 GMT
ARG VERBOSE=false
# Tue, 12 Aug 2025 13:27:51 GMT
ARG OPENJ9_SCC=true
# Tue, 12 Aug 2025 13:27:51 GMT
ARG LIBERTY_VERSION=25.0.0.8
# Tue, 12 Aug 2025 13:27:51 GMT
ARG LIBERTY_BUILD_LABEL=cl250420250407-1902
# Tue, 12 Aug 2025 13:27:51 GMT
ARG LIBERTY_SHA=27abac812660d4dba368044ba969b29c27e23f85
# Tue, 12 Aug 2025 13:27:51 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.8 org.opencontainers.image.revision=cl250420250407-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.8 com.ibm.websphere.liberty.version=25.0.0.8
# Tue, 12 Aug 2025 13:27:51 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Tue, 12 Aug 2025 13:27:51 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.8 BuildLabel=cl250420250407-1902
# Tue, 12 Aug 2025 13:27:51 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.8 LIBERTY_BUILD_LABEL=cl250420250407-1902 LIBERTY_SHA=27abac812660d4dba368044ba969b29c27e23f85
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 12 Aug 2025 13:27:51 GMT
ARG LIBERTY_URL
# Tue, 12 Aug 2025 13:27:51 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 12 Aug 2025 13:27:51 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.8 LIBERTY_BUILD_LABEL=cl250420250407-1902 LIBERTY_SHA=27abac812660d4dba368044ba969b29c27e23f85 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 13:27:51 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 12 Aug 2025 13:27:51 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.8 LIBERTY_BUILD_LABEL=cl250420250407-1902 LIBERTY_SHA=27abac812660d4dba368044ba969b29c27e23f85 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 12 Aug 2025 13:27:51 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 12 Aug 2025 13:27:51 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 12 Aug 2025 13:27:51 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 12 Aug 2025 13:27:51 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.8 LIBERTY_BUILD_LABEL=cl250420250407-1902 LIBERTY_SHA=27abac812660d4dba368044ba969b29c27e23f85 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Tue, 12 Aug 2025 13:27:51 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.8 LIBERTY_BUILD_LABEL=cl250420250407-1902 LIBERTY_SHA=27abac812660d4dba368044ba969b29c27e23f85 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 12 Aug 2025 13:27:51 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Tue, 12 Aug 2025 13:27:51 GMT
USER 1001
# Tue, 12 Aug 2025 13:27:51 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 12 Aug 2025 13:27:51 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 12 Aug 2025 13:27:51 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 12 Aug 2025 13:27:51 GMT
ARG VERBOSE=false
# Tue, 12 Aug 2025 13:27:51 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 12 Aug 2025 13:27:51 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Tue, 12 Aug 2025 13:27:51 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Tue, 12 Aug 2025 13:27:51 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:9c54d9d5bd2c16422a2ac0653717d2ef3d3e03f04fb894713d9682ff2fb1a339`  
		Last Modified: Tue, 12 Aug 2025 17:29:30 GMT  
		Size: 28.0 MB (28003219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1f8a63a7a987fdc761e7e8968ba27654e47f55b299e1e97fe6e51a2c4940f6`  
		Last Modified: Tue, 12 Aug 2025 18:03:01 GMT  
		Size: 1.5 MB (1455837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b282bb47e354fef0c2bcd88a6519010f31c0cb841b9d18790126035171dc4c2`  
		Last Modified: Tue, 12 Aug 2025 21:17:31 GMT  
		Size: 132.3 MB (132290870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9094fefb6297a916e78d73e2f9202ef1be49f4db07459646a47ede3ce902ef29`  
		Last Modified: Tue, 12 Aug 2025 21:39:41 GMT  
		Size: 114.7 KB (114653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5589aee8545f4ea5bc5acb5b76575944edab739e32abf7f5d5f8384068eb4c`  
		Last Modified: Tue, 12 Aug 2025 21:39:44 GMT  
		Size: 17.6 MB (17649915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a7848b30a578f6789ecfdd5201c4ffdf049d7f41f532fb293a2e0b4c5f4557`  
		Last Modified: Tue, 12 Aug 2025 21:39:42 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dbf3b8c5019a9a0c751f6dbff928d5f6f22fea8c7ac6cb7fbc79d9b639a7520`  
		Last Modified: Tue, 12 Aug 2025 21:39:43 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1731607f34fa28fe502c2b92a1f5de95ed5266381e3bf65e892a06933c65369`  
		Last Modified: Tue, 12 Aug 2025 21:39:44 GMT  
		Size: 14.3 KB (14285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51559874b87699f664829bc1e90f4fe4c73919ea33c61f1bd45c9706c1778d03`  
		Last Modified: Tue, 12 Aug 2025 21:39:46 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ca3fcffa79b674d29a38f16b76f60d1f781904b015d1d1628909057319b2a9`  
		Last Modified: Tue, 12 Aug 2025 21:39:46 GMT  
		Size: 15.1 KB (15112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7cb90d737b241f0180763696a547a34477c2b23014cc8b1db1d5a4dc66bd967`  
		Last Modified: Tue, 12 Aug 2025 21:39:47 GMT  
		Size: 5.9 MB (5928096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47597285dfee9f7ff47d31a08fdbd783bc656a3c8a53bd62398f408554b62c0c`  
		Last Modified: Wed, 13 Aug 2025 07:49:23 GMT  
		Size: 364.8 MB (364813632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ae5b38cc38fd7d1108499db5f7c43f413f9e0ed24e3fd020b59dd6874ca056`  
		Last Modified: Wed, 13 Aug 2025 06:22:36 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75438b7c324dd62b11495330d6c2212c947097386b5426d850eea03ae722b943`  
		Last Modified: Wed, 13 Aug 2025 06:22:37 GMT  
		Size: 16.2 MB (16216922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:latest` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:3689caa215147bffc480e46cea4df909d30ad3dcd00f5ce9a8ddf64221a2cf5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4375378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0443f6a616d10a262ceaf9f8abc318ad86779eb95b2b4a87b0b5cfb3b7d635`

```dockerfile
```

-	Layers:
	-	`sha256:607d55a8eea9117f8f0186411ed987ed0a3da9b9a4459f01e11061a580f41591`  
		Last Modified: Wed, 13 Aug 2025 09:20:54 GMT  
		Size: 4.4 MB (4356256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db2adeb6ad32963a54025fa2cadf0a20b7940044c169884c7fb526c6da080db7`  
		Last Modified: Wed, 13 Aug 2025 09:20:55 GMT  
		Size: 19.1 KB (19122 bytes)  
		MIME: application/vnd.in-toto+json
