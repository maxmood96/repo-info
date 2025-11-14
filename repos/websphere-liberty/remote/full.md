## `websphere-liberty:full`

```console
$ docker pull websphere-liberty@sha256:62b1e82a9335902153f8f2ceacbcc915a9749c143c104c0d02ee5b0653299511
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
$ docker pull websphere-liberty@sha256:1d5f325a774d90e1fb39fb6f9c5f1f745d72aae91f34c64edb519e6317ccaed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.8 MB (571767684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca19b5e0cb8976b10df36779a191400467103ac919bb6f6249d483646b657450`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:27:50 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 13 Nov 2025 23:27:50 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:27:50 GMT
ENV JAVA_VERSION=8.0.8.55
# Thu, 13 Nov 2025 23:27:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a6095b036bda7d4344607de6b91823d7704d2bf8b1c4c4cb4b01aa87e9ac0e1f';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a1d3984e2f6971117f950bcc6ac88ea5e4772e687b41af95ceb569cc47b82c73';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='37d9a6cbdd5ce45605d8b05843770151f857efc1280071bdc293cab4dc967c6d';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 13 Nov 2025 23:27:57 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 14 Nov 2025 00:47:00 GMT
USER root
# Fri, 14 Nov 2025 00:47:00 GMT
ARG VERBOSE=false
# Fri, 14 Nov 2025 00:47:00 GMT
ARG OPENJ9_SCC=true
# Fri, 14 Nov 2025 00:47:00 GMT
ARG LIBERTY_VERSION=25.0.0.11
# Fri, 14 Nov 2025 00:47:00 GMT
ARG LIBERTY_BUILD_LABEL=cl251120251020-0302
# Fri, 14 Nov 2025 00:47:00 GMT
ARG LIBERTY_SHA=698f922ad71f49cf40936e3b0313fc2e86a7a4c8
# Fri, 14 Nov 2025 00:47:00 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.11 org.opencontainers.image.revision=cl251120251020-0302 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.11 com.ibm.websphere.liberty.version=25.0.0.11
# Fri, 14 Nov 2025 00:47:00 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Fri, 14 Nov 2025 00:47:00 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.11 BuildLabel=cl251120251020-0302
# Fri, 14 Nov 2025 00:47:00 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.11 LIBERTY_BUILD_LABEL=cl251120251020-0302 LIBERTY_SHA=698f922ad71f49cf40936e3b0313fc2e86a7a4c8
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 00:47:00 GMT
ARG LIBERTY_URL
# Fri, 14 Nov 2025 00:47:00 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 14 Nov 2025 00:47:09 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.11 LIBERTY_BUILD_LABEL=cl251120251020-0302 LIBERTY_SHA=698f922ad71f49cf40936e3b0313fc2e86a7a4c8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:47:09 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 14 Nov 2025 00:47:10 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.11 LIBERTY_BUILD_LABEL=cl251120251020-0302 LIBERTY_SHA=698f922ad71f49cf40936e3b0313fc2e86a7a4c8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 14 Nov 2025 00:47:10 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Fri, 14 Nov 2025 00:47:10 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Fri, 14 Nov 2025 00:47:10 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Fri, 14 Nov 2025 00:47:10 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.11 LIBERTY_BUILD_LABEL=cl251120251020-0302 LIBERTY_SHA=698f922ad71f49cf40936e3b0313fc2e86a7a4c8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 14 Nov 2025 00:47:15 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.11 LIBERTY_BUILD_LABEL=cl251120251020-0302 LIBERTY_SHA=698f922ad71f49cf40936e3b0313fc2e86a7a4c8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Fri, 14 Nov 2025 00:47:15 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 14 Nov 2025 00:47:15 GMT
USER 1001
# Fri, 14 Nov 2025 00:47:15 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 14 Nov 2025 00:47:15 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 14 Nov 2025 00:47:15 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 14 Nov 2025 01:37:18 GMT
ARG VERBOSE=false
# Fri, 14 Nov 2025 01:37:18 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 14 Nov 2025 01:37:18 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Fri, 14 Nov 2025 01:37:18 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Fri, 14 Nov 2025 01:37:40 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a5a071dc71ec50d9e6bf289bce551e32f53569352f578e0fc2333f145b9d3d`  
		Last Modified: Thu, 13 Nov 2025 23:28:20 GMT  
		Size: 1.5 MB (1450101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a24fa2c8172ddda044d8b4efc0b0e749b7b1f9ef2ea15c077e9c4556dd0ef1`  
		Last Modified: Fri, 14 Nov 2025 00:46:50 GMT  
		Size: 135.5 MB (135541139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf23c995404938632a3a71c19ec72e0f72227e697df24dbc6242fadad1a445a0`  
		Last Modified: Fri, 14 Nov 2025 00:47:32 GMT  
		Size: 113.8 KB (113758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963f05205773e24d7d63b5dc8943792bc2a15c17dc0b537a17f993d87aa56ac4`  
		Last Modified: Fri, 14 Nov 2025 00:47:33 GMT  
		Size: 17.7 MB (17733855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95b4407107b00ef1951cbf42ad8f2da265ed7784075dcfb893116d5a9ce17a8`  
		Last Modified: Fri, 14 Nov 2025 00:47:32 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e5694e0fb9a3737e40766ac827231bf6deb0f0131a391612827dbf1647ba3b`  
		Last Modified: Fri, 14 Nov 2025 00:47:32 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9fba074e5492644ee205b636c8e12820a0097cfa5cd3be408da62067d124f4`  
		Last Modified: Fri, 14 Nov 2025 00:47:31 GMT  
		Size: 14.1 KB (14120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673abfb1ddf47d5ba3674778565c72b29d75531dede2fbdf31db91b44a7fb5ed`  
		Last Modified: Fri, 14 Nov 2025 00:47:32 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8348dfdee6b19e4d646ab6cdea74bed43e4e7b4e8cf238fa6c0a63b0c0bd901d`  
		Last Modified: Fri, 14 Nov 2025 00:47:33 GMT  
		Size: 15.0 KB (14998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e271c4611626928e8109b629473f023320cdd2e3f73ee0c4a6296500bcf2c69d`  
		Last Modified: Fri, 14 Nov 2025 00:47:33 GMT  
		Size: 5.8 MB (5766246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9659ad196fa9a244f121bb0597bd55c644e8cff24ba383a513f0c2779f3ceb33`  
		Last Modified: Fri, 14 Nov 2025 06:12:38 GMT  
		Size: 365.5 MB (365485395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6227e555ee37d7b592bb4c21e9e3ed5f0a2fb26e12d4a8bf479e3fe2727eac4`  
		Last Modified: Fri, 14 Nov 2025 01:38:28 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54513415118f6573bf7a181fa886e677ab7061d87fdc3fc04321592a7a99cba`  
		Last Modified: Fri, 14 Nov 2025 01:38:30 GMT  
		Size: 16.1 MB (16107971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:900341142ccd82d8bd0bf251b434ffa27f9dfc58e7c9842b6c1dfe24dcde7377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb6cbbc6f081c3c962951c8f9635638c24f031dd52cded9bb818e1fb20aeb9e`

```dockerfile
```

-	Layers:
	-	`sha256:586010d2dec50382bf46482ce8cf962b79fa1eb5af9cd7a0930d1900628346ab`  
		Last Modified: Fri, 14 Nov 2025 04:24:53 GMT  
		Size: 4.4 MB (4359455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6f2d38debc1c64edd17ad9b25e5770fdd8432e9c3051b1b7570ebd49376460`  
		Last Modified: Fri, 14 Nov 2025 04:24:54 GMT  
		Size: 19.1 KB (19093 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:3c7d659e4b22c20a2c2f8791c94794211254d95cc9a1617862acb03b2ae70707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.7 MB (574738858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:524a70d0355772b7e4212a8d1906ea6a122c1d6b0b704ad333beb30f21308a86`
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
# Wed, 05 Nov 2025 09:29:20 GMT
USER root
# Wed, 05 Nov 2025 09:29:20 GMT
ARG VERBOSE=false
# Wed, 05 Nov 2025 09:29:20 GMT
ARG OPENJ9_SCC=true
# Wed, 05 Nov 2025 09:29:20 GMT
ARG LIBERTY_VERSION=25.0.0.11
# Wed, 05 Nov 2025 09:29:20 GMT
ARG LIBERTY_BUILD_LABEL=cl251120251020-0302
# Wed, 05 Nov 2025 09:29:20 GMT
ARG LIBERTY_SHA=698f922ad71f49cf40936e3b0313fc2e86a7a4c8
# Wed, 05 Nov 2025 09:29:20 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.11 org.opencontainers.image.revision=cl251120251020-0302 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.11 com.ibm.websphere.liberty.version=25.0.0.11
# Wed, 05 Nov 2025 09:29:20 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Wed, 05 Nov 2025 09:29:20 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.11 BuildLabel=cl251120251020-0302
# Wed, 05 Nov 2025 09:29:20 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.11 LIBERTY_BUILD_LABEL=cl251120251020-0302 LIBERTY_SHA=698f922ad71f49cf40936e3b0313fc2e86a7a4c8
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 05 Nov 2025 09:29:20 GMT
ARG LIBERTY_URL
# Wed, 05 Nov 2025 09:29:20 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 05 Nov 2025 09:29:37 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.11 LIBERTY_BUILD_LABEL=cl251120251020-0302 LIBERTY_SHA=698f922ad71f49cf40936e3b0313fc2e86a7a4c8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 09:29:37 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 05 Nov 2025 09:29:40 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.11 LIBERTY_BUILD_LABEL=cl251120251020-0302 LIBERTY_SHA=698f922ad71f49cf40936e3b0313fc2e86a7a4c8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 05 Nov 2025 09:29:40 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 05 Nov 2025 09:29:41 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 05 Nov 2025 09:29:41 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 05 Nov 2025 09:29:42 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.11 LIBERTY_BUILD_LABEL=cl251120251020-0302 LIBERTY_SHA=698f922ad71f49cf40936e3b0313fc2e86a7a4c8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Wed, 05 Nov 2025 09:29:54 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.11 LIBERTY_BUILD_LABEL=cl251120251020-0302 LIBERTY_SHA=698f922ad71f49cf40936e3b0313fc2e86a7a4c8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 05 Nov 2025 09:29:54 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 05 Nov 2025 09:29:54 GMT
USER 1001
# Wed, 05 Nov 2025 09:29:54 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 05 Nov 2025 09:29:54 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 05 Nov 2025 09:29:54 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 05 Nov 2025 10:36:14 GMT
ARG VERBOSE=false
# Wed, 05 Nov 2025 10:36:14 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 05 Nov 2025 10:36:14 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Wed, 05 Nov 2025 10:36:14 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Wed, 05 Nov 2025 10:36:55 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
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
	-	`sha256:7eb4aa2187a7bfe8d5c0d2aee4ae69dac5265f995fd287152bb71753f6ef2f8e`  
		Last Modified: Wed, 05 Nov 2025 09:30:34 GMT  
		Size: 118.1 KB (118096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6861a526b3be9c95ab09291c9072ffcaadd0aeb5c859ef850de751ad155d7f85`  
		Last Modified: Wed, 05 Nov 2025 09:30:36 GMT  
		Size: 17.7 MB (17734170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:879326dccf2136db10309a343effced97af76bb608759d67e06e6209cd2b2bb0`  
		Last Modified: Wed, 05 Nov 2025 09:30:34 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da628722adad763f44d5099bf6c2a8452751657929bdcde997e08ef93992b1f`  
		Last Modified: Wed, 05 Nov 2025 09:30:34 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245fe608d68581355e86733a5b128567aef038ffd10324acf73344f85fbbf766`  
		Last Modified: Wed, 05 Nov 2025 09:30:34 GMT  
		Size: 14.1 KB (14120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c01b836dd55eacfc9a1b9e1cf20f87022b5949a191fdeac29e01447ae9e3ae`  
		Last Modified: Wed, 05 Nov 2025 09:30:34 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3107cfd2d676da3100e367e04d5d1beff5ac84a1e63f2d81366ef33694faedf1`  
		Last Modified: Wed, 05 Nov 2025 09:30:34 GMT  
		Size: 15.0 KB (15000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3bbe01ed71ecf1de630a9d1512c26045c794fd52d00bbe0eae0f3b8308f733c`  
		Last Modified: Wed, 05 Nov 2025 09:30:35 GMT  
		Size: 5.5 MB (5525721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ae5a4b0ae18f76f61146f626e7b7c43eafd226a08d815dab8fd15ccbb04ab2`  
		Last Modified: Wed, 05 Nov 2025 13:54:01 GMT  
		Size: 365.5 MB (365479723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d7d05d596352260f422e710f1d1afc5be4f93db2e10fd26e8b847727edccfe`  
		Last Modified: Wed, 05 Nov 2025 10:38:14 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bc0de69fc9c384e0c57a99274546f4df23d9c0191e04806b56e4abbfe66d86`  
		Last Modified: Wed, 05 Nov 2025 10:38:16 GMT  
		Size: 13.4 MB (13378786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:6e618a6d29d452b879941e5ed4fff1539ba9165f16c4e1ad1816d4295d3ab4c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c99329433338a59772a109d9028080622c5f192d661a8a3477c9f2c654668552`

```dockerfile
```

-	Layers:
	-	`sha256:663dbd87aa098dbde72c313fcb751143548609f2b6d40a898a0528240e372268`  
		Last Modified: Wed, 05 Nov 2025 13:21:51 GMT  
		Size: 4.4 MB (4362730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2aa629fa2e0cdf0a85a85f07ae044587259d10a16a022cd2327eac2e69a2028e`  
		Last Modified: Wed, 05 Nov 2025 13:21:53 GMT  
		Size: 19.1 KB (19134 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:71f2654d0861152069c5c5975ab32a042fa297e59e1f53749827eed8e731a54a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.6 MB (567580502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51caae6af6ee261495265f7ff3ca520e5618ddca8d1261575da078b9a39211b7`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:42 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:44 GMT
ADD file:3d940f8d55eafd405ad4e9fa11689b18e385411a264e560df2a7b1b1fd1c45ea in / 
# Mon, 13 Oct 2025 17:23:44 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:33 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 13 Nov 2025 23:21:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:33 GMT
ENV JAVA_VERSION=8.0.8.55
# Thu, 13 Nov 2025 23:21:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a6095b036bda7d4344607de6b91823d7704d2bf8b1c4c4cb4b01aa87e9ac0e1f';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a1d3984e2f6971117f950bcc6ac88ea5e4772e687b41af95ceb569cc47b82c73';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='37d9a6cbdd5ce45605d8b05843770151f857efc1280071bdc293cab4dc967c6d';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 13 Nov 2025 23:21:45 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 14 Nov 2025 00:45:25 GMT
USER root
# Fri, 14 Nov 2025 00:45:25 GMT
ARG VERBOSE=false
# Fri, 14 Nov 2025 00:45:25 GMT
ARG OPENJ9_SCC=true
# Fri, 14 Nov 2025 00:45:25 GMT
ARG LIBERTY_VERSION=25.0.0.11
# Fri, 14 Nov 2025 00:45:25 GMT
ARG LIBERTY_BUILD_LABEL=cl251120251020-0302
# Fri, 14 Nov 2025 00:45:25 GMT
ARG LIBERTY_SHA=698f922ad71f49cf40936e3b0313fc2e86a7a4c8
# Fri, 14 Nov 2025 00:45:25 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.11 org.opencontainers.image.revision=cl251120251020-0302 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.11 com.ibm.websphere.liberty.version=25.0.0.11
# Fri, 14 Nov 2025 00:45:25 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Fri, 14 Nov 2025 00:45:25 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.11 BuildLabel=cl251120251020-0302
# Fri, 14 Nov 2025 00:45:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.11 LIBERTY_BUILD_LABEL=cl251120251020-0302 LIBERTY_SHA=698f922ad71f49cf40936e3b0313fc2e86a7a4c8
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 00:45:25 GMT
ARG LIBERTY_URL
# Fri, 14 Nov 2025 00:45:25 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 14 Nov 2025 00:45:31 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.11 LIBERTY_BUILD_LABEL=cl251120251020-0302 LIBERTY_SHA=698f922ad71f49cf40936e3b0313fc2e86a7a4c8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:45:31 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 14 Nov 2025 00:45:31 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.11 LIBERTY_BUILD_LABEL=cl251120251020-0302 LIBERTY_SHA=698f922ad71f49cf40936e3b0313fc2e86a7a4c8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 14 Nov 2025 00:45:31 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Fri, 14 Nov 2025 00:45:31 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Fri, 14 Nov 2025 00:45:31 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Fri, 14 Nov 2025 00:45:32 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.11 LIBERTY_BUILD_LABEL=cl251120251020-0302 LIBERTY_SHA=698f922ad71f49cf40936e3b0313fc2e86a7a4c8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 14 Nov 2025 00:45:37 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.11 LIBERTY_BUILD_LABEL=cl251120251020-0302 LIBERTY_SHA=698f922ad71f49cf40936e3b0313fc2e86a7a4c8 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Fri, 14 Nov 2025 00:45:37 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 14 Nov 2025 00:45:37 GMT
USER 1001
# Fri, 14 Nov 2025 00:45:37 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 14 Nov 2025 00:45:37 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 14 Nov 2025 00:45:37 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 14 Nov 2025 02:39:08 GMT
ARG VERBOSE=false
# Fri, 14 Nov 2025 02:39:08 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 14 Nov 2025 02:39:08 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Fri, 14 Nov 2025 02:39:08 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Fri, 14 Nov 2025 02:39:33 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:d15824160d0d57e05338a0838871eb3f72224cf5de518ea6af54ba25e7e9c4da`  
		Last Modified: Thu, 13 Nov 2025 23:02:52 GMT  
		Size: 28.0 MB (28003285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9a9678ab189281593619203e2450fdcbd36a8625ad07efac390df083e4d257`  
		Last Modified: Thu, 13 Nov 2025 23:22:14 GMT  
		Size: 1.5 MB (1455765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24054275a262fe9d62e2d7392bd56dbbe9b0fb90ae5d7d3ad2c3d805bf38e31`  
		Last Modified: Fri, 14 Nov 2025 00:45:19 GMT  
		Size: 133.0 MB (132950461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a4480f8b60b6133789eabf6a0ff9c38c2b890c09a4a0a0211186fb977ce7ea`  
		Last Modified: Fri, 14 Nov 2025 00:46:01 GMT  
		Size: 114.6 KB (114620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1967529377b950a35b4f42997e3ef61f423b31de7755895dfc2b9c98a0b3b2`  
		Last Modified: Fri, 14 Nov 2025 00:46:03 GMT  
		Size: 17.7 MB (17733704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cdafd68577c7bccc0ecc0e71a48aa19e01c71ef73bf61894544bc296f8f6e5`  
		Last Modified: Fri, 14 Nov 2025 00:46:01 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c5537dc5f848ad548435b15597bb5446ff4491b00bfba0e1d251dc8e2612ff`  
		Last Modified: Fri, 14 Nov 2025 00:46:01 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c65dcabf57af9afd5d58afe4e2ac9d3b0b84042f7349b3da726bd6e80917791`  
		Last Modified: Fri, 14 Nov 2025 00:46:02 GMT  
		Size: 14.1 KB (14122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ca9059c91d7abd63ae52d5d4355702c464bd56d3be46ad46c298264eec7a29`  
		Last Modified: Fri, 14 Nov 2025 00:46:01 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267ffa2621a939e801159c68a35456764cef66c3a1f999a1341ac1ee22bc3065`  
		Last Modified: Fri, 14 Nov 2025 00:46:01 GMT  
		Size: 15.0 KB (14996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec94c1ede72d6d51123aaa9749aad14f70a6070856818dbaac730a8e42b0e0cb`  
		Last Modified: Fri, 14 Nov 2025 00:46:02 GMT  
		Size: 6.0 MB (6018074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600f1956f567ff0654dfd72bee4a85a6c0cfe9d997480d4e3aee06965e521fef`  
		Last Modified: Fri, 14 Nov 2025 06:03:19 GMT  
		Size: 365.5 MB (365484735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6245d4e944f0e0857b2f4f7571335e72a0b52dead13c50ee4b151feb4d48ed1`  
		Last Modified: Fri, 14 Nov 2025 02:40:20 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f5cae0251f2bd9e9926e3cd7ed7782cbf6abbdf306dc522f1dd094f6555909`  
		Last Modified: Fri, 14 Nov 2025 02:40:22 GMT  
		Size: 15.8 MB (15787446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:d826892129b646aca3d921ea50e11f9fb810469960f7d9cca598bc18d67d79ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4377311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d96daba326d07a3e2701edba85cbab02860c1ed3feaf27afe632bac9d433d524`

```dockerfile
```

-	Layers:
	-	`sha256:db1ead2932875b0ea24aa9e4e5193a5fe2fc943a80aceb835c0cca9197868d59`  
		Last Modified: Fri, 14 Nov 2025 04:25:03 GMT  
		Size: 4.4 MB (4358216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19822c907659c2f43651de11fa496ce777ab03ae6bfe9dff147284e9e19f7f06`  
		Last Modified: Fri, 14 Nov 2025 04:25:04 GMT  
		Size: 19.1 KB (19095 bytes)  
		MIME: application/vnd.in-toto+json
