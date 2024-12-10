## `websphere-liberty:latest`

```console
$ docker pull websphere-liberty@sha256:a333cb7f30e1cbba7040165c6f49e86d25698dd7279a738aa7af4e6c8efdfcf2
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
$ docker pull websphere-liberty@sha256:09813c814d110dd7ff6ff083f0636ab257dc4ef3d300dcc0f4398595711d7b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.9 MB (564949648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5096501d3f710541251317bdd5f32be9b30c44c5a22baafeee150e72ddcc8956`
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
# Tue, 03 Dec 2024 20:42:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 03 Dec 2024 20:42:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
ENV JAVA_VERSION=8.0.8.35
# Tue, 03 Dec 2024 20:42:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b1674f3fd30e4dcb3d385291132f551ac8d7344403a5ad960a2d20279739bee3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='057a8c0a079e1cf27b60c6bc03d164be99a94aed6d84025b6659178e51da78ca';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ec722e7ca051a1d708246c568656558c2a630bf9d727c90745bee7a3518cd76d';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='71a55e0ed61840d5a67bd0cb6637df80c114e2aca15b28929763c9296c3eda8d';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 03 Dec 2024 20:42:13 GMT
USER root
# Tue, 03 Dec 2024 20:42:13 GMT
ARG VERBOSE=false
# Tue, 03 Dec 2024 20:42:13 GMT
ARG OPENJ9_SCC=true
# Tue, 03 Dec 2024 20:42:13 GMT
ARG LIBERTY_VERSION=24.0.0.12
# Tue, 03 Dec 2024 20:42:13 GMT
ARG LIBERTY_BUILD_LABEL=cl241220241119-0657
# Tue, 03 Dec 2024 20:42:13 GMT
ARG LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4
# Tue, 03 Dec 2024 20:42:13 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.12 org.opencontainers.image.revision=cl241220241119-0657 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Tue, 03 Dec 2024 20:42:13 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Tue, 03 Dec 2024 20:42:13 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.12 BuildLabel=cl241220241119-0657
# Tue, 03 Dec 2024 20:42:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.12 LIBERTY_BUILD_LABEL=cl241220241119-0657 LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
ARG LIBERTY_URL
# Tue, 03 Dec 2024 20:42:13 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 03 Dec 2024 20:42:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.12 LIBERTY_BUILD_LABEL=cl241220241119-0657 LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 03 Dec 2024 20:42:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.12 LIBERTY_BUILD_LABEL=cl241220241119-0657 LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.12 LIBERTY_BUILD_LABEL=cl241220241119-0657 LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.12 LIBERTY_BUILD_LABEL=cl241220241119-0657 LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Tue, 03 Dec 2024 20:42:13 GMT
USER 1001
# Tue, 03 Dec 2024 20:42:13 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 03 Dec 2024 20:42:13 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 03 Dec 2024 20:42:13 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 03 Dec 2024 20:42:13 GMT
ARG VERBOSE=false
# Tue, 03 Dec 2024 20:42:13 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 03 Dec 2024 20:42:13 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
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
	-	`sha256:83c592812681ab3c4d9502d6fedcf53b9745e55bd54e7bf8bbaded1826ea4b39`  
		Last Modified: Mon, 09 Dec 2024 20:37:58 GMT  
		Size: 113.3 KB (113315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49b2f035f3a78e12019d2b54e89f5d3c5dcf7e7492abc812d1a788a86cddea1`  
		Last Modified: Mon, 09 Dec 2024 20:37:59 GMT  
		Size: 17.4 MB (17435817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544a3990d6fbb23a44504b50a30aa463b5fdd81806902faff73fd651fcdd1a22`  
		Last Modified: Mon, 09 Dec 2024 20:37:58 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf71a857bc6c6829db8e6980ed9544ac65778ea387f2470305d8355995d2e0a7`  
		Last Modified: Mon, 09 Dec 2024 20:37:58 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b996f676c44f0c7b1b1fefc3ca482c443a98d7f507dd2aa93c64a9f5e6afb06`  
		Last Modified: Mon, 09 Dec 2024 20:37:59 GMT  
		Size: 11.8 KB (11837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e3a7915c36a573cc1260db5844e2257479dd309c21d1709ad10c74222483d4`  
		Last Modified: Mon, 09 Dec 2024 20:37:59 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27625f771d469cbdc9139896363a3796f6d052222e3398944a4f8faffcd37ed`  
		Last Modified: Mon, 09 Dec 2024 20:37:59 GMT  
		Size: 12.6 KB (12640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a9fcb3498d05bd82e365dde17b49603ca54415366cac52de200b439c203c07`  
		Last Modified: Mon, 09 Dec 2024 20:38:01 GMT  
		Size: 5.8 MB (5816936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1afac40584e205a895976afd56c79d3232cd6644128219777edca7b91b4f831`  
		Last Modified: Mon, 09 Dec 2024 21:20:19 GMT  
		Size: 359.4 MB (359360955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308531e08a401f28526b39cdc856cedb2f8ea7b5d6e16e63493aeb3f9b9c9444`  
		Last Modified: Mon, 09 Dec 2024 21:20:14 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f17491c18f717d459f0a12354839936655a393f67aae51b0ff07c4100c0ff6a`  
		Last Modified: Mon, 09 Dec 2024 21:20:15 GMT  
		Size: 15.9 MB (15876288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:latest` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:11a37057b38ba52045623e2163455a0c6d384d4e15215f2df207f3f27bde12d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4318166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:602559f8fef17e66a2e01918b5650989c9b19e9af545bcf74f92cf3c52be9d68`

```dockerfile
```

-	Layers:
	-	`sha256:4dc629b5c9ce081e9485a689408aacdf413636ea4a4700108cbb3b163cef157b`  
		Last Modified: Mon, 09 Dec 2024 21:20:14 GMT  
		Size: 4.3 MB (4299094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77522b448faae6f4ab93a91141e70c82712664f88816daa04d5e909b3839ae56`  
		Last Modified: Mon, 09 Dec 2024 21:20:14 GMT  
		Size: 19.1 KB (19072 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:latest` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:d68b86d3844968f3c0c9ebf3de3eb9d9cfd04797ec8a1916bdfa4f5f329d073e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.7 MB (567693254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9526247d812b3ef11bf35a361427ccc627a988bd62a40996312a092c217d7c6`
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
# Tue, 03 Dec 2024 20:42:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 03 Dec 2024 20:42:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
ENV JAVA_VERSION=8.0.8.35
# Tue, 03 Dec 2024 20:42:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b1674f3fd30e4dcb3d385291132f551ac8d7344403a5ad960a2d20279739bee3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='057a8c0a079e1cf27b60c6bc03d164be99a94aed6d84025b6659178e51da78ca';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ec722e7ca051a1d708246c568656558c2a630bf9d727c90745bee7a3518cd76d';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='71a55e0ed61840d5a67bd0cb6637df80c114e2aca15b28929763c9296c3eda8d';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 03 Dec 2024 20:42:13 GMT
USER root
# Tue, 03 Dec 2024 20:42:13 GMT
ARG VERBOSE=false
# Tue, 03 Dec 2024 20:42:13 GMT
ARG OPENJ9_SCC=true
# Tue, 03 Dec 2024 20:42:13 GMT
ARG LIBERTY_VERSION=24.0.0.12
# Tue, 03 Dec 2024 20:42:13 GMT
ARG LIBERTY_BUILD_LABEL=cl241220241119-0657
# Tue, 03 Dec 2024 20:42:13 GMT
ARG LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4
# Tue, 03 Dec 2024 20:42:13 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.12 org.opencontainers.image.revision=cl241220241119-0657 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Tue, 03 Dec 2024 20:42:13 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Tue, 03 Dec 2024 20:42:13 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.12 BuildLabel=cl241220241119-0657
# Tue, 03 Dec 2024 20:42:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.12 LIBERTY_BUILD_LABEL=cl241220241119-0657 LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
ARG LIBERTY_URL
# Tue, 03 Dec 2024 20:42:13 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 03 Dec 2024 20:42:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.12 LIBERTY_BUILD_LABEL=cl241220241119-0657 LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 03 Dec 2024 20:42:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.12 LIBERTY_BUILD_LABEL=cl241220241119-0657 LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.12 LIBERTY_BUILD_LABEL=cl241220241119-0657 LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.12 LIBERTY_BUILD_LABEL=cl241220241119-0657 LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Tue, 03 Dec 2024 20:42:13 GMT
USER 1001
# Tue, 03 Dec 2024 20:42:13 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 03 Dec 2024 20:42:13 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 03 Dec 2024 20:42:13 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 03 Dec 2024 20:42:13 GMT
ARG VERBOSE=false
# Tue, 03 Dec 2024 20:42:13 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 03 Dec 2024 20:42:13 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
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
	-	`sha256:7fec13b2dd1628240a2c343a36acdb81feb1c81b3d913b9abcfcf748681e5ac4`  
		Last Modified: Mon, 09 Dec 2024 23:29:31 GMT  
		Size: 117.8 KB (117848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5134bb0f01062beb3c8828d488836ee577ffd49bd4d313283989df89402f0757`  
		Last Modified: Mon, 09 Dec 2024 23:29:32 GMT  
		Size: 17.4 MB (17436339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c36fc320168a386e59bdc6511f6a4a90c86b442276633f3be3ac5037e2d237`  
		Last Modified: Mon, 09 Dec 2024 23:29:31 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf531ea51069493d46a429fed1c58f8b63ae08c7aacd430dbb391c50c131c20`  
		Last Modified: Mon, 09 Dec 2024 23:29:31 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab27333d45f08e84ba320f9fde13861eea543b154f3c9e7b187d1b2e41465c92`  
		Last Modified: Mon, 09 Dec 2024 23:29:32 GMT  
		Size: 11.8 KB (11834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb304ca54c6ab2819bb89bbc48bfece569f1614d8d396195826bef6df9ac6142`  
		Last Modified: Mon, 09 Dec 2024 23:29:32 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9909eef4161cf808e2bf0c9f8f1543c44efae4e9b99ae5870816524388d55a49`  
		Last Modified: Mon, 09 Dec 2024 23:29:32 GMT  
		Size: 12.6 KB (12647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca886db5fbc3d2153ddb7d0d42fa7306fd90b31fb6df5d61bf440556b263b40e`  
		Last Modified: Mon, 09 Dec 2024 23:29:34 GMT  
		Size: 5.4 MB (5368234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb25755b1a5afe50ed314c4fe14c5360a12068e8b6ac702ca326ce11d65f3c2f`  
		Last Modified: Tue, 10 Dec 2024 00:22:00 GMT  
		Size: 359.4 MB (359361503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f306c091f3272f2e0faa71954f77fb782404164ad1112bcab2d77ddf1c3c5ca`  
		Last Modified: Tue, 10 Dec 2024 00:21:48 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59bb15be5ba623c262b82bdad87c2a78b749c1667774d5d1c77f5000802d37af`  
		Last Modified: Tue, 10 Dec 2024 00:21:49 GMT  
		Size: 13.2 MB (13248469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:latest` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:2912c8145a889c851fee0ebdd462725ac6804acf4117e568bc1bf387a7c68ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4315487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e79c4626512b9c1ad3008f96668c5df48732b5450a1a0eaaad97179fcd25554`

```dockerfile
```

-	Layers:
	-	`sha256:7db221ad1451f17fbfe1b4fec8a7d165ff8579da76b542191fb85855168fdedf`  
		Last Modified: Tue, 10 Dec 2024 00:21:48 GMT  
		Size: 4.3 MB (4296375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:718a6325de8b7a5edb9ef581bdba48b62c73aa8d7ed141c2494f94d534f967b2`  
		Last Modified: Tue, 10 Dec 2024 00:21:47 GMT  
		Size: 19.1 KB (19112 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:latest` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:1418b2ee70164e66f00f78758e41e4081d20c1e37eb94dc4c8fb3fe01ee879ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.8 MB (559842715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb342c9280573c4a9c99cd16ef277aa63dd30dd9f10b10bf6337048f7d46a7a`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 15 Aug 2024 07:06:00 GMT
ARG RELEASE
# Thu, 15 Aug 2024 07:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 15 Aug 2024 07:06:00 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Thu, 15 Aug 2024 07:06:00 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 07:06:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Aug 2024 07:06:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_VERSION=8.0.8.30
# Thu, 15 Aug 2024 07:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='918434b2288854235f141966710e2fe783d52a2956446dc0c6eb2902793bf068';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f84a996f9ad2aee005a670ed57a698bfcf4aff58157ec8fe2540735a87df546d';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='bb57be5b606eb9add4da90e083104979cae9fa37b0a173003c4712fc781af8bf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='e8e00b99cae3277421b8277c843f481f31ee0e2857a67cc19b97460f9136dd9a';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 03 Dec 2024 20:42:13 GMT
USER root
# Tue, 03 Dec 2024 20:42:13 GMT
ARG VERBOSE=false
# Tue, 03 Dec 2024 20:42:13 GMT
ARG OPENJ9_SCC=true
# Tue, 03 Dec 2024 20:42:13 GMT
ARG LIBERTY_VERSION=24.0.0.12
# Tue, 03 Dec 2024 20:42:13 GMT
ARG LIBERTY_BUILD_LABEL=cl241220241119-0657
# Tue, 03 Dec 2024 20:42:13 GMT
ARG LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4
# Tue, 03 Dec 2024 20:42:13 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.12 org.opencontainers.image.revision=cl241220241119-0657 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Tue, 03 Dec 2024 20:42:13 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Tue, 03 Dec 2024 20:42:13 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.12 BuildLabel=cl241220241119-0657
# Tue, 03 Dec 2024 20:42:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.12 LIBERTY_BUILD_LABEL=cl241220241119-0657 LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
ARG LIBERTY_URL
# Tue, 03 Dec 2024 20:42:13 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 03 Dec 2024 20:42:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.12 LIBERTY_BUILD_LABEL=cl241220241119-0657 LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 03 Dec 2024 20:42:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.12 LIBERTY_BUILD_LABEL=cl241220241119-0657 LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.12 LIBERTY_BUILD_LABEL=cl241220241119-0657 LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.12 LIBERTY_BUILD_LABEL=cl241220241119-0657 LIBERTY_SHA=2e27858abf32abb6b6b61caf3a78fafe15472fb4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Tue, 03 Dec 2024 20:42:13 GMT
USER 1001
# Tue, 03 Dec 2024 20:42:13 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 03 Dec 2024 20:42:13 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 03 Dec 2024 20:42:13 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 03 Dec 2024 20:42:13 GMT
ARG VERBOSE=false
# Tue, 03 Dec 2024 20:42:13 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 03 Dec 2024 20:42:13 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Tue, 03 Dec 2024 20:42:13 GMT
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
	-	`sha256:dc820c088a0e7092d35c10e7db527e40828db015630f299fb22a1addd4bd545e`  
		Last Modified: Tue, 17 Sep 2024 02:12:23 GMT  
		Size: 131.9 MB (131936849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a956e6f660bd63c447edb29215422b848ebac951dcbea04e717f09af8b9ced`  
		Last Modified: Tue, 03 Dec 2024 23:07:23 GMT  
		Size: 114.7 KB (114738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7018dd81e9a6077c1d80d479e8077782bbeefda24a9698317af204245c3a0ab`  
		Last Modified: Tue, 03 Dec 2024 23:07:24 GMT  
		Size: 17.4 MB (17436060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e644bce66184f040a0c814b47e73b5fcfe9afa500e96d35e1e1689ef27144860`  
		Last Modified: Tue, 03 Dec 2024 23:07:23 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd626214cd6edad365f2d5a1e6c9c2969b4c22c29c89f6b2138d5f6148b0e3b4`  
		Last Modified: Tue, 03 Dec 2024 23:07:24 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28136784e63dc16842e78c1583fab20d197be16b96deed708e1bcf2a79befd7b`  
		Last Modified: Tue, 03 Dec 2024 23:07:24 GMT  
		Size: 11.8 KB (11841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4406ee56b765876aee60cc66cf9dc99d74538da288c11f280ef7e1b65e36107`  
		Last Modified: Tue, 03 Dec 2024 23:07:24 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e46f49e468f840640163528681a9154328dc61d8679cf2bad61b6043f3addcb`  
		Last Modified: Tue, 03 Dec 2024 23:07:24 GMT  
		Size: 12.6 KB (12643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fb072fe748fe2865aa3c9151c6191cc373d4dafec7369c1caf47f4727a63fc`  
		Last Modified: Tue, 03 Dec 2024 23:07:25 GMT  
		Size: 6.1 MB (6137164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb58a88212f9a5b9607e824f1f7ff8ddf5342c00a8439246ee4852913d6126f7`  
		Last Modified: Tue, 03 Dec 2024 23:40:31 GMT  
		Size: 359.4 MB (359360826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8295d6034c83ad20b0318f21edf5b759da35ca0ab6acd10a544c32adf6a5b3`  
		Last Modified: Tue, 03 Dec 2024 23:40:26 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17bcb9a2f5fc1a43565d664ea0a9504699206497ab1dd4633a5fd83a2dda130`  
		Last Modified: Tue, 03 Dec 2024 23:40:27 GMT  
		Size: 15.4 MB (15385892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:latest` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:a99baa0578aa7d1f26c088d1efdfec30edc669c845561027c1544ababb9536a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4310500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9e33d4b1edbe3e39587aa5e8dfe71773b55eac9d85d628d3810513c947f4d1`

```dockerfile
```

-	Layers:
	-	`sha256:22b340dd5bbb3e945a755d8d9edc3db3f8704551a885c80291f9ea4c67293584`  
		Last Modified: Tue, 03 Dec 2024 23:40:25 GMT  
		Size: 4.3 MB (4291428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5949e8a7146ef8111d39c6387aabc52aa611294c09db30fd3451b638e114c9c9`  
		Last Modified: Tue, 03 Dec 2024 23:40:25 GMT  
		Size: 19.1 KB (19072 bytes)  
		MIME: application/vnd.in-toto+json
