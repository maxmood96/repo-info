## `websphere-liberty:kernel`

```console
$ docker pull websphere-liberty@sha256:9ffc290fca1ef5c518b54dd79d9b2439ad9d6ae08bc5016b0adec69ebf0d2ff9
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
$ docker pull websphere-liberty@sha256:5fbcd0868191ae1c4f04ec77f6264432fca08d834b38788a4a49c3c6b39a117b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.1 MB (190068685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3790e34090b0a0a71c2aeb83075a69eb0bdd03161e3fa27e877086391ef2006`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 23:53:58 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 30 Oct 2025 23:53:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 23:53:58 GMT
ENV JAVA_VERSION=8.0.8.55
# Thu, 30 Oct 2025 23:54:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a6095b036bda7d4344607de6b91823d7704d2bf8b1c4c4cb4b01aa87e9ac0e1f';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a1d3984e2f6971117f950bcc6ac88ea5e4772e687b41af95ceb569cc47b82c73';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='37d9a6cbdd5ce45605d8b05843770151f857efc1280071bdc293cab4dc967c6d';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 30 Oct 2025 23:54:06 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 31 Oct 2025 00:13:48 GMT
USER root
# Fri, 31 Oct 2025 00:13:48 GMT
ARG VERBOSE=false
# Fri, 31 Oct 2025 00:13:48 GMT
ARG OPENJ9_SCC=true
# Fri, 31 Oct 2025 00:13:48 GMT
ARG LIBERTY_VERSION=25.0.0.10
# Fri, 31 Oct 2025 00:13:48 GMT
ARG LIBERTY_BUILD_LABEL=cl251020250923-1355
# Fri, 31 Oct 2025 00:13:48 GMT
ARG LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa
# Fri, 31 Oct 2025 00:13:48 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.10 org.opencontainers.image.revision=cl251020250923-1355 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.10 com.ibm.websphere.liberty.version=25.0.0.10
# Fri, 31 Oct 2025 00:13:48 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Fri, 31 Oct 2025 00:13:48 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.10 BuildLabel=cl251020250923-1355
# Fri, 31 Oct 2025 00:13:48 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 31 Oct 2025 00:13:48 GMT
ARG LIBERTY_URL
# Fri, 31 Oct 2025 00:13:48 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 31 Oct 2025 00:13:57 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Oct 2025 00:13:57 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 31 Oct 2025 00:13:57 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 31 Oct 2025 00:13:57 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Fri, 31 Oct 2025 00:13:57 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Fri, 31 Oct 2025 00:13:57 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Fri, 31 Oct 2025 00:13:58 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 31 Oct 2025 00:14:03 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Fri, 31 Oct 2025 00:14:03 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 31 Oct 2025 00:14:03 GMT
USER 1001
# Fri, 31 Oct 2025 00:14:03 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 31 Oct 2025 00:14:03 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 31 Oct 2025 00:14:03 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23311177b9d27a75a99852778c82058eb31857a33e6c02ab885b46db249dfb6`  
		Last Modified: Thu, 30 Oct 2025 23:54:29 GMT  
		Size: 1.5 MB (1450037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66f1caeb7e84826796a497d9ceb42d9b8215b3a835f80f501735abb6593db75`  
		Last Modified: Fri, 31 Oct 2025 00:13:35 GMT  
		Size: 135.5 MB (135541117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55c6a04305182e6a97f06c1beb703e4907cd7ebe573341f683761c60e44ae39`  
		Last Modified: Fri, 31 Oct 2025 00:14:22 GMT  
		Size: 113.7 KB (113667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dcc245c0e8c829b153ec9ccf821c4efa237834af38fbb50481cd55aa435015f`  
		Last Modified: Fri, 31 Oct 2025 00:14:26 GMT  
		Size: 17.7 MB (17655713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db849eaa97f29ae067bf184e7685841c10e9e4dd5d1a8e0b48a1f2da9dcc639`  
		Last Modified: Fri, 31 Oct 2025 00:14:22 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425e491d67ea016afc4e311cafd3a99c97b886397dc7764382d168c242a5a9b5`  
		Last Modified: Fri, 31 Oct 2025 00:14:22 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a288877d9a0dbe73942107325353079fd908c20fdc4df62270aab83e2ee94d`  
		Last Modified: Fri, 31 Oct 2025 00:14:22 GMT  
		Size: 14.4 KB (14391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2d5f836558d12ed1f85d97c26261de7cc0aef8e4a4dceea3389da15eaf93bf`  
		Last Modified: Fri, 31 Oct 2025 00:14:22 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f398bdac7c7263b997fecb65ba6e81bd76ea1949be46584118f71e4db134226`  
		Last Modified: Fri, 31 Oct 2025 00:14:22 GMT  
		Size: 15.3 KB (15266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b5120eaa54bcf09f0660938c50c4a8789466cdc17e6a7fe4a991c20d09b136`  
		Last Modified: Fri, 31 Oct 2025 00:14:23 GMT  
		Size: 5.7 MB (5739331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:3e0787b80a9fe6fbaf8984f8d0d55d45381d40c1053182036d58a82162353c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2343327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c216ce29dba3a4b02ac0c1fd82c910354bf084c0ab4c80c0f94c205ff12ec1`

```dockerfile
```

-	Layers:
	-	`sha256:01c878e9861b029b44f8d5beb776687fdc956c7bddac9308fce30ca47d4a6bd7`  
		Last Modified: Fri, 31 Oct 2025 03:20:46 GMT  
		Size: 2.3 MB (2304336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65871cc3d0b8cfcbcfc1992216b9e61c9d169eaaf6fb4243cffe80592f9bd428`  
		Last Modified: Fri, 31 Oct 2025 03:20:47 GMT  
		Size: 39.0 KB (38991 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:4e7b30cf9b1f67a015fd0b1ed57f03f6cee72ff5b14809adfc571648b5145d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195657676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:278b0d2625386b0ebaa299dd13db5a75a41b4f944f88ceb0af428b06bd3c779d`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 01 Oct 2025 07:06:37 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:06:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:06:42 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Wed, 01 Oct 2025 07:06:43 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:46:30 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 31 Oct 2025 00:46:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Oct 2025 00:46:30 GMT
ENV JAVA_VERSION=8.0.8.55
# Fri, 31 Oct 2025 00:46:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a6095b036bda7d4344607de6b91823d7704d2bf8b1c4c4cb4b01aa87e9ac0e1f';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a1d3984e2f6971117f950bcc6ac88ea5e4772e687b41af95ceb569cc47b82c73';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='37d9a6cbdd5ce45605d8b05843770151f857efc1280071bdc293cab4dc967c6d';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 31 Oct 2025 00:46:40 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 31 Oct 2025 01:10:29 GMT
USER root
# Fri, 31 Oct 2025 01:10:29 GMT
ARG VERBOSE=false
# Fri, 31 Oct 2025 01:10:29 GMT
ARG OPENJ9_SCC=true
# Fri, 31 Oct 2025 01:10:29 GMT
ARG LIBERTY_VERSION=25.0.0.10
# Fri, 31 Oct 2025 01:10:29 GMT
ARG LIBERTY_BUILD_LABEL=cl251020250923-1355
# Fri, 31 Oct 2025 01:10:29 GMT
ARG LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa
# Fri, 31 Oct 2025 01:10:29 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.10 org.opencontainers.image.revision=cl251020250923-1355 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.10 com.ibm.websphere.liberty.version=25.0.0.10
# Fri, 31 Oct 2025 01:10:29 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Fri, 31 Oct 2025 01:10:29 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.10 BuildLabel=cl251020250923-1355
# Fri, 31 Oct 2025 01:10:29 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 31 Oct 2025 01:10:29 GMT
ARG LIBERTY_URL
# Fri, 31 Oct 2025 01:10:29 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 31 Oct 2025 01:10:39 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Oct 2025 01:10:39 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 31 Oct 2025 01:10:40 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 31 Oct 2025 01:10:41 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Fri, 31 Oct 2025 01:10:42 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Fri, 31 Oct 2025 01:10:42 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Fri, 31 Oct 2025 01:10:43 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 31 Oct 2025 01:10:52 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Fri, 31 Oct 2025 01:10:52 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 31 Oct 2025 01:10:52 GMT
USER 1001
# Fri, 31 Oct 2025 01:10:52 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 31 Oct 2025 01:10:52 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 31 Oct 2025 01:10:52 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b2c2c5b1d0021029ccc4064df99950687160117bc008ac4bce5618b2dd9154`  
		Last Modified: Fri, 31 Oct 2025 00:47:22 GMT  
		Size: 1.5 MB (1536224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71758d1bf4a4ec11b0b439b7f4e5df0559ccc7ccaa49ca2ddd38186a648e5466`  
		Last Modified: Fri, 31 Oct 2025 02:39:40 GMT  
		Size: 136.5 MB (136486921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6633947d9c68200fa3c0defb154480854eea090260f36dd6607ee13ad329a850`  
		Last Modified: Fri, 31 Oct 2025 01:11:21 GMT  
		Size: 118.1 KB (118068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df24564a32e5e53bafe87a281883f11603f7d0d0761ea60dd4161f622949e3e`  
		Last Modified: Fri, 31 Oct 2025 01:11:22 GMT  
		Size: 17.7 MB (17656037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dae845a3b72cd91a1b5c87f45a7ec8c3a4784a6637deb91be2c4ee4d17fce9d`  
		Last Modified: Fri, 31 Oct 2025 01:11:20 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e94c3b2b4a1f9b8293ea28b7690825f242420e1a473ab9c87bbccb51f52250`  
		Last Modified: Fri, 31 Oct 2025 01:11:21 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e743973d24630caf8438dd0b3698b832820642e7b34aa4d1e5a2215a32c90e`  
		Last Modified: Fri, 31 Oct 2025 01:11:21 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25465c086442061b5f4653f0cb8efaa27e77182f5e569784fbd832667fe584b2`  
		Last Modified: Fri, 31 Oct 2025 01:11:21 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdbf447fa59608a84e35d9c593ce3767f79de6e86fe1886008e44259502f1482`  
		Last Modified: Fri, 31 Oct 2025 01:11:21 GMT  
		Size: 15.3 KB (15271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea028410d05c922ba9140c97c0d29eacf943d6b57c6373e0c540902c75ee728`  
		Last Modified: Fri, 31 Oct 2025 01:11:21 GMT  
		Size: 5.4 MB (5381638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:5283105cb6fa6928c3312c14835a7de437d1d7f2b9b289644042b7fb57c7dd71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2346648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c49002e1c6e4da7e1af035ebfa52777d3bd3e07c22be1f912df7ecd97f08e8`

```dockerfile
```

-	Layers:
	-	`sha256:fdf20fd0c56ef5721ab3b65cf9ec409fa174e900a9ccc53fa730747d61545098`  
		Last Modified: Fri, 31 Oct 2025 03:20:52 GMT  
		Size: 2.3 MB (2307611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dac25747b924e46132f4f1348784fd009ad7e170567514b0a8f1f799d0c15833`  
		Last Modified: Fri, 31 Oct 2025 03:20:53 GMT  
		Size: 39.0 KB (39037 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:3a93312bda053d4748e365fe0b1efb064bd3acfe46c12bbc8ce8019f1eac76a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.2 MB (186241982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eb0852b0fb07c515a55748c958a72b71f835c4c99bd1e65ccf97428adcc47aa`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:26 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:28 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Wed, 01 Oct 2025 07:05:28 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 22:32:22 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 30 Oct 2025 22:32:22 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 22:32:22 GMT
ENV JAVA_VERSION=8.0.8.55
# Thu, 30 Oct 2025 22:32:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a6095b036bda7d4344607de6b91823d7704d2bf8b1c4c4cb4b01aa87e9ac0e1f';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a1d3984e2f6971117f950bcc6ac88ea5e4772e687b41af95ceb569cc47b82c73';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='37d9a6cbdd5ce45605d8b05843770151f857efc1280071bdc293cab4dc967c6d';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 30 Oct 2025 22:32:30 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Thu, 30 Oct 2025 23:10:44 GMT
USER root
# Thu, 30 Oct 2025 23:10:44 GMT
ARG VERBOSE=false
# Thu, 30 Oct 2025 23:10:44 GMT
ARG OPENJ9_SCC=true
# Thu, 30 Oct 2025 23:10:44 GMT
ARG LIBERTY_VERSION=25.0.0.10
# Thu, 30 Oct 2025 23:10:44 GMT
ARG LIBERTY_BUILD_LABEL=cl251020250923-1355
# Thu, 30 Oct 2025 23:10:44 GMT
ARG LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa
# Thu, 30 Oct 2025 23:10:44 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.10 org.opencontainers.image.revision=cl251020250923-1355 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.10 com.ibm.websphere.liberty.version=25.0.0.10
# Thu, 30 Oct 2025 23:10:44 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Thu, 30 Oct 2025 23:10:44 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.10 BuildLabel=cl251020250923-1355
# Thu, 30 Oct 2025 23:10:44 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 30 Oct 2025 23:10:44 GMT
ARG LIBERTY_URL
# Thu, 30 Oct 2025 23:10:44 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 30 Oct 2025 23:11:20 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 23:11:20 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 30 Oct 2025 23:11:22 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 30 Oct 2025 23:11:22 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Thu, 30 Oct 2025 23:11:23 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Thu, 30 Oct 2025 23:11:24 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Thu, 30 Oct 2025 23:11:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Thu, 30 Oct 2025 23:11:37 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Thu, 30 Oct 2025 23:11:37 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Thu, 30 Oct 2025 23:11:37 GMT
USER 1001
# Thu, 30 Oct 2025 23:11:37 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 30 Oct 2025 23:11:37 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 30 Oct 2025 23:11:37 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:e4a5a322dd65d010805129ca793d5d5e6b07872cbc2f41d566a84091b39c794e`  
		Last Modified: Thu, 02 Oct 2025 00:25:04 GMT  
		Size: 28.0 MB (28003413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a741b67c0dbf6d2e66e6ffe23e30ec9031bce057ebe9e2cb812bbb79480aa2d`  
		Last Modified: Thu, 30 Oct 2025 22:33:02 GMT  
		Size: 1.5 MB (1455880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a84a4d22587d870899aa47dbf78b8c505bacb62aff4ef27f67a3e726f2d3aa`  
		Last Modified: Fri, 31 Oct 2025 02:26:34 GMT  
		Size: 133.0 MB (132950452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581c5323b4ffc276582fd5a7d00ab5bbc87f998e5d8323375d029a2be3b5b21c`  
		Last Modified: Thu, 30 Oct 2025 23:12:33 GMT  
		Size: 114.7 KB (114657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be72829a2a67a3d2928b56df2e577197ca0487112aa5483d557c9b1e47ae06e`  
		Last Modified: Thu, 30 Oct 2025 23:12:34 GMT  
		Size: 17.7 MB (17655493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef52288f7f40993e48868291041d009b72cf36eabe89e5d16dfb9dc0595798ff`  
		Last Modified: Thu, 30 Oct 2025 23:12:33 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f08d73472bdb754e4f46b2ce6cd355207ebcb83e83782e7488f6c4463d52155`  
		Last Modified: Thu, 30 Oct 2025 23:12:32 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6483bdd102b5f106117ebc5c18b355f79d2aa63774fa0d65c4dcfe7c75162fb5`  
		Last Modified: Thu, 30 Oct 2025 23:12:33 GMT  
		Size: 14.4 KB (14392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5bc652d01350a4dd0f5a077828ce174a5d98c4bb00c6a13523e77ed1542f14`  
		Last Modified: Thu, 30 Oct 2025 23:12:33 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf92a9c6dd90ceaa3edfe1c0818a93dd739a7a929ce4ba3e09c0a8f68a3a3f1`  
		Last Modified: Thu, 30 Oct 2025 23:12:33 GMT  
		Size: 15.3 KB (15273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25bbec8543ec9fb06149431357c24317f0291a0620c5c3c060fc6d4aec25555`  
		Last Modified: Thu, 30 Oct 2025 23:12:33 GMT  
		Size: 6.0 MB (6030072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:ed659bd58476b283534d12fb562e9994b41af8505f420e44a41244f0c168ef7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2342088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6166e7cead037c9442e0f33a893725312dda5981539873e2db7a113c86a97c01`

```dockerfile
```

-	Layers:
	-	`sha256:86f1f708b7ec01137528785f362a29efc9b035dd16b46f141c6faef72d94cdac`  
		Last Modified: Fri, 31 Oct 2025 00:20:41 GMT  
		Size: 2.3 MB (2303097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:989777a3c93d3c69b4a90e4060dc0c6b09a9d544544e3aa918334949f86b8d03`  
		Last Modified: Fri, 31 Oct 2025 00:20:42 GMT  
		Size: 39.0 KB (38991 bytes)  
		MIME: application/vnd.in-toto+json
