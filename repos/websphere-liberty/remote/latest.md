## `websphere-liberty:latest`

```console
$ docker pull websphere-liberty@sha256:8a3f663e4f0a3c17cae6839e339b5e10e27f013b407414a2618ba39bb195fe75
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
$ docker pull websphere-liberty@sha256:866c11216caf283b75f34bf2a91ce602ca4bbdcc27f4fedcbfd3af6ad706cac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.5 MB (571513801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf71bbcb5a8d76c99b06b33d1a71147096ad59eeb4f91b46b927191f0065e064`
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
# Fri, 31 Oct 2025 01:23:21 GMT
ARG VERBOSE=false
# Fri, 31 Oct 2025 01:23:21 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 31 Oct 2025 01:23:21 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Fri, 31 Oct 2025 01:23:21 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Fri, 31 Oct 2025 01:23:44 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
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
	-	`sha256:ea22acb8d1b01f140d2ce64019a39aefeac974cd589469dfd2ba1f8192252eae`  
		Last Modified: Fri, 31 Oct 2025 04:49:40 GMT  
		Size: 365.5 MB (365507003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac5cb0ebf96d4b8e5fdeb921efee197d7cceeda1702db19b792aae3a4539db1`  
		Last Modified: Fri, 31 Oct 2025 01:24:23 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da3c355b898acdad52af287bbd2be0fab02197d5785c3fa99e6c2e6148d6574`  
		Last Modified: Fri, 31 Oct 2025 01:24:25 GMT  
		Size: 15.9 MB (15937163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:latest` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:91aa1196c0592d2a52a53d31e1508021ee8d462c64cf1da76961d48cd9d36da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:680ef4735107c50d84ae2d33d71538b0a18984bc41e4c53f7586b8ae41aacb10`

```dockerfile
```

-	Layers:
	-	`sha256:4acf4c971c934a602c144b1305ccd84b2fb79e88cff1fa93536933fcc7ef6b61`  
		Last Modified: Fri, 31 Oct 2025 03:22:06 GMT  
		Size: 4.4 MB (4359455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae72d92996aa231d9152cf1f2b4b61bee0abeb3189db0d03c32c6317e11f9423`  
		Last Modified: Fri, 31 Oct 2025 03:22:09 GMT  
		Size: 19.1 KB (19095 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:latest` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:a2b6adcecd606889b39e2efe946410b820902f6a61e9a4ecd7bec25ae1cf24a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.7 MB (574676471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e2036ef0079210db4160205a6d60fefd1f87f79efafcd9a6ef4bf05784381c`
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
# Fri, 31 Oct 2025 03:05:19 GMT
ARG VERBOSE=false
# Fri, 31 Oct 2025 03:05:19 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 31 Oct 2025 03:05:19 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Fri, 31 Oct 2025 03:05:20 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Fri, 31 Oct 2025 03:06:07 GMT
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
	-	`sha256:a8e4bce9d4f0db5a6ed58ce62e66271f4601f83998e08995f92e6915cf9bd1d4`  
		Last Modified: Fri, 31 Oct 2025 03:07:24 GMT  
		Size: 365.5 MB (365507702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce5d09c6c7aaa2028889f43c4d30786f5ab410f67d36ae3e89b2d128f95cad1`  
		Last Modified: Fri, 31 Oct 2025 03:07:39 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd40f7c8bbbbddb3d73606f9c052d97ffcb8426e2dad6fc8d0bf70ae1b0f76b`  
		Last Modified: Fri, 31 Oct 2025 03:07:40 GMT  
		Size: 13.5 MB (13510148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:latest` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:7aa28e54920fc19f9990bf2d9bc074965c4160d369e27a107c5946090b07d3d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7d54b090f6aaf8a952be251c209a9cef609badb6d4ed619d4b68a1fefecf55`

```dockerfile
```

-	Layers:
	-	`sha256:35434849da1b8f9d84d12d6ca6f56391bddecf97d4ba776f94309e0f95736c56`  
		Last Modified: Fri, 31 Oct 2025 03:22:13 GMT  
		Size: 4.4 MB (4362730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cc68bc69f43f3c42b8416702244a8dcece9c5d93cf4885c98a83c248e0420e2`  
		Last Modified: Fri, 31 Oct 2025 03:22:14 GMT  
		Size: 19.1 KB (19135 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:latest` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:459111704292def8208771c1d5fe8b4df7f0640dc32665953cd387d8bd6247f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.8 MB (567770498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3515a9b99535d675454a30c2957f88945f3788382e595c5b20e839589b4e6e04`
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
# Fri, 31 Oct 2025 00:23:24 GMT
ARG VERBOSE=false
# Fri, 31 Oct 2025 00:23:24 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 31 Oct 2025 00:23:24 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Fri, 31 Oct 2025 00:23:24 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Fri, 31 Oct 2025 00:23:50 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
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
	-	`sha256:5c40cc17b72c4a535391535a7c3e6141cbcd15d5713946f7de14d471eb5877b5`  
		Last Modified: Fri, 31 Oct 2025 04:06:01 GMT  
		Size: 365.5 MB (365507378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6971aaffee6a6a2fcb8aa3a2bff1d7bfd6ee33c2c749446e4e132674f708f8`  
		Last Modified: Fri, 31 Oct 2025 00:24:57 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c2733b121a011ad08dbff8530d2b72b83edefbc8d6716ac588721c795de984`  
		Last Modified: Fri, 31 Oct 2025 00:24:58 GMT  
		Size: 16.0 MB (16020188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:latest` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:2f023e392dd6a2b7e0cd45a9f8e5a4b81afcc8e4831b787d223c92c6b959c6e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4377311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ef8be8f53bfcc830344fb9622af17686a831d7ba75c77b33c6c8dcbaa8f71c`

```dockerfile
```

-	Layers:
	-	`sha256:58855487f1a386bb4ddb4de3163598fce020991372df5db3c1b898f12ca9654b`  
		Last Modified: Fri, 31 Oct 2025 03:22:18 GMT  
		Size: 4.4 MB (4358216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d68c2dcfebe96049d33d6717ad6d8954535bff5e89e3b0d809a8b97773500fe`  
		Last Modified: Fri, 31 Oct 2025 03:22:19 GMT  
		Size: 19.1 KB (19095 bytes)  
		MIME: application/vnd.in-toto+json
