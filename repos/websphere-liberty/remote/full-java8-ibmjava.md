## `websphere-liberty:full-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:995464c1bfea955e5f2d886ce42998aee93562ad0de48dfdf7d893f2b4e20a1e
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
$ docker pull websphere-liberty@sha256:3d55dea5934c4e38a7eacf12759bd3ef97805aacff44a08f6c1ae1f039d9f28c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.5 MB (570454052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6597d106aed131728e87f233c534f1fe9d2f83191a653004cec63491d78ae4b`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 11 Sep 2025 07:18:43 GMT
ARG RELEASE
# Thu, 11 Sep 2025 07:18:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Sep 2025 07:18:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Sep 2025 07:18:43 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Sep 2025 07:18:43 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Thu, 11 Sep 2025 07:18:43 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 07:18:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 11 Sep 2025 07:18:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_VERSION=8.0.8.51
# Thu, 11 Sep 2025 07:18:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f60e0d5d6ccfd8485f946e32a47aa2f27c8c3ffea4f8be3da44fd485e769296b';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='3570bdc9bc6171ca97900a592ca0958630abf445980054cf196a565369b31dd8';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='a2e8c1dc63e33ac0b62072ea27c8ab7aa0e77f16214079fd0d4e4e3ab00770db';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Thu, 11 Sep 2025 16:08:13 GMT
USER root
# Thu, 11 Sep 2025 16:08:13 GMT
ARG VERBOSE=false
# Thu, 11 Sep 2025 16:08:13 GMT
ARG OPENJ9_SCC=true
# Thu, 11 Sep 2025 16:08:13 GMT
ARG LIBERTY_VERSION=25.0.0.9
# Thu, 11 Sep 2025 16:08:13 GMT
ARG LIBERTY_BUILD_LABEL=cl250920250821-1629
# Thu, 11 Sep 2025 16:08:13 GMT
ARG LIBERTY_SHA=7bfd3fb8cb8034df7e237e354af8da53892df731
# Thu, 11 Sep 2025 16:08:13 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.9 org.opencontainers.image.revision=cl250920250821-1629 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.9 com.ibm.websphere.liberty.version=25.0.0.9
# Thu, 11 Sep 2025 16:08:13 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Thu, 11 Sep 2025 16:08:13 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.9 BuildLabel=cl250920250821-1629
# Thu, 11 Sep 2025 16:08:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.9 LIBERTY_BUILD_LABEL=cl250920250821-1629 LIBERTY_SHA=7bfd3fb8cb8034df7e237e354af8da53892df731
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
ARG LIBERTY_URL
# Thu, 11 Sep 2025 16:08:13 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 11 Sep 2025 16:08:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.9 LIBERTY_BUILD_LABEL=cl250920250821-1629 LIBERTY_SHA=7bfd3fb8cb8034df7e237e354af8da53892df731 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 11 Sep 2025 16:08:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.9 LIBERTY_BUILD_LABEL=cl250920250821-1629 LIBERTY_SHA=7bfd3fb8cb8034df7e237e354af8da53892df731 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.9 LIBERTY_BUILD_LABEL=cl250920250821-1629 LIBERTY_SHA=7bfd3fb8cb8034df7e237e354af8da53892df731 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.9 LIBERTY_BUILD_LABEL=cl250920250821-1629 LIBERTY_SHA=7bfd3fb8cb8034df7e237e354af8da53892df731 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Thu, 11 Sep 2025 16:08:13 GMT
USER 1001
# Thu, 11 Sep 2025 16:08:13 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 11 Sep 2025 16:08:13 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 11 Sep 2025 16:08:13 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 11 Sep 2025 16:08:13 GMT
ARG VERBOSE=false
# Thu, 11 Sep 2025 16:08:13 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 11 Sep 2025 16:08:13 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b630d2ba464c8bd8ff49280b803545a8da1fa9eff9a591020617488ac256d2df`  
		Last Modified: Thu, 02 Oct 2025 05:08:57 GMT  
		Size: 1.5 MB (1450007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2fcbd100eba59226b4675b5327cd91948d812f20109027a03ea109bbc357e30`  
		Last Modified: Thu, 02 Oct 2025 08:02:56 GMT  
		Size: 135.4 MB (135417529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af773c37db4d04d79cfd5d10e3d2b190528d914a5ab6bb2dc132f8380e68e2ac`  
		Last Modified: Thu, 02 Oct 2025 08:52:59 GMT  
		Size: 113.7 KB (113665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18b04162d030701c582aed028c7ebaa33eda4f2aca9883444236fcf3e5aee49`  
		Last Modified: Thu, 02 Oct 2025 08:52:59 GMT  
		Size: 17.7 MB (17659237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61673341d43aefb1ba2965e2a3f9a2330394dcb19d7954b06b032dabefa8245`  
		Last Modified: Thu, 02 Oct 2025 08:52:59 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9966917635c61f93b6e54f84eaf801331eb1ca283c3bc9226f1a765e3904a7`  
		Last Modified: Thu, 02 Oct 2025 08:52:59 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5349479359cc739f6e10850d10dca29fe0c9f825b657527dd8b745643e772a`  
		Last Modified: Thu, 02 Oct 2025 08:52:59 GMT  
		Size: 14.3 KB (14285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4c98ac9a5c961acf58b4ed7bf5d325b833f055b06cd8a3e759856466cba0e4`  
		Last Modified: Thu, 02 Oct 2025 08:52:59 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833b50db437d4026097665ec68aaa8b0d611b0e6537a0fe1867f39214b1c9f61`  
		Last Modified: Thu, 02 Oct 2025 08:52:59 GMT  
		Size: 15.1 KB (15113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b4ead831e1f5633bf08e0e2fade8a0f585e0ce4086cde4537cb14a812fb248`  
		Last Modified: Thu, 02 Oct 2025 08:52:59 GMT  
		Size: 5.8 MB (5819341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53873a99f3ef6d4323cb0cd5c74d43e580424b6c08eac4718d18f865eeec35dd`  
		Last Modified: Thu, 02 Oct 2025 12:21:17 GMT  
		Size: 365.0 MB (364950158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d083f3a30b23e369fbc3510091f1fb68f06fc8170197b519244698e6053971`  
		Last Modified: Thu, 02 Oct 2025 12:21:22 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89bb8b58ad04ae866be16ce5cb99de70b4a7e74266f1f48d0fcd30a4307473a`  
		Last Modified: Thu, 02 Oct 2025 12:21:24 GMT  
		Size: 15.5 MB (15474606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:4cf3c8e2d72b39e62e75c22add3b5dc36cf1f81435cb0bb50100f81ac624fd91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4376632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9053c72800f759c821279bd3d1dd334db882c72a3506b657b135f363b139556`

```dockerfile
```

-	Layers:
	-	`sha256:8cda46251577f16e6ae0a7541fa95597a2bc73da08b2ecc3a06b60393296c05e`  
		Last Modified: Thu, 02 Oct 2025 15:21:43 GMT  
		Size: 4.4 MB (4357511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35eea31ccd602cb77b2845468c81188d7c89e48d60a069af91470faa8626d63a`  
		Last Modified: Thu, 02 Oct 2025 15:21:44 GMT  
		Size: 19.1 KB (19121 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:de006eed251551b529eaef4b3177fbd7417b54e721040491cca7eebc54f70dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.0 MB (573951355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc5b0bcdd181936dc1751a812010c15056db2bd5bb45624590ee79fcc6a234c`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 11 Sep 2025 07:18:43 GMT
ARG RELEASE
# Thu, 11 Sep 2025 07:18:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Sep 2025 07:18:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Sep 2025 07:18:43 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Sep 2025 07:18:43 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Thu, 11 Sep 2025 07:18:43 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 07:18:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 11 Sep 2025 07:18:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_VERSION=8.0.8.51
# Thu, 11 Sep 2025 07:18:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f60e0d5d6ccfd8485f946e32a47aa2f27c8c3ffea4f8be3da44fd485e769296b';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='3570bdc9bc6171ca97900a592ca0958630abf445980054cf196a565369b31dd8';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='a2e8c1dc63e33ac0b62072ea27c8ab7aa0e77f16214079fd0d4e4e3ab00770db';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Thu, 11 Sep 2025 16:08:13 GMT
USER root
# Thu, 11 Sep 2025 16:08:13 GMT
ARG VERBOSE=false
# Thu, 11 Sep 2025 16:08:13 GMT
ARG OPENJ9_SCC=true
# Thu, 11 Sep 2025 16:08:13 GMT
ARG LIBERTY_VERSION=25.0.0.9
# Thu, 11 Sep 2025 16:08:13 GMT
ARG LIBERTY_BUILD_LABEL=cl250920250821-1629
# Thu, 11 Sep 2025 16:08:13 GMT
ARG LIBERTY_SHA=7bfd3fb8cb8034df7e237e354af8da53892df731
# Thu, 11 Sep 2025 16:08:13 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.9 org.opencontainers.image.revision=cl250920250821-1629 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.9 com.ibm.websphere.liberty.version=25.0.0.9
# Thu, 11 Sep 2025 16:08:13 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Thu, 11 Sep 2025 16:08:13 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.9 BuildLabel=cl250920250821-1629
# Thu, 11 Sep 2025 16:08:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.9 LIBERTY_BUILD_LABEL=cl250920250821-1629 LIBERTY_SHA=7bfd3fb8cb8034df7e237e354af8da53892df731
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
ARG LIBERTY_URL
# Thu, 11 Sep 2025 16:08:13 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 11 Sep 2025 16:08:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.9 LIBERTY_BUILD_LABEL=cl250920250821-1629 LIBERTY_SHA=7bfd3fb8cb8034df7e237e354af8da53892df731 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 11 Sep 2025 16:08:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.9 LIBERTY_BUILD_LABEL=cl250920250821-1629 LIBERTY_SHA=7bfd3fb8cb8034df7e237e354af8da53892df731 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.9 LIBERTY_BUILD_LABEL=cl250920250821-1629 LIBERTY_SHA=7bfd3fb8cb8034df7e237e354af8da53892df731 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.9 LIBERTY_BUILD_LABEL=cl250920250821-1629 LIBERTY_SHA=7bfd3fb8cb8034df7e237e354af8da53892df731 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Thu, 11 Sep 2025 16:08:13 GMT
USER 1001
# Thu, 11 Sep 2025 16:08:13 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 11 Sep 2025 16:08:13 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 11 Sep 2025 16:08:13 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 11 Sep 2025 16:08:13 GMT
ARG VERBOSE=false
# Thu, 11 Sep 2025 16:08:13 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 11 Sep 2025 16:08:13 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47fbbb835d2e356809aec45fea40b6f5278fa45ef4d3e943633fba2d851c7c9`  
		Last Modified: Thu, 02 Oct 2025 03:15:21 GMT  
		Size: 1.5 MB (1536203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb52a404998e428dd16934db1dfa0502df2cb19148926c0a32dfd93bf873cb6`  
		Last Modified: Thu, 02 Oct 2025 14:12:08 GMT  
		Size: 136.4 MB (136363132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80b888ac263401bc45e5c366d3d3ab943cb5ead4aba8514a0b21189fc0de4b8`  
		Last Modified: Thu, 02 Oct 2025 07:36:23 GMT  
		Size: 118.1 KB (118086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bc3dd2c12a8a192c19b9f1d2f3885952e201aaa23d5cd96551b4b1ac36e8df`  
		Last Modified: Thu, 02 Oct 2025 07:36:32 GMT  
		Size: 17.7 MB (17659634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afea8ba4a6a1f31d98cb729309b9eed94ec60ccacce1db87060722082def6f5`  
		Last Modified: Thu, 02 Oct 2025 07:36:25 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6dda79dc648ab5e98a56706c452782b9a138ef0dad73a920a8d9bd6753af1a`  
		Last Modified: Thu, 02 Oct 2025 07:36:25 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78994b2cc8d273c93fe16c36f027bb56f6b2be818016cda11d8899a2e40f137`  
		Last Modified: Thu, 02 Oct 2025 07:36:27 GMT  
		Size: 14.3 KB (14286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430e6ca1fb8cc22e67e56f790aed03f6bd9de6b63b5d1a1aecdfa208af616361`  
		Last Modified: Thu, 02 Oct 2025 07:36:28 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0c6331b3dea6426f7edafbe45d1003c13f847223fd4ea77ed81c8bbf978749`  
		Last Modified: Thu, 02 Oct 2025 07:36:28 GMT  
		Size: 15.1 KB (15124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e4fdaa48904512a2db017d493ad14d7ef310964c4e3db7b58932b56b2e367a`  
		Last Modified: Thu, 02 Oct 2025 07:36:29 GMT  
		Size: 5.4 MB (5402230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed0c45781ced856181430f1600edaa2dd359607de4758e07525f598088a4b82`  
		Last Modified: Thu, 02 Oct 2025 14:12:10 GMT  
		Size: 365.0 MB (364950762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede8bd5850217eba7f5d5a0f3cf641bd1f2b02dd5008ae09e04d283e2d90c18b`  
		Last Modified: Thu, 02 Oct 2025 13:57:03 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077c37027581b784a577ce4e845717cb1377dbd8bd3152c4c9fc372e0f24e2cf`  
		Last Modified: Thu, 02 Oct 2025 13:57:04 GMT  
		Size: 13.4 MB (13441804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:d7e04b827273bfc2d6c4bf11f539550fc4545641d86a75d3164e39e310171d0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4379948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7161effcf38738039c0f42140cf800edc834b2645f4d4f569ddc1aced69c6b32`

```dockerfile
```

-	Layers:
	-	`sha256:cec46d7234f0abe67a89a526ae9e83684a9d1a69f04131119aa6ba779e8bc0d9`  
		Last Modified: Thu, 02 Oct 2025 15:21:49 GMT  
		Size: 4.4 MB (4360786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ada5fa5463f60be7c3380af32f9d3b5533e2390527e29a7fa9af46c101e2f4a`  
		Last Modified: Thu, 02 Oct 2025 15:21:49 GMT  
		Size: 19.2 KB (19162 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:d887e3a88592770e4232252f33f3c3795d68c0282c7ccb7bf43148e95f7c706a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **566.3 MB (566333007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77b4f2b10aad6f50c9e8ec57c918fe9c811907ba4830a6e3822236c2f4e1787f`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 11 Sep 2025 07:18:43 GMT
ARG RELEASE
# Thu, 11 Sep 2025 07:18:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Sep 2025 07:18:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Sep 2025 07:18:43 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Sep 2025 07:18:43 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Thu, 11 Sep 2025 07:18:43 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 07:18:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 11 Sep 2025 07:18:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_VERSION=8.0.8.51
# Thu, 11 Sep 2025 07:18:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f60e0d5d6ccfd8485f946e32a47aa2f27c8c3ffea4f8be3da44fd485e769296b';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='3570bdc9bc6171ca97900a592ca0958630abf445980054cf196a565369b31dd8';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='a2e8c1dc63e33ac0b62072ea27c8ab7aa0e77f16214079fd0d4e4e3ab00770db';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Thu, 11 Sep 2025 16:08:13 GMT
USER root
# Thu, 11 Sep 2025 16:08:13 GMT
ARG VERBOSE=false
# Thu, 11 Sep 2025 16:08:13 GMT
ARG OPENJ9_SCC=true
# Thu, 11 Sep 2025 16:08:13 GMT
ARG LIBERTY_VERSION=25.0.0.9
# Thu, 11 Sep 2025 16:08:13 GMT
ARG LIBERTY_BUILD_LABEL=cl250920250821-1629
# Thu, 11 Sep 2025 16:08:13 GMT
ARG LIBERTY_SHA=7bfd3fb8cb8034df7e237e354af8da53892df731
# Thu, 11 Sep 2025 16:08:13 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.9 org.opencontainers.image.revision=cl250920250821-1629 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.9 com.ibm.websphere.liberty.version=25.0.0.9
# Thu, 11 Sep 2025 16:08:13 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Thu, 11 Sep 2025 16:08:13 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.9 BuildLabel=cl250920250821-1629
# Thu, 11 Sep 2025 16:08:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.9 LIBERTY_BUILD_LABEL=cl250920250821-1629 LIBERTY_SHA=7bfd3fb8cb8034df7e237e354af8da53892df731
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
ARG LIBERTY_URL
# Thu, 11 Sep 2025 16:08:13 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 11 Sep 2025 16:08:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.9 LIBERTY_BUILD_LABEL=cl250920250821-1629 LIBERTY_SHA=7bfd3fb8cb8034df7e237e354af8da53892df731 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 11 Sep 2025 16:08:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.9 LIBERTY_BUILD_LABEL=cl250920250821-1629 LIBERTY_SHA=7bfd3fb8cb8034df7e237e354af8da53892df731 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.9 LIBERTY_BUILD_LABEL=cl250920250821-1629 LIBERTY_SHA=7bfd3fb8cb8034df7e237e354af8da53892df731 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.9 LIBERTY_BUILD_LABEL=cl250920250821-1629 LIBERTY_SHA=7bfd3fb8cb8034df7e237e354af8da53892df731 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Thu, 11 Sep 2025 16:08:13 GMT
USER 1001
# Thu, 11 Sep 2025 16:08:13 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 11 Sep 2025 16:08:13 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 11 Sep 2025 16:08:13 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 11 Sep 2025 16:08:13 GMT
ARG VERBOSE=false
# Thu, 11 Sep 2025 16:08:13 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 11 Sep 2025 16:08:13 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:e4a5a322dd65d010805129ca793d5d5e6b07872cbc2f41d566a84091b39c794e`  
		Last Modified: Thu, 02 Oct 2025 00:25:04 GMT  
		Size: 28.0 MB (28003413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b543bf796c5e3ca3d689f3ec6349f0c52c782a4da34026d3f7dbd32fbf895bed`  
		Last Modified: Thu, 02 Oct 2025 02:03:56 GMT  
		Size: 1.5 MB (1455749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de907172531984cb0df927f7d324217899d7c8530a0aaaba07ce8be7ff47a848`  
		Last Modified: Thu, 02 Oct 2025 05:01:35 GMT  
		Size: 132.3 MB (132288850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c378a2a2f164fee0bff632d20a0d998af396c8eb68d7549d8ee6b791443ba465`  
		Last Modified: Thu, 02 Oct 2025 04:03:25 GMT  
		Size: 114.6 KB (114615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d9e7c788ad3241d09a823882db1d30270862bfc52b41615fbb6be9f71662a`  
		Last Modified: Thu, 02 Oct 2025 04:03:26 GMT  
		Size: 17.7 MB (17658953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b91c7f0a27ee207bc4b4b865001c69236c92aef786aa032ecfe186e30419a7`  
		Last Modified: Thu, 02 Oct 2025 04:03:25 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8502befe8ba123a433043b526db5e3e5f098ac4c99bcef5b7caf81d2f855a1a0`  
		Last Modified: Thu, 02 Oct 2025 04:03:25 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6398cb55994d5c16b1141d8f436181cf10c2c020e5235de9a14257f7fa84c6cd`  
		Last Modified: Thu, 02 Oct 2025 04:03:25 GMT  
		Size: 14.3 KB (14283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a4e80422de1df8f749befae3b90696485fdc21aaca99ffbb4be3bb23fb5b17`  
		Last Modified: Thu, 02 Oct 2025 04:03:25 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d63c5ef139fad28e1b0ff33e00b9a632501fdf25c884151e1c616da759c0b4`  
		Last Modified: Thu, 02 Oct 2025 04:03:25 GMT  
		Size: 15.1 KB (15115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6956fb511930294337abb978847d7a7392f06ee1f794fa03fef5a0ba57d607d3`  
		Last Modified: Thu, 02 Oct 2025 04:03:25 GMT  
		Size: 6.0 MB (5955323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b49ba599c21fe298a776438f8dc42ff436163942dc74633234fab640247998`  
		Last Modified: Thu, 02 Oct 2025 06:13:18 GMT  
		Size: 365.0 MB (364951101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495883a670b79aaa99a060d34ad3967432fa09b73c5c0098dab3824902dd0998`  
		Last Modified: Thu, 02 Oct 2025 06:02:04 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101460b83f7a25333adbfdff0d96d31cd069ee2965d209c90a353f461002f8b2`  
		Last Modified: Thu, 02 Oct 2025 06:02:11 GMT  
		Size: 15.9 MB (15872310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:fef6f51f51d24e0639c830f1b2730152d2e20a694a44cf3a62a4e3f3123131a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4375393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f47167c29f53999a4d98cfe1b1a67db3d4f5c34aa31e9b3cc8f2d6bb8b524ba`

```dockerfile
```

-	Layers:
	-	`sha256:2fa7ff632eb6195696357a4c8ec9720769ac8aef11ed7168f9f80c762ecbecb8`  
		Last Modified: Thu, 02 Oct 2025 06:22:29 GMT  
		Size: 4.4 MB (4356272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94ea5cac8b1952409851d3f16d1fff4f1cff873b1a440c1b1a7477f0b34b45c8`  
		Last Modified: Thu, 02 Oct 2025 06:22:30 GMT  
		Size: 19.1 KB (19121 bytes)  
		MIME: application/vnd.in-toto+json
