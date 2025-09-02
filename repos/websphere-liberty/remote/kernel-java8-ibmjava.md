## `websphere-liberty:kernel-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:66ad03f08628c687651af1bb51a3626fffe0e733e313c893cb69b09b7cb7c0ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `websphere-liberty:kernel-java8-ibmjava` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:c5f304f626f7cc6dea7ea907b8c03f9342d8e8c985f464354d7f1f3bb1f211fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190031703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:269855bdbd9b149ce0704737a7fc2436fa8ab51e4b61659c6efff713100c9cf9`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 05 Aug 2025 06:32:13 GMT
ARG RELEASE
# Tue, 05 Aug 2025 06:32:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 05 Aug 2025 06:32:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 05 Aug 2025 06:32:13 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 05 Aug 2025 06:32:13 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 05 Aug 2025 06:32:13 GMT
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
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896e0ae2cbfdc6277a7e652adde91b66b71bec100b18f0fb6184ddaeb6c11f9b`  
		Last Modified: Tue, 02 Sep 2025 00:15:48 GMT  
		Size: 1.5 MB (1450053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59155fe51a434ca93afac9f47931138b6f38e2bdc452166db0b9ea0736ea43b2`  
		Last Modified: Tue, 02 Sep 2025 00:16:02 GMT  
		Size: 135.4 MB (135419126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e35e897ddc1f96d97d673455b401feeddcdbc2778c88fddb83cfeb1b98d53e9`  
		Last Modified: Tue, 02 Sep 2025 01:12:48 GMT  
		Size: 113.7 KB (113721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220c5a219e54afd07083e7b34f8a8847726686c95f7ef2faffac98061d48fbf2`  
		Last Modified: Tue, 02 Sep 2025 01:12:49 GMT  
		Size: 17.7 MB (17650187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f23d764d761e0dfecca0d903f66c115fd60bc99fd8902c121760c2181638ca5`  
		Last Modified: Tue, 02 Sep 2025 01:12:47 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dee524417948200b9f7d0cee6acbb948586730b6b091e133d82c9aef7f2a557`  
		Last Modified: Tue, 02 Sep 2025 01:12:47 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825076509fe0eb97d32a1fb21caad3426b7bae00ffe0c5d15be27942b2ed7df2`  
		Last Modified: Tue, 02 Sep 2025 01:12:46 GMT  
		Size: 14.3 KB (14284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22337c9a4deff232b12beabc2f1fd69111002f5511ad2377f0870ecaf52c10b3`  
		Last Modified: Tue, 02 Sep 2025 01:12:45 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b732813c1883b3c086d5bb25f96eef389cd940e649d0c3290f912454215fee0f`  
		Last Modified: Tue, 02 Sep 2025 01:12:45 GMT  
		Size: 15.1 KB (15102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d893a54b3efe162927321664586a66a5ef9fda3721ef3c89b0269a5649b723`  
		Last Modified: Tue, 02 Sep 2025 01:12:48 GMT  
		Size: 5.8 MB (5829945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:46753dcb1dad68ae8b94973e02398257692c1ce606cc70adfa14b351f80ff56a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2342203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34635c67bc94834fa86cb6c5c29069278eef828f0e7eb919d1c126df4d6e576b`

```dockerfile
```

-	Layers:
	-	`sha256:0b50d637c903abf2814630744ab1d4fe15b32f6cf0f8e5fd2e5855bfbb91ac03`  
		Last Modified: Tue, 02 Sep 2025 03:22:37 GMT  
		Size: 2.3 MB (2303754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5536fd9735c0d9e77353e4015be87c64c7e6026fa60d28dcee20a7b967a7487c`  
		Last Modified: Tue, 02 Sep 2025 03:22:38 GMT  
		Size: 38.4 KB (38449 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:dae0ff04f7f82fcdc79b830fc1ac45dbc68117629b1679d0873f508f6c4dd5d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195529988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27fee49a09ac7a4f1bbc5a8c5322f0aebf55df35e7c9eab23cc52f8b24c2cde4`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 05 Aug 2025 06:32:13 GMT
ARG RELEASE
# Tue, 05 Aug 2025 06:32:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 05 Aug 2025 06:32:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 05 Aug 2025 06:32:13 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 05 Aug 2025 06:32:13 GMT
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Tue, 05 Aug 2025 06:32:13 GMT
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
```

-	Layers:
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c192fa06531347041f063475dcc6b4d9821e21d789e42dbdb74912b07cb28d9`  
		Last Modified: Tue, 02 Sep 2025 01:05:09 GMT  
		Size: 1.5 MB (1536215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fdac6df39533400b0abc5b1686e398d4afff32994f3acae7c5f12a79cdf9cf`  
		Last Modified: Tue, 02 Sep 2025 01:19:48 GMT  
		Size: 136.4 MB (136367659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b02dffa1809f67ef7a116b287a259d660f3f2ac6eedda6ef2cc0c5e080a49b`  
		Last Modified: Tue, 02 Sep 2025 07:27:53 GMT  
		Size: 118.1 KB (118074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9115180ac15ea2777d2c7917eca32f880f5e4642609ed8c4785b21964fb2baaf`  
		Last Modified: Tue, 02 Sep 2025 07:27:55 GMT  
		Size: 17.7 MB (17650515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa62ff0abae97f05cd7bc384a2d77ff7ac961f6cb7e7f78663fa35c07e03436`  
		Last Modified: Tue, 02 Sep 2025 07:27:54 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49a771e2d42440a05c613d97b6dfc09c5e86f0614d29acbdda424cb7730c4fd`  
		Last Modified: Tue, 02 Sep 2025 07:27:54 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c9bb99582388b90c3a34119e414b214e27d105a49f3e92311967b795bf2cc2`  
		Last Modified: Tue, 02 Sep 2025 07:27:54 GMT  
		Size: 14.3 KB (14287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94777123e394bc2e65b7ebb5288bd37babcb49980253d3bb66f84f4a80a6774`  
		Last Modified: Tue, 02 Sep 2025 07:27:54 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec06fa8cc80fcc101b30481ce61146985e4f5b58eb667ba13e4dfb4e254f5a51`  
		Last Modified: Tue, 02 Sep 2025 07:27:54 GMT  
		Size: 15.1 KB (15117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0af0c966fb81d0110815b0bd0b492dd32e271a6a0d7682672bab6d630c19d4`  
		Last Modified: Tue, 02 Sep 2025 07:27:55 GMT  
		Size: 5.4 MB (5382537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:ec7eae709b0251a96907b56fa2c8def9d1f5284ecc5b28d66abbada8d7689a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2345524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa43fa22b4db2d3da534b019d59c566a67666c39a8a29bd9f2c8e0b26ad41ad9`

```dockerfile
```

-	Layers:
	-	`sha256:a3a42ceb4f145d70eaf9662b75d5948b31e0e6f32ce44298180b628891bc18c4`  
		Last Modified: Tue, 02 Sep 2025 09:21:37 GMT  
		Size: 2.3 MB (2307029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2353964a560668eedd84fb43430edc9fad3e54cd4691d63f0eea0488c0bf92a3`  
		Last Modified: Tue, 02 Sep 2025 09:21:38 GMT  
		Size: 38.5 KB (38495 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:5a6d3b6becb4b1d23efac5583ae0c4199eb4323cb254057d77fca2bc11d6524b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.5 MB (185494336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4996deeeeaaee4aae6243b279cf8e87a95950c1ba55897cfd5b573025aad37f`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 05 Aug 2025 06:32:13 GMT
ARG RELEASE
# Tue, 05 Aug 2025 06:32:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 05 Aug 2025 06:32:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 05 Aug 2025 06:32:13 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 05 Aug 2025 06:32:13 GMT
ADD file:29917512cc6cafe60268e67a6ab4ee1e581cd8f4c2bca9a228ba5a680375b746 in / 
# Tue, 05 Aug 2025 06:32:13 GMT
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
```

-	Layers:
	-	`sha256:2109104756ac117958527cffddc193d2cf33d0621953649a7d5800a93fa86665`  
		Last Modified: Mon, 01 Sep 2025 22:59:18 GMT  
		Size: 28.0 MB (28003668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bf2d3d267a3b9732481174fcba7d138507ff103bf415dc927e0315a8dba6ad`  
		Last Modified: Mon, 01 Sep 2025 23:52:51 GMT  
		Size: 1.5 MB (1455714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23041f9fb1025131e13518bbacaff8850699669b14e32fda791934ebd107971e`  
		Last Modified: Tue, 02 Sep 2025 02:16:22 GMT  
		Size: 132.3 MB (132290825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f466171c610790c04bbe144239f749d30d85f3c1d04a87457d0e90165eb32fc`  
		Last Modified: Tue, 02 Sep 2025 01:31:04 GMT  
		Size: 114.6 KB (114644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033b7a5b9ec5481fd3fb5640775d7f0ba262e72954e7c94e33c7e32ac032899b`  
		Last Modified: Tue, 02 Sep 2025 01:31:05 GMT  
		Size: 17.6 MB (17649882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8b93fffcc74bc794661912a1b8231092efd0e7ffdae5375d92d0f25567d8a7`  
		Last Modified: Tue, 02 Sep 2025 01:31:04 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3504ac1641ec0769fac45c9b35613c42f9283ac2324737a25e4d15ec99fd7c67`  
		Last Modified: Tue, 02 Sep 2025 01:31:04 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f259657e4e76b2b31c241ca3fa515ee8b2c72f70d02e287a8cc509b2a89278`  
		Last Modified: Tue, 02 Sep 2025 01:31:04 GMT  
		Size: 14.3 KB (14288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf78123d54db43db8424856da3e844372cdcbb89aca0e0ed85cc8926817dd5b6`  
		Last Modified: Tue, 02 Sep 2025 01:31:04 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b7916ed199714e72f8fc3f1e1876604bbd9f409b4645123ddb16ac32e99f26`  
		Last Modified: Tue, 02 Sep 2025 01:31:04 GMT  
		Size: 15.1 KB (15114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b1655b7414b69b8c9ee2d099428c5224af43ded9e0170277305c362fdad48a`  
		Last Modified: Tue, 02 Sep 2025 01:31:05 GMT  
		Size: 5.9 MB (5947851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:a510e133331477f01ab16e5a624d035b31b62fe524df7b436ecce3e37d300d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2340964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b3a1f06a30f2d4f1514c9c938da44d3778617db6cb05dc9611675397c624c41`

```dockerfile
```

-	Layers:
	-	`sha256:6aca5df339d934d79349cf17bfb89c58de6a2c0324432084eb42a535cb5c5023`  
		Last Modified: Tue, 02 Sep 2025 03:22:45 GMT  
		Size: 2.3 MB (2302515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7365ad755065cef3b37dda3ae0e543a83198bf2e931119006a8eabe4ab243c17`  
		Last Modified: Tue, 02 Sep 2025 03:22:46 GMT  
		Size: 38.4 KB (38449 bytes)  
		MIME: application/vnd.in-toto+json
