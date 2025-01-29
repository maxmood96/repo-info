## `websphere-liberty:full`

```console
$ docker pull websphere-liberty@sha256:934bd3da6c3308f01f9799bd264123e88cc3e6e31a803c439d26d96c9555a412
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `websphere-liberty:full` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:10cd7601e7cdbad881a41f88ac1929cf2e84a7758a00589af771f929427fe3c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.8 MB (563815997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c0141fe264d8360fde670b125f95ae148c702f6495361322cae6bf7dd1bf00`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 08:06:01 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Mon, 09 Dec 2024 08:06:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 08:06:01 GMT
ENV JAVA_VERSION=8.0.8.35
# Mon, 09 Dec 2024 08:06:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b1674f3fd30e4dcb3d385291132f551ac8d7344403a5ad960a2d20279739bee3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='057a8c0a079e1cf27b60c6bc03d164be99a94aed6d84025b6659178e51da78ca';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ec722e7ca051a1d708246c568656558c2a630bf9d727c90745bee7a3518cd76d';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='71a55e0ed61840d5a67bd0cb6637df80c114e2aca15b28929763c9296c3eda8d';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Mon, 09 Dec 2024 08:06:01 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 28 Jan 2025 17:42:04 GMT
USER root
# Tue, 28 Jan 2025 17:42:04 GMT
ARG VERBOSE=false
# Tue, 28 Jan 2025 17:42:04 GMT
ARG OPENJ9_SCC=true
# Tue, 28 Jan 2025 17:42:04 GMT
ARG LIBERTY_VERSION=25.0.0.1
# Tue, 28 Jan 2025 17:42:04 GMT
ARG LIBERTY_BUILD_LABEL=cl250120250113-0302
# Tue, 28 Jan 2025 17:42:04 GMT
ARG LIBERTY_SHA=2185933b7437ede506552cdd0e11ad3a650c6556
# Tue, 28 Jan 2025 17:42:04 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.1 org.opencontainers.image.revision=cl250120250113-0302 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.1 com.ibm.websphere.liberty.version=25.0.0.1
# Tue, 28 Jan 2025 17:42:04 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Tue, 28 Jan 2025 17:42:04 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.1 BuildLabel=cl250120250113-0302
# Tue, 28 Jan 2025 17:42:04 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.1 LIBERTY_BUILD_LABEL=cl250120250113-0302 LIBERTY_SHA=2185933b7437ede506552cdd0e11ad3a650c6556
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 28 Jan 2025 17:42:04 GMT
ARG LIBERTY_URL
# Tue, 28 Jan 2025 17:42:04 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 28 Jan 2025 17:42:04 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.1 LIBERTY_BUILD_LABEL=cl250120250113-0302 LIBERTY_SHA=2185933b7437ede506552cdd0e11ad3a650c6556 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 17:42:04 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 28 Jan 2025 17:42:04 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.1 LIBERTY_BUILD_LABEL=cl250120250113-0302 LIBERTY_SHA=2185933b7437ede506552cdd0e11ad3a650c6556 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 28 Jan 2025 17:42:04 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 28 Jan 2025 17:42:04 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 28 Jan 2025 17:42:04 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 28 Jan 2025 17:42:04 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.1 LIBERTY_BUILD_LABEL=cl250120250113-0302 LIBERTY_SHA=2185933b7437ede506552cdd0e11ad3a650c6556 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Tue, 28 Jan 2025 17:42:04 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.1 LIBERTY_BUILD_LABEL=cl250120250113-0302 LIBERTY_SHA=2185933b7437ede506552cdd0e11ad3a650c6556 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 28 Jan 2025 17:42:04 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Tue, 28 Jan 2025 17:42:04 GMT
USER 1001
# Tue, 28 Jan 2025 17:42:04 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 28 Jan 2025 17:42:04 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 28 Jan 2025 17:42:04 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 28 Jan 2025 17:42:04 GMT
ARG VERBOSE=false
# Tue, 28 Jan 2025 17:42:04 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 28 Jan 2025 17:42:04 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Tue, 28 Jan 2025 17:42:04 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Tue, 28 Jan 2025 17:42:04 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553391b8eb6633eae13e4ec6a00a98f908bd3400991e6ab26678c47bb0119b26`  
		Last Modified: Mon, 09 Dec 2024 19:28:47 GMT  
		Size: 1.4 MB (1449619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3446c9ab27f9cdb7e154f53a8dc456e4dafb38cf1e4ae2efe1ea0f91297f2f`  
		Last Modified: Mon, 09 Dec 2024 19:28:49 GMT  
		Size: 135.3 MB (135333253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681d981a6c838bf966747889f091f986cbc2b56e88355f045afbd7e59f7341e8`  
		Last Modified: Wed, 29 Jan 2025 00:27:28 GMT  
		Size: 113.3 KB (113315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c93621794cd1f8935337fa2df8cc2be3e1ee611c24d109b23c7fb7bce998cee`  
		Last Modified: Wed, 29 Jan 2025 00:27:29 GMT  
		Size: 17.4 MB (17408141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57ac7fa02ee8c4fed7dffecf18c86f34c06f0fb8ab7841bafaf76242764762a`  
		Last Modified: Wed, 29 Jan 2025 00:27:28 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc92a67335f5f3b43199715f0b54f2820f20c5977031267f143356adc5b6e75`  
		Last Modified: Wed, 29 Jan 2025 00:27:29 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72dcad2f475f63677952edd654152762b7a25d0bb257e5034430c3f3f010e80`  
		Last Modified: Wed, 29 Jan 2025 00:27:29 GMT  
		Size: 11.9 KB (11950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99203747d659aa36331f9e9530c58f90f8aef0416aad8abe7f3825921e62378f`  
		Last Modified: Wed, 29 Jan 2025 00:27:29 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3256b655a27b4cfc9218dd8c8e16298cf52752883c4c4dda3f757050763866cc`  
		Last Modified: Wed, 29 Jan 2025 00:27:29 GMT  
		Size: 12.8 KB (12753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f50d4c37fb926bed6eda44ddbbaae85733cdcbcd4b9e11087e175580c70c45`  
		Last Modified: Wed, 29 Jan 2025 00:27:30 GMT  
		Size: 5.8 MB (5799070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a8ffb5e2beccd90c0aec71fc20516e8e936bc9e5bb388b040c49977225ba6b`  
		Last Modified: Wed, 29 Jan 2025 01:37:46 GMT  
		Size: 358.3 MB (358339735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738810d3bcc9274a34e7c9527e98ba35e823bc85954408567e0ff780ed4c6640`  
		Last Modified: Wed, 29 Jan 2025 01:37:41 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2744c0985ce790f710852afcb8215deae08fec96af3a0cd2fa4e41db56ed17b9`  
		Last Modified: Wed, 29 Jan 2025 01:37:41 GMT  
		Size: 15.8 MB (15809174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:29691693fcd87134b669f7f7de7d8d95b0286b9b6863728d85fd89fd9bf2cca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4207734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:086edfca2a9714e86de56f0f0e46f9bfa3e8a56181168da5c6cb67e957802164`

```dockerfile
```

-	Layers:
	-	`sha256:a50a4b79aab866d3ad9e996873f1f8caf58cd4148ba64bc3c009ac285c2aa175`  
		Last Modified: Wed, 29 Jan 2025 01:37:40 GMT  
		Size: 4.2 MB (4188663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b68baf3a84bf59241796ca1953851441679664d32a81f35d7e6d184a3bc8137`  
		Last Modified: Wed, 29 Jan 2025 01:37:40 GMT  
		Size: 19.1 KB (19071 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:3cbb795360218b19d2561eee7de0a7f3d4dc3fc4e0cba36ce537d811e0b3b1de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **566.7 MB (566692564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa0706ff842b185029593b2514ca73feafa20f9a046394d7b58c5798b3c1ed6`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 08:06:01 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Mon, 09 Dec 2024 08:06:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 08:06:01 GMT
ENV JAVA_VERSION=8.0.8.35
# Mon, 09 Dec 2024 08:06:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b1674f3fd30e4dcb3d385291132f551ac8d7344403a5ad960a2d20279739bee3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='057a8c0a079e1cf27b60c6bc03d164be99a94aed6d84025b6659178e51da78ca';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ec722e7ca051a1d708246c568656558c2a630bf9d727c90745bee7a3518cd76d';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='71a55e0ed61840d5a67bd0cb6637df80c114e2aca15b28929763c9296c3eda8d';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Mon, 09 Dec 2024 08:06:01 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 28 Jan 2025 17:42:04 GMT
USER root
# Tue, 28 Jan 2025 17:42:04 GMT
ARG VERBOSE=false
# Tue, 28 Jan 2025 17:42:04 GMT
ARG OPENJ9_SCC=true
# Tue, 28 Jan 2025 17:42:04 GMT
ARG LIBERTY_VERSION=25.0.0.1
# Tue, 28 Jan 2025 17:42:04 GMT
ARG LIBERTY_BUILD_LABEL=cl250120250113-0302
# Tue, 28 Jan 2025 17:42:04 GMT
ARG LIBERTY_SHA=2185933b7437ede506552cdd0e11ad3a650c6556
# Tue, 28 Jan 2025 17:42:04 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.1 org.opencontainers.image.revision=cl250120250113-0302 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.1 com.ibm.websphere.liberty.version=25.0.0.1
# Tue, 28 Jan 2025 17:42:04 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Tue, 28 Jan 2025 17:42:04 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.1 BuildLabel=cl250120250113-0302
# Tue, 28 Jan 2025 17:42:04 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.1 LIBERTY_BUILD_LABEL=cl250120250113-0302 LIBERTY_SHA=2185933b7437ede506552cdd0e11ad3a650c6556
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 28 Jan 2025 17:42:04 GMT
ARG LIBERTY_URL
# Tue, 28 Jan 2025 17:42:04 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 28 Jan 2025 17:42:04 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.1 LIBERTY_BUILD_LABEL=cl250120250113-0302 LIBERTY_SHA=2185933b7437ede506552cdd0e11ad3a650c6556 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 17:42:04 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 28 Jan 2025 17:42:04 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.1 LIBERTY_BUILD_LABEL=cl250120250113-0302 LIBERTY_SHA=2185933b7437ede506552cdd0e11ad3a650c6556 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 28 Jan 2025 17:42:04 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 28 Jan 2025 17:42:04 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 28 Jan 2025 17:42:04 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 28 Jan 2025 17:42:04 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.1 LIBERTY_BUILD_LABEL=cl250120250113-0302 LIBERTY_SHA=2185933b7437ede506552cdd0e11ad3a650c6556 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Tue, 28 Jan 2025 17:42:04 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.1 LIBERTY_BUILD_LABEL=cl250120250113-0302 LIBERTY_SHA=2185933b7437ede506552cdd0e11ad3a650c6556 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 28 Jan 2025 17:42:04 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Tue, 28 Jan 2025 17:42:04 GMT
USER 1001
# Tue, 28 Jan 2025 17:42:04 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 28 Jan 2025 17:42:04 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 28 Jan 2025 17:42:04 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 28 Jan 2025 17:42:04 GMT
ARG VERBOSE=false
# Tue, 28 Jan 2025 17:42:04 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 28 Jan 2025 17:42:04 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Tue, 28 Jan 2025 17:42:04 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Tue, 28 Jan 2025 17:42:04 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5432b06a5eb0b15c862e467e7550b35e423da42224cc982fc620a3e04b458d07`  
		Last Modified: Tue, 17 Sep 2024 01:31:54 GMT  
		Size: 1.5 MB (1523245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7973e271c24305ae4250a4e1d179e3209a78407b28ac91639b51f9f2ee787ca0`  
		Last Modified: Mon, 09 Dec 2024 19:29:01 GMT  
		Size: 136.2 MB (136161585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c308a0452f793f4cc1cf9a3e9ad3132e49ee358d4ea27ce6d3a24ececad595b`  
		Last Modified: Wed, 29 Jan 2025 01:24:47 GMT  
		Size: 117.9 KB (117877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65af2e137f5b9976497cf12c30094cb33a83a3dd9bed565ace49571599783624`  
		Last Modified: Wed, 29 Jan 2025 01:24:48 GMT  
		Size: 17.4 MB (17408599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37bc38107a9c5009a199af08ab3b5d56a8ed1fe5ecb48c99d7db502f090b706`  
		Last Modified: Wed, 29 Jan 2025 01:24:47 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7d1ad777c96ad564db8d119571fabca9065f5ba10ce455b799ffc23cf41fc4`  
		Last Modified: Wed, 29 Jan 2025 01:24:47 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca81c38183d5367c8b1aa4cc7a20a06a46a0ea80f1f8535249a2d783df05e8e7`  
		Last Modified: Wed, 29 Jan 2025 01:24:48 GMT  
		Size: 12.0 KB (11955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0f9eaa780e75459affcfc3b8f80ea233c19b86859c151218696c7101a1b0ce`  
		Last Modified: Wed, 29 Jan 2025 01:24:48 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134ebb014d1f6dc579d4367125831fb7acfccb2c5eee1859be195aff39235133`  
		Last Modified: Wed, 29 Jan 2025 01:24:48 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6770d974940ae7ffc5b23486935144caa4180b9218e56110e29652ec3ad44e2a`  
		Last Modified: Wed, 29 Jan 2025 01:24:50 GMT  
		Size: 5.4 MB (5357270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78cc222a05719e914071b4ccee0d100ccb287020bede27f0d280e04235c0f11a`  
		Last Modified: Wed, 29 Jan 2025 01:55:43 GMT  
		Size: 358.3 MB (358340398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fa8f4873311c78d62da3c19b16f81c8fffa28bbdae9e516a624718affdeabc`  
		Last Modified: Wed, 29 Jan 2025 01:55:19 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d76e44a71a3820174ccad2e1650a05fb2c543e6d1ab04d53d777b58c267664`  
		Last Modified: Wed, 29 Jan 2025 01:55:19 GMT  
		Size: 13.3 MB (13307317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:84b24df0f00546b5bfc2e1b54d968af6a272fe52dd6eaf4deb35f3bf478384cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4205056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d213c85b29538a9e6ec4408ae272d2c252ac985938d13af19f9cbceb9c0d15f`

```dockerfile
```

-	Layers:
	-	`sha256:d76a0d10a533c1c2e245d3bf0e78c84d2731cb9b89c7ba4c858c06321bc396b9`  
		Last Modified: Wed, 29 Jan 2025 01:55:18 GMT  
		Size: 4.2 MB (4185945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8779426ff6b0eb9907f816922d3d02ecc1e6a55b480b4bfd6642152657ee127`  
		Last Modified: Wed, 29 Jan 2025 01:55:17 GMT  
		Size: 19.1 KB (19111 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:e7e407e066bb022e6ec038a7b0783fdcb8cbb45667060cab47d03599a8dbf8f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.3 MB (559283094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d385ef9498c196b7728de22b3e4e0d24065aa2459beb306d0ac3cd3fb992fd`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:31 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:32 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 11 Sep 2024 16:25:32 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 08:06:01 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Mon, 09 Dec 2024 08:06:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 08:06:01 GMT
ENV JAVA_VERSION=8.0.8.35
# Mon, 09 Dec 2024 08:06:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b1674f3fd30e4dcb3d385291132f551ac8d7344403a5ad960a2d20279739bee3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='057a8c0a079e1cf27b60c6bc03d164be99a94aed6d84025b6659178e51da78ca';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ec722e7ca051a1d708246c568656558c2a630bf9d727c90745bee7a3518cd76d';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='71a55e0ed61840d5a67bd0cb6637df80c114e2aca15b28929763c9296c3eda8d';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Mon, 09 Dec 2024 08:06:01 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 28 Jan 2025 17:42:04 GMT
USER root
# Tue, 28 Jan 2025 17:42:04 GMT
ARG VERBOSE=false
# Tue, 28 Jan 2025 17:42:04 GMT
ARG OPENJ9_SCC=true
# Tue, 28 Jan 2025 17:42:04 GMT
ARG LIBERTY_VERSION=25.0.0.1
# Tue, 28 Jan 2025 17:42:04 GMT
ARG LIBERTY_BUILD_LABEL=cl250120250113-0302
# Tue, 28 Jan 2025 17:42:04 GMT
ARG LIBERTY_SHA=2185933b7437ede506552cdd0e11ad3a650c6556
# Tue, 28 Jan 2025 17:42:04 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.1 org.opencontainers.image.revision=cl250120250113-0302 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.1 com.ibm.websphere.liberty.version=25.0.0.1
# Tue, 28 Jan 2025 17:42:04 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Tue, 28 Jan 2025 17:42:04 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.1 BuildLabel=cl250120250113-0302
# Tue, 28 Jan 2025 17:42:04 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.1 LIBERTY_BUILD_LABEL=cl250120250113-0302 LIBERTY_SHA=2185933b7437ede506552cdd0e11ad3a650c6556
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 28 Jan 2025 17:42:04 GMT
ARG LIBERTY_URL
# Tue, 28 Jan 2025 17:42:04 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 28 Jan 2025 17:42:04 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.1 LIBERTY_BUILD_LABEL=cl250120250113-0302 LIBERTY_SHA=2185933b7437ede506552cdd0e11ad3a650c6556 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 17:42:04 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 28 Jan 2025 17:42:04 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.1 LIBERTY_BUILD_LABEL=cl250120250113-0302 LIBERTY_SHA=2185933b7437ede506552cdd0e11ad3a650c6556 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 28 Jan 2025 17:42:04 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 28 Jan 2025 17:42:04 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 28 Jan 2025 17:42:04 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 28 Jan 2025 17:42:04 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.1 LIBERTY_BUILD_LABEL=cl250120250113-0302 LIBERTY_SHA=2185933b7437ede506552cdd0e11ad3a650c6556 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Tue, 28 Jan 2025 17:42:04 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.1 LIBERTY_BUILD_LABEL=cl250120250113-0302 LIBERTY_SHA=2185933b7437ede506552cdd0e11ad3a650c6556 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 28 Jan 2025 17:42:04 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Tue, 28 Jan 2025 17:42:04 GMT
USER 1001
# Tue, 28 Jan 2025 17:42:04 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 28 Jan 2025 17:42:04 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 28 Jan 2025 17:42:04 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 28 Jan 2025 17:42:04 GMT
ARG VERBOSE=false
# Tue, 28 Jan 2025 17:42:04 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 28 Jan 2025 17:42:04 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Tue, 28 Jan 2025 17:42:04 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Tue, 28 Jan 2025 17:42:04 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6d015aafef1cc8c93af1c71f0f144845de0b5e0e0bbcd3c27bccf671404292`  
		Last Modified: Tue, 17 Sep 2024 02:12:21 GMT  
		Size: 1.4 MB (1441914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b5ee1b4aea2eb53f28f33b78c5d4a81f3ccb0aab0c6564549accefa761168b`  
		Last Modified: Tue, 10 Dec 2024 02:23:34 GMT  
		Size: 132.3 MB (132342244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b6a3162525244bfe558cc6a1d1c2f1c127a26cb86ab53142251e76428cbdcf`  
		Last Modified: Wed, 29 Jan 2025 01:19:20 GMT  
		Size: 114.7 KB (114705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ab545e26e389780c4d89bd192853b3b90643addc64474200b2bb16f8cf97a6`  
		Last Modified: Wed, 29 Jan 2025 01:19:21 GMT  
		Size: 17.4 MB (17408276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1051aee0bc27d1a2fe4db3f4cb53ab27e30910b2498812c0bf6271c4b7f5febd`  
		Last Modified: Wed, 29 Jan 2025 01:19:20 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d7183cb394b7af522fc4d89ecd36e3d2b72d646725c17ea984ff35c000e033`  
		Last Modified: Wed, 29 Jan 2025 01:19:20 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff751f1b8e23928b1a72e00f0d6f78b0184fa222a96feee07fa7fcacb163378e`  
		Last Modified: Wed, 29 Jan 2025 01:19:21 GMT  
		Size: 11.9 KB (11950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0bfecf89a2380c05b488f73bc63ca5ea679ceea1d493e33e253b195f7eaef7`  
		Last Modified: Wed, 29 Jan 2025 01:19:21 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d67369a07c4ea099ce984ddcc02979a46e1cee797a462228cc3ad31217f3468`  
		Last Modified: Wed, 29 Jan 2025 01:19:21 GMT  
		Size: 12.8 KB (12753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0951b17ac3b94eb5737ebecb1d38f1710b1f0d91e4552ed2b602908ab7a135`  
		Last Modified: Wed, 29 Jan 2025 01:19:22 GMT  
		Size: 6.0 MB (5960054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd6fe38a17249906990ec701e4e67a325563c738c5bbfd29db24157b8ea5b58`  
		Last Modified: Wed, 29 Jan 2025 01:46:13 GMT  
		Size: 358.3 MB (358340078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe107aed667e0c6cce912f293b1b5ec955c33f3cf15f494f88002bfb520ac05f`  
		Last Modified: Wed, 29 Jan 2025 01:46:08 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe72f4ff73d57f2037066af739db65e9d2b0bc4a91c331e2cbc7f0e7da254f6`  
		Last Modified: Wed, 29 Jan 2025 01:46:09 GMT  
		Size: 15.6 MB (15646346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:2d9ecbb4ba99bf399bdc2188de066c1a939734d363d4b3de9babeb75ff842a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4200605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae5409a43d5f9ff995389af66cabe30732e4890e861748c2c222fe91cf1f13e`

```dockerfile
```

-	Layers:
	-	`sha256:9a00500bbddbbe8177b2ac8e27cc56441abe573ea6446f17bc6ad6fa09a34462`  
		Last Modified: Wed, 29 Jan 2025 01:46:07 GMT  
		Size: 4.2 MB (4181533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd729b29b5fd9bb9034812c677671a7349fb3536833b4c28f1f42890876c16b3`  
		Last Modified: Wed, 29 Jan 2025 01:46:07 GMT  
		Size: 19.1 KB (19072 bytes)  
		MIME: application/vnd.in-toto+json
