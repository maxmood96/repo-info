## `websphere-liberty:kernel-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:195415557cad59cb952f2f6547f69abfc8a05983f4d5dcae14b4a67c3e9fddfe
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
$ docker pull websphere-liberty@sha256:1a2e8c33b3801d7fffa3c351c8ef4d778856a5f7a4c480a421b0f747e86ec967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190327934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:181d9e518271ddc8ceab9ea716519964320fc1eac2f1be2997c7cd18917db0f3`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 21 May 2025 02:47:06 GMT
USER root
# Wed, 21 May 2025 02:47:06 GMT
ARG VERBOSE=false
# Wed, 21 May 2025 02:47:06 GMT
ARG OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_VERSION=25.0.0.5
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_BUILD_LABEL=cl250520250504-1901
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.5 org.opencontainers.image.revision=cl250520250504-1901 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.5 com.ibm.websphere.liberty.version=25.0.0.5
# Wed, 21 May 2025 02:47:06 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.5 BuildLabel=cl250520250504-1901
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 21 May 2025 02:47:06 GMT
USER 1001
# Wed, 21 May 2025 02:47:06 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 21 May 2025 02:47:06 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 21 May 2025 02:47:06 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8803db35073b2740da6f9573de7c61691c99ce2638f0e6818c242609f4f3417e`  
		Last Modified: Wed, 14 May 2025 19:35:21 GMT  
		Size: 1.5 MB (1450255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa120ccd89f04004bf22720a697c7c4a886668c5f0b4bf862447e6a0849572e`  
		Last Modified: Wed, 14 May 2025 19:35:24 GMT  
		Size: 135.8 MB (135784811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468d25ac00211887c8fd95b36960c6e36f3d8dab35a9c39c9e6abb61b8824f4e`  
		Last Modified: Wed, 21 May 2025 17:37:33 GMT  
		Size: 113.8 KB (113840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2331ca5489a8df04bfae12df9b12dece7e52b8fe662e0f4aea47c6c440b2ef`  
		Last Modified: Wed, 21 May 2025 17:37:33 GMT  
		Size: 17.6 MB (17550712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6737b3e02587dcc93bbb39c32b456c38e92b0eab0fbf5efc6b95a70f7f61f2b`  
		Last Modified: Wed, 21 May 2025 17:37:32 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b8a914759a74937528d0185db4446910ba609b3ed6205652776038ef1a1b73`  
		Last Modified: Wed, 21 May 2025 17:37:33 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821a1259f03aefb1da30a446ce27ae18b32d60d943935dcc8504196562cc6dc9`  
		Last Modified: Wed, 21 May 2025 17:37:33 GMT  
		Size: 12.3 KB (12318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5e9bae8a69acb6687f910a3101fd8799ec21ddc31b30a23b2c498aa295a825`  
		Last Modified: Wed, 21 May 2025 17:37:33 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d62d3d62d3ddd8d67274cef9f65cb1fe69592fdcee21263b01179b0d89ee76`  
		Last Modified: Wed, 21 May 2025 17:37:33 GMT  
		Size: 13.1 KB (13121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c551982ffbcfa72e6a842d26c09ab3752cbf71ac9adc3d784be69ebd2f580f1`  
		Last Modified: Wed, 21 May 2025 17:37:34 GMT  
		Size: 5.9 MB (5867916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:1961a1d61133aa73a5cffd0e2ebf89e11d823a23f743594ef9381bffae64cb48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2242738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d22d80eadec9e0c2f88cc7b18ded0342e9f49c512786f72f4c5111a248a1aaa2`

```dockerfile
```

-	Layers:
	-	`sha256:352bf8dcd89fd9f92f3454edd97f8e5396d31516340fcfe8ffab52294dc4a756`  
		Last Modified: Wed, 21 May 2025 17:37:33 GMT  
		Size: 2.2 MB (2204447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dce8f84d0942b0bc260401f7fae367a671591b0d598c7056dfe560126d1186e`  
		Last Modified: Wed, 21 May 2025 17:37:32 GMT  
		Size: 38.3 KB (38291 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:a3b4f3b434c206c9b1b9a8ad0acc4b2a61a6d938a91ebc0d6276bfa5b09e416d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195679078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808851beac5c81c08bddefb0a686f5e44e8fc2f99f57ac2f359a13d60fe729ca`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 28 Apr 2025 09:45:54 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:45:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:45:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:45:58 GMT
ADD file:f6d72fdda03fb8754d82331b1f726d49b6b7d2d850ad2d1dfc2de6e1b365251b in / 
# Mon, 28 Apr 2025 09:45:59 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 21 May 2025 02:47:06 GMT
USER root
# Wed, 21 May 2025 02:47:06 GMT
ARG VERBOSE=false
# Wed, 21 May 2025 02:47:06 GMT
ARG OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_VERSION=25.0.0.5
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_BUILD_LABEL=cl250520250504-1901
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.5 org.opencontainers.image.revision=cl250520250504-1901 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.5 com.ibm.websphere.liberty.version=25.0.0.5
# Wed, 21 May 2025 02:47:06 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.5 BuildLabel=cl250520250504-1901
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 21 May 2025 02:47:06 GMT
USER 1001
# Wed, 21 May 2025 02:47:06 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 21 May 2025 02:47:06 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 21 May 2025 02:47:06 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:95ba4619a43d3f4f7f5ee2c8fbe313d19bb9c0e9ca5fa9efeb7b93f942dcf377`  
		Last Modified: Mon, 28 Apr 2025 10:44:03 GMT  
		Size: 34.4 MB (34443215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce266802d90bd81a35f2bfa06dda920a30ccaf77bd70a0f972e5ac85814cd8a`  
		Last Modified: Mon, 05 May 2025 17:22:29 GMT  
		Size: 1.5 MB (1536203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd2353677fff4d204b05c3ede75419526f90b6d0c20311ab2f6f641cbb7a658`  
		Last Modified: Wed, 14 May 2025 19:36:05 GMT  
		Size: 136.6 MB (136628899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45411c8bbdb7bcf1c1ece55f9d18cb215596e2213aba05618aadb9ff298ae93`  
		Last Modified: Wed, 21 May 2025 18:04:48 GMT  
		Size: 118.1 KB (118086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99ea1eb424e595d612fa69039dcf7ac18b5f6bd61bec807dae58fac68c791bc`  
		Last Modified: Wed, 21 May 2025 18:04:48 GMT  
		Size: 17.6 MB (17550844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84e49b4672e56cbc07bec11de0356e3fda45a85366e53e094dbb7d25bc9efd6`  
		Last Modified: Wed, 21 May 2025 18:04:48 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed42a7e671abb57791eb90c179e1e3ea389bc9986bc5121aa192f07e29e4afc5`  
		Last Modified: Wed, 21 May 2025 18:04:48 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53ec4cf3a893da44ede90154c26d076b0a6ce6404efc9fa69741cb78e6dc30f`  
		Last Modified: Wed, 21 May 2025 18:04:49 GMT  
		Size: 12.3 KB (12315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cab8b8ad7387526b1893f2699dfc518c349f22540d82c132d624ad435ad249`  
		Last Modified: Wed, 21 May 2025 18:04:49 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00d13740ffd6894f51d64bb646313b18895f7eff5e7e7f282a5e7b1832052d0`  
		Last Modified: Wed, 21 May 2025 18:04:49 GMT  
		Size: 13.1 KB (13127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f400ff2c2b155d22802b715ee56537b50092e9c3eeb2790f08396b8364ab1f`  
		Last Modified: Wed, 21 May 2025 18:04:50 GMT  
		Size: 5.4 MB (5374036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:589453bd3d25d31c30aa53089e01688c905d2ac82d0aa75cd9e7ea0cef2609a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2246060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0dcc0baa79f9f7ed6e4c20a22430a093a9faad11ce1c69d569f54ffcb708f9`

```dockerfile
```

-	Layers:
	-	`sha256:4d7bcf8118d910063f44760a3726b52632d23f90a248646c44bfc0146ff91bff`  
		Last Modified: Wed, 21 May 2025 18:04:48 GMT  
		Size: 2.2 MB (2207722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76bdd45dff70916a5abd954877fa31960ced59fc8bdd6a2f4f7b0066844b3b3f`  
		Last Modified: Wed, 21 May 2025 18:04:48 GMT  
		Size: 38.3 KB (38338 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:79c6fb3640d54ac71af32f0fa5084e4212cfcd57a812e9ade8f687a412eba691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.1 MB (186066197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa3fb84d614e3cddae766cba46e7301cf5abe7237dc37b224bc5efd73c06de5`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 23 Apr 2025 12:53:39 GMT
ARG RELEASE
# Wed, 23 Apr 2025 12:53:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 12:53:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 12:53:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 12:53:39 GMT
ADD file:4be5dde78df6dfb2332aa60bf4714ecf19075f664a5fac89ff50019cbee5434d in / 
# Wed, 23 Apr 2025 12:53:39 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 12:53:39 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 23 Apr 2025 12:53:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 23 Apr 2025 12:53:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 23 Apr 2025 12:53:39 GMT
USER root
# Wed, 23 Apr 2025 12:53:39 GMT
ARG VERBOSE=false
# Wed, 23 Apr 2025 12:53:39 GMT
ARG OPENJ9_SCC=true
# Wed, 23 Apr 2025 12:53:39 GMT
ARG LIBERTY_VERSION=25.0.0.4
# Wed, 23 Apr 2025 12:53:39 GMT
ARG LIBERTY_BUILD_LABEL=cl250420250407-1902
# Wed, 23 Apr 2025 12:53:39 GMT
ARG LIBERTY_SHA=9f30a336264ad7fe10fff6e0dfabc71ef8483760
# Wed, 23 Apr 2025 12:53:39 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.4 org.opencontainers.image.revision=cl250420250407-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.4 com.ibm.websphere.liberty.version=25.0.0.4
# Wed, 23 Apr 2025 12:53:39 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 23 Apr 2025 12:53:39 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.4 BuildLabel=cl250420250407-1902
# Wed, 23 Apr 2025 12:53:39 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.4 LIBERTY_BUILD_LABEL=cl250420250407-1902 LIBERTY_SHA=9f30a336264ad7fe10fff6e0dfabc71ef8483760
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
ARG LIBERTY_URL
# Wed, 23 Apr 2025 12:53:39 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 23 Apr 2025 12:53:39 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.4 LIBERTY_BUILD_LABEL=cl250420250407-1902 LIBERTY_SHA=9f30a336264ad7fe10fff6e0dfabc71ef8483760 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 23 Apr 2025 12:53:39 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.4 LIBERTY_BUILD_LABEL=cl250420250407-1902 LIBERTY_SHA=9f30a336264ad7fe10fff6e0dfabc71ef8483760 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.4 LIBERTY_BUILD_LABEL=cl250420250407-1902 LIBERTY_SHA=9f30a336264ad7fe10fff6e0dfabc71ef8483760 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.4 LIBERTY_BUILD_LABEL=cl250420250407-1902 LIBERTY_SHA=9f30a336264ad7fe10fff6e0dfabc71ef8483760 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 23 Apr 2025 12:53:39 GMT
USER 1001
# Wed, 23 Apr 2025 12:53:39 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 23 Apr 2025 12:53:39 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 23 Apr 2025 12:53:39 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:64d717faaf8dba48ef4989d39eb6faef5fe680871a4064f1753d9cc21de5bc3c`  
		Last Modified: Mon, 28 Apr 2025 10:44:16 GMT  
		Size: 28.0 MB (27999984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a80e8992168178f43fd2602a23cc2b2a1380dcba5882f3fbf1da5fe7f83ac5`  
		Last Modified: Mon, 05 May 2025 17:22:31 GMT  
		Size: 1.5 MB (1455700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2e97bf327de9faf2ba1006ffe91356f4a07ad8ca28c996b313b77ffabe65ed`  
		Last Modified: Wed, 14 May 2025 19:37:01 GMT  
		Size: 132.8 MB (132811842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2dc8e3ca5ba8ab4b4b03c48f7330467d6f3b56ea910ede18f3e09e9637b48ab`  
		Last Modified: Wed, 14 May 2025 20:05:10 GMT  
		Size: 114.7 KB (114668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14a2b41ba9bf327ceba8dc22280c896cf292aa69a3479b2377996b11156eeb0`  
		Last Modified: Wed, 14 May 2025 20:05:11 GMT  
		Size: 17.5 MB (17546911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34bce48de7da7a8ea5e8b894153a26a88d3064137a86a98b270ed69025c04b5`  
		Last Modified: Wed, 14 May 2025 20:05:10 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc52d464c51a5570a0c1eb37672ff8874407c9d119da58fc34de8f17cf1fe9c6`  
		Last Modified: Wed, 14 May 2025 20:05:10 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7e805736e501c75524b81a6f096b2ff157a7b27367f360183bb0ef46674148`  
		Last Modified: Wed, 14 May 2025 20:05:11 GMT  
		Size: 12.3 KB (12316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ce90a4a1800d95a092ca76f965fb2857c8081939ae9d9a3177c044cde5f352`  
		Last Modified: Wed, 14 May 2025 20:05:11 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d845ea81397537632a30ec403c6b661631a22417130cb6c5af1491afa80fe5e`  
		Last Modified: Wed, 14 May 2025 20:05:11 GMT  
		Size: 13.1 KB (13131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d104a2863665bb361cfb4d6b27ca3b2861687555e5642e42aab1bd7bebcad44c`  
		Last Modified: Wed, 14 May 2025 20:05:12 GMT  
		Size: 6.1 MB (6109295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:e26eaa2e77f61421bf180a363c9c5fb7e67ed5893da0f865d6d08b944b4ef938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bbecb404e9f290a5e24769a4e8088bebf5cf8d7429cbe91db0221897e4d7b94`

```dockerfile
```

-	Layers:
	-	`sha256:299f3e89e122292a4f78ee9c8b39d53136683c7b9138acd32aa00d1e8e894f00`  
		Last Modified: Wed, 14 May 2025 20:05:10 GMT  
		Size: 2.2 MB (2176387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfdf60e13a7901b0b6b5cf2476160127cdd1a4d392806d1d02582c571398c44a`  
		Last Modified: Wed, 14 May 2025 20:05:10 GMT  
		Size: 38.3 KB (38292 bytes)  
		MIME: application/vnd.in-toto+json
