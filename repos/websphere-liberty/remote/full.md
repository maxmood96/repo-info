## `websphere-liberty:full`

```console
$ docker pull websphere-liberty@sha256:d6c63ae8083a3e1e27c0cf2e0839cb5d7693b7a654fd9e3cf1a46d6e0773854a
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
$ docker pull websphere-liberty@sha256:e8630a8c900be98463f11cf415194b29e0fd61b1fdd8ff3ce215e61120955a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.1 MB (594105952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f2cf7fd43b3dd4fb77c9b6639275b2693e497385d682dbdaa2437c6ba14320a`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:18:50 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 15 May 2026 21:18:50 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:18:50 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 15 May 2026 21:19:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f848631ac7f7e61aa26d1e648bc7a96e97da64c33cbc4f76627ea3b367c9a085';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='9fad050b730cf070b341e5f7b5353c6cdd0a5a6f2d2b150678bfdff1f94f2637';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c844b329e2161a7d0c5810b30085b5deeec28b911844220cb3b930f860b10884';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 15 May 2026 21:19:33 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 17 Jun 2026 22:06:03 GMT
USER root
# Wed, 17 Jun 2026 22:06:03 GMT
ARG VERBOSE=false
# Wed, 17 Jun 2026 22:06:03 GMT
ARG OPENJ9_SCC=true
# Wed, 17 Jun 2026 22:06:03 GMT
ARG LIBERTY_VERSION=26.0.0.6
# Wed, 17 Jun 2026 22:06:03 GMT
ARG LIBERTY_BUILD_LABEL=cl260620260531-0302
# Wed, 17 Jun 2026 22:06:03 GMT
ARG LIBERTY_SHA=7a614ebeb2fc9c6c542cc973b0575c0a8515173d
# Wed, 17 Jun 2026 22:06:03 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.6 org.opencontainers.image.revision=cl260620260531-0302 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.6 com.ibm.websphere.liberty.version=26.0.0.6
# Wed, 17 Jun 2026 22:06:03 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Wed, 17 Jun 2026 22:06:03 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.6 BuildLabel=cl260620260531-0302
# Wed, 17 Jun 2026 22:06:03 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.6 LIBERTY_BUILD_LABEL=cl260620260531-0302 LIBERTY_SHA=7a614ebeb2fc9c6c542cc973b0575c0a8515173d
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 17 Jun 2026 22:06:03 GMT
ARG LIBERTY_URL
# Wed, 17 Jun 2026 22:06:03 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 17 Jun 2026 22:06:15 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.6 LIBERTY_BUILD_LABEL=cl260620260531-0302 LIBERTY_SHA=7a614ebeb2fc9c6c542cc973b0575c0a8515173d LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jun 2026 22:06:15 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 17 Jun 2026 22:06:15 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.6 LIBERTY_BUILD_LABEL=cl260620260531-0302 LIBERTY_SHA=7a614ebeb2fc9c6c542cc973b0575c0a8515173d LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 17 Jun 2026 22:06:15 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 17 Jun 2026 22:06:15 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 17 Jun 2026 22:06:16 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 17 Jun 2026 22:06:16 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.6 LIBERTY_BUILD_LABEL=cl260620260531-0302 LIBERTY_SHA=7a614ebeb2fc9c6c542cc973b0575c0a8515173d LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Wed, 17 Jun 2026 22:06:21 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.6 LIBERTY_BUILD_LABEL=cl260620260531-0302 LIBERTY_SHA=7a614ebeb2fc9c6c542cc973b0575c0a8515173d LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 17 Jun 2026 22:06:21 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 17 Jun 2026 22:06:21 GMT
USER 1001
# Wed, 17 Jun 2026 22:06:21 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 17 Jun 2026 22:06:21 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 17 Jun 2026 22:06:21 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 17 Jun 2026 22:42:23 GMT
ARG VERBOSE=false
# Wed, 17 Jun 2026 22:42:23 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 17 Jun 2026 22:42:23 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Wed, 17 Jun 2026 22:42:23 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Wed, 17 Jun 2026 22:42:43 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2745aaec1f27f3ce64535cccd00ad568bf55bbe89df5b402c9d4e75e445ab0`  
		Last Modified: Fri, 15 May 2026 21:19:47 GMT  
		Size: 1.5 MB (1450194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3014eee4fc2ffbbc50d2bff5a7c48962701a29f1d1d64ab5d45495f3ddb8a16c`  
		Last Modified: Fri, 15 May 2026 21:19:51 GMT  
		Size: 136.2 MB (136233781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cf29e24caeaa7aa4608c5367c6cd671e560d123a63f19fcfcbe488e6b527f6`  
		Last Modified: Wed, 17 Jun 2026 22:06:31 GMT  
		Size: 113.8 KB (113813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8284cfef123d25523b8a3888abaa8b7c5af8b25d56753e0111ec3fd8cb54eeeb`  
		Last Modified: Wed, 17 Jun 2026 22:06:31 GMT  
		Size: 18.5 MB (18521474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee542cef92b85192b65b8f163f1a8e0584cbf04b33f936670510b28f5b7586c`  
		Last Modified: Wed, 17 Jun 2026 22:06:31 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bea7f71e4d716da073d84ce3ae3368cc5dd14e83b9afe2247d544d028f2e95`  
		Last Modified: Wed, 17 Jun 2026 22:06:31 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a2cb30c79913b41a8b721df55bf8d79aecd3ac146f563f197a71a1239daa9d`  
		Last Modified: Wed, 17 Jun 2026 22:06:32 GMT  
		Size: 14.2 KB (14190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3dcac5f6d9ccec31c77197b166676542dfacb5f1e1037304c588d8aeed7dc26`  
		Last Modified: Wed, 17 Jun 2026 22:06:32 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45efa32fba93cdc8e13af7f29137b0bea4706b1545c17624fcc2a0ebd7dad6c3`  
		Last Modified: Wed, 17 Jun 2026 22:06:33 GMT  
		Size: 15.1 KB (15066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1b74f14b6e18ae7cca28ac2edb497e0b8358831682a849de4e26f382da1ce4`  
		Last Modified: Wed, 17 Jun 2026 22:06:33 GMT  
		Size: 5.8 MB (5806264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dacbca49985572cb4f70a3beacc6de6201b98e1c1cd43603acb9ad4dd43e7fb`  
		Last Modified: Wed, 17 Jun 2026 22:43:18 GMT  
		Size: 387.4 MB (387383133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6a0af4e29264b58b04b238ad250fde310198d14da480dad07f123e7acf2471`  
		Last Modified: Wed, 17 Jun 2026 22:43:11 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e296155cef4f7478cf9fbb14dbb3e82e74031571afbb973f9d03e1bc650e9caf`  
		Last Modified: Wed, 17 Jun 2026 22:43:12 GMT  
		Size: 14.8 MB (14828056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:a48f0fd65d4da592f1093e4b115d519d5f7dacb2c97c57b7e6922a0405069139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4436592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c749885f3fdd0fad69cd25436599283b4b05eaafc94afcc666e66588a463f2e`

```dockerfile
```

-	Layers:
	-	`sha256:101879ff32daedbd80cd43a874d3a8755ab8def889f0d74a5602194855264081`  
		Last Modified: Wed, 17 Jun 2026 22:43:11 GMT  
		Size: 4.4 MB (4417497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8c0d35f7d8a6671d6517c1d6e7899d4941e381fbfa41b0c529608d1b36ca9e4`  
		Last Modified: Wed, 17 Jun 2026 22:43:11 GMT  
		Size: 19.1 KB (19095 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:cfc58ad30ee83673f9711dde71b3bd92bc7320b5d43c6523ddb9cd9a5cc319a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.6 MB (599588075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7ed01469b906fc624297a2f66f5f12febca0d5a693a7409298ac67409b05fa`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 09 May 2026 04:51:05 GMT
ARG RELEASE
# Sat, 09 May 2026 04:51:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:51:05 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:51:11 GMT
ADD file:bd6823713e9d7c2f4ea7ca1d6d549e2bed56e8ce1fc6f98e14f6eb3a3371ebfa in / 
# Sat, 09 May 2026 04:51:12 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:28:40 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 15 May 2026 21:28:40 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:28:40 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 15 May 2026 21:29:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f848631ac7f7e61aa26d1e648bc7a96e97da64c33cbc4f76627ea3b367c9a085';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='9fad050b730cf070b341e5f7b5353c6cdd0a5a6f2d2b150678bfdff1f94f2637';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c844b329e2161a7d0c5810b30085b5deeec28b911844220cb3b930f860b10884';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 15 May 2026 21:29:20 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 29 May 2026 23:21:46 GMT
USER root
# Fri, 29 May 2026 23:21:46 GMT
ARG VERBOSE=false
# Fri, 29 May 2026 23:21:46 GMT
ARG OPENJ9_SCC=true
# Fri, 29 May 2026 23:21:46 GMT
ARG LIBERTY_VERSION=26.0.0.5
# Fri, 29 May 2026 23:21:46 GMT
ARG LIBERTY_BUILD_LABEL=cl260520260430-1602
# Fri, 29 May 2026 23:21:46 GMT
ARG LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf
# Fri, 29 May 2026 23:21:46 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.5 org.opencontainers.image.revision=cl260520260430-1602 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.5 com.ibm.websphere.liberty.version=26.0.0.5
# Fri, 29 May 2026 23:21:46 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Fri, 29 May 2026 23:21:46 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.5 BuildLabel=cl260520260430-1602
# Fri, 29 May 2026 23:21:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 29 May 2026 23:21:46 GMT
ARG LIBERTY_URL
# Fri, 29 May 2026 23:21:46 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 29 May 2026 23:22:00 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 May 2026 23:22:00 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 29 May 2026 23:22:01 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 29 May 2026 23:22:01 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Fri, 29 May 2026 23:22:02 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Fri, 29 May 2026 23:22:02 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Fri, 29 May 2026 23:22:03 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 29 May 2026 23:22:12 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Fri, 29 May 2026 23:22:12 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 29 May 2026 23:22:12 GMT
USER 1001
# Fri, 29 May 2026 23:22:12 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 29 May 2026 23:22:12 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 29 May 2026 23:22:12 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Sat, 30 May 2026 02:33:05 GMT
ARG VERBOSE=false
# Sat, 30 May 2026 02:33:05 GMT
ARG REPOSITORIES_PROPERTIES=
# Sat, 30 May 2026 02:33:05 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Sat, 30 May 2026 02:33:05 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Sat, 30 May 2026 02:33:47 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:6970bf2b5ef1698cb51975b1a652f6511f8fd9f88ae7b247e3ee32591d975e63`  
		Last Modified: Sat, 09 May 2026 05:25:11 GMT  
		Size: 34.6 MB (34646720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1d9502a29e5927b7c6acfcd4d85b9058b023b826aa21b29033ebc1aa0f839a`  
		Last Modified: Fri, 15 May 2026 21:29:48 GMT  
		Size: 1.5 MB (1536350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ea9fcf12bfe40ab2713b4d79b8765e828a093bdce0e8e57c4039e0ba7d83f7`  
		Last Modified: Fri, 15 May 2026 21:29:52 GMT  
		Size: 137.1 MB (137149789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5694362eb8bc0725bceb6ccbd77b34d9059cff07fe497b2d6dd7799d1e8cb28`  
		Last Modified: Fri, 29 May 2026 23:22:31 GMT  
		Size: 118.2 KB (118229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099a6ecb7d26c695cfae266fc3137f6206958ff87de159e898726fb5f984100d`  
		Last Modified: Fri, 29 May 2026 23:22:32 GMT  
		Size: 18.1 MB (18110042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17d2ef544989ded3e892cefa4996c5c26b6dff96275bd7185a2d15882ed7938`  
		Last Modified: Fri, 29 May 2026 23:22:31 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e693268d3ebd3d8185f7f25d2e7dcd29c2ddb0b229cc88aa2ffefdc2552657`  
		Last Modified: Fri, 29 May 2026 23:22:31 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29df268e3fad08535ad6792515947e4da1fea928e988af8bae5997734c85ad5a`  
		Last Modified: Fri, 29 May 2026 23:22:32 GMT  
		Size: 14.2 KB (14189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1098c901e12cc29660d9a728e9b788e421a52b55c9796b44e1385bab6d3ba3f0`  
		Last Modified: Fri, 29 May 2026 23:22:32 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76bb1d9fabfde9867e650c3f9ce5db0e2994148d53148aae7cb6d763cf3f9acb`  
		Last Modified: Fri, 29 May 2026 23:22:32 GMT  
		Size: 15.1 KB (15079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e9256d54056e368cce0bb29b5936d46d5fe2f6fbe74c47ad0cf97e2626167f`  
		Last Modified: Fri, 29 May 2026 23:22:33 GMT  
		Size: 5.4 MB (5407237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb5f50d995f84c0c1ff148cb82ef482c6601a1aaff7af5fb1f2851b6ba087b8`  
		Last Modified: Sat, 30 May 2026 02:34:52 GMT  
		Size: 389.7 MB (389675039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2450c437e8b6efe6d01830bc8f6cf2ed4792c9308c84c0ddf5efc1ba24d5a9f`  
		Last Modified: Sat, 30 May 2026 02:34:44 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab59620c7a8fd3b955cbee2105302574126ed2a3bcbda1bf4c78d50b1a7dad77`  
		Last Modified: Sat, 30 May 2026 02:34:44 GMT  
		Size: 12.9 MB (12912095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:3d6f0174a9185f64d49885868d7a769fc202306f1651eb095c3841c38a397a1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4436658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2250e6a561edebc27d4df3cb31c0d2b777f6bc9f778b2bc8093ba05e461436bd`

```dockerfile
```

-	Layers:
	-	`sha256:2fcab25cd1020b411a3b5b3cbd8ac5d2c54f93e7da93e88b0916e7fd83dcecb5`  
		Last Modified: Sat, 30 May 2026 02:34:44 GMT  
		Size: 4.4 MB (4417523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:451182645379b4dfea2bedac76ef84c426f333b590d0dd39fd421a7042c78bbe`  
		Last Modified: Sat, 30 May 2026 02:34:43 GMT  
		Size: 19.1 KB (19135 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:d978fe364876aec22e8f8e4310d80132ab2d8a57184d344651ddf448ec3854af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.6 MB (591606788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10df2b3b44963936220bc348bc8adadcc72e0376ad63be1b7cb25ae25c816ca1`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 09 May 2026 04:50:49 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:51 GMT
ADD file:17ca3274b34edf79b2d4401a24984fb8dc339a8298f0e3703af025f51b67336b in / 
# Sat, 09 May 2026 04:50:51 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:25:40 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 15 May 2026 21:25:40 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:25:40 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 15 May 2026 21:26:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f848631ac7f7e61aa26d1e648bc7a96e97da64c33cbc4f76627ea3b367c9a085';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='9fad050b730cf070b341e5f7b5353c6cdd0a5a6f2d2b150678bfdff1f94f2637';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c844b329e2161a7d0c5810b30085b5deeec28b911844220cb3b930f860b10884';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 15 May 2026 21:26:26 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 17 Jun 2026 22:07:29 GMT
USER root
# Wed, 17 Jun 2026 22:07:29 GMT
ARG VERBOSE=false
# Wed, 17 Jun 2026 22:07:29 GMT
ARG OPENJ9_SCC=true
# Wed, 17 Jun 2026 22:07:29 GMT
ARG LIBERTY_VERSION=26.0.0.6
# Wed, 17 Jun 2026 22:07:29 GMT
ARG LIBERTY_BUILD_LABEL=cl260620260531-0302
# Wed, 17 Jun 2026 22:07:29 GMT
ARG LIBERTY_SHA=7a614ebeb2fc9c6c542cc973b0575c0a8515173d
# Wed, 17 Jun 2026 22:07:29 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.6 org.opencontainers.image.revision=cl260620260531-0302 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.6 com.ibm.websphere.liberty.version=26.0.0.6
# Wed, 17 Jun 2026 22:07:29 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Wed, 17 Jun 2026 22:07:29 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.6 BuildLabel=cl260620260531-0302
# Wed, 17 Jun 2026 22:07:29 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.6 LIBERTY_BUILD_LABEL=cl260620260531-0302 LIBERTY_SHA=7a614ebeb2fc9c6c542cc973b0575c0a8515173d
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 17 Jun 2026 22:07:29 GMT
ARG LIBERTY_URL
# Wed, 17 Jun 2026 22:07:29 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 17 Jun 2026 22:07:38 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.6 LIBERTY_BUILD_LABEL=cl260620260531-0302 LIBERTY_SHA=7a614ebeb2fc9c6c542cc973b0575c0a8515173d LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jun 2026 22:07:38 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 17 Jun 2026 22:07:39 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.6 LIBERTY_BUILD_LABEL=cl260620260531-0302 LIBERTY_SHA=7a614ebeb2fc9c6c542cc973b0575c0a8515173d LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 17 Jun 2026 22:07:39 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 17 Jun 2026 22:07:39 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 17 Jun 2026 22:07:39 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 17 Jun 2026 22:07:39 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.6 LIBERTY_BUILD_LABEL=cl260620260531-0302 LIBERTY_SHA=7a614ebeb2fc9c6c542cc973b0575c0a8515173d LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Wed, 17 Jun 2026 22:07:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.6 LIBERTY_BUILD_LABEL=cl260620260531-0302 LIBERTY_SHA=7a614ebeb2fc9c6c542cc973b0575c0a8515173d LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 17 Jun 2026 22:07:46 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 17 Jun 2026 22:07:46 GMT
USER 1001
# Wed, 17 Jun 2026 22:07:46 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 17 Jun 2026 22:07:46 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 17 Jun 2026 22:07:46 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 17 Jun 2026 22:44:45 GMT
ARG VERBOSE=false
# Wed, 17 Jun 2026 22:44:45 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 17 Jun 2026 22:44:45 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Wed, 17 Jun 2026 22:44:45 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Wed, 17 Jun 2026 22:45:08 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:c8acb84faa73cc102915433858f425bdd6749804de64fd2e27d5f491f005a91b`  
		Last Modified: Sat, 09 May 2026 05:25:25 GMT  
		Size: 28.2 MB (28202305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1931cfb90bc60ae24d6e589e0cba39f54353e12baecae083fef9e1dab4874f`  
		Last Modified: Fri, 15 May 2026 21:27:00 GMT  
		Size: 1.5 MB (1455939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d580608bb6b95870f23bd08c8ab108f7f19dd838c173a89887d6c80bba5b67a`  
		Last Modified: Fri, 15 May 2026 21:27:03 GMT  
		Size: 134.6 MB (134620694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35604d085cbcbe7e1420e0bd019d9b4f675e216521253555b4679dafbbe434c`  
		Last Modified: Wed, 17 Jun 2026 22:08:00 GMT  
		Size: 114.8 KB (114817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231b4dff5227f239dc122d8256c5c6494a3bcf4b63567d1b470552e950863ff5`  
		Last Modified: Wed, 17 Jun 2026 22:08:00 GMT  
		Size: 18.5 MB (18521916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182b16819807898b96c8567b7dc1e0e6bc7c1b0f542d3dcd080b582e4b097832`  
		Last Modified: Wed, 17 Jun 2026 22:08:00 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db1120774611986efb4e117fd354c57e1383e9dad820c29b95dc97398c931d1`  
		Last Modified: Wed, 17 Jun 2026 22:08:00 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd014d90d8b3efdc020223c7b573ddf9d93a0577be0e7b6d2d4e0388c8bdd40`  
		Last Modified: Wed, 17 Jun 2026 22:08:01 GMT  
		Size: 14.2 KB (14184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5aba972db799f50698b67c7eed4d24bfef992fdce61206180bbe43d19d41b7`  
		Last Modified: Wed, 17 Jun 2026 22:08:01 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7d460599535585bb16d12d8412bc29525a98756a2a0672715be4a72b616538`  
		Last Modified: Wed, 17 Jun 2026 22:08:01 GMT  
		Size: 15.1 KB (15066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b446a32f6e015c4ac6bf29c74df235f6fc37e73c27dec86047874ba6352323a6`  
		Last Modified: Wed, 17 Jun 2026 22:08:02 GMT  
		Size: 6.1 MB (6120281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74bf48cf9d26be872ebff0977a4972caa123b63e12e539353ce91b671d18ab86`  
		Last Modified: Wed, 17 Jun 2026 22:45:58 GMT  
		Size: 387.4 MB (387382695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e3c7ff0a1e1b55ce0856e88819a7d132eb18eeca46b1d6e6ffc03cd3c53e2e`  
		Last Modified: Wed, 17 Jun 2026 22:45:51 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53770bbe941f08e2478e62c812654520e2c5e3f0671f894c8acf1a80cf208421`  
		Last Modified: Wed, 17 Jun 2026 22:45:52 GMT  
		Size: 15.2 MB (15155590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:7ddc5226c9b5aa7f5d3136e8faa08226e30861cdaa8418557ffc814de7f61ede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4435339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c55875688541a61eb1f16d12d5ceeb1f0b298d076699987bfa173bd9cdb65ad`

```dockerfile
```

-	Layers:
	-	`sha256:d616e76c451c2a7358958e89de9abdb8f63d24b8eef8c2d877d82d4903b6c922`  
		Last Modified: Wed, 17 Jun 2026 22:45:51 GMT  
		Size: 4.4 MB (4416244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:774ec1e05c7b4bd78bd7a79e102fe8705a8faa1b12b2e1b5ba4fee22b8e26950`  
		Last Modified: Wed, 17 Jun 2026 22:45:51 GMT  
		Size: 19.1 KB (19095 bytes)  
		MIME: application/vnd.in-toto+json
