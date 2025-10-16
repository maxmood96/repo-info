## `websphere-liberty:full-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:4e884b394aa2f5c198ca7e69639c764d96d2dd3ac7d37146086895f22477ef37
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
$ docker pull websphere-liberty@sha256:7d2190dc6d26ca2687a9bac719e96b700e197bc352d107867398be677c7b296c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.0 MB (571037549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94a6de6f9212eb608954c1c53911d30137493ae5bec79b87b03a1614abbc343`
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
# Thu, 09 Oct 2025 13:18:45 GMT
USER root
# Thu, 09 Oct 2025 13:18:45 GMT
ARG VERBOSE=false
# Thu, 09 Oct 2025 13:18:45 GMT
ARG OPENJ9_SCC=true
# Thu, 09 Oct 2025 13:18:45 GMT
ARG LIBERTY_VERSION=25.0.0.10
# Thu, 09 Oct 2025 13:18:45 GMT
ARG LIBERTY_BUILD_LABEL=cl251020250923-1355
# Thu, 09 Oct 2025 13:18:45 GMT
ARG LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa
# Thu, 09 Oct 2025 13:18:45 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.10 org.opencontainers.image.revision=cl251020250923-1355 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.10 com.ibm.websphere.liberty.version=25.0.0.10
# Thu, 09 Oct 2025 13:18:45 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Thu, 09 Oct 2025 13:18:45 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.10 BuildLabel=cl251020250923-1355
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
ARG LIBERTY_URL
# Thu, 09 Oct 2025 13:18:45 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Thu, 09 Oct 2025 13:18:45 GMT
USER 1001
# Thu, 09 Oct 2025 13:18:45 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 09 Oct 2025 13:18:45 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 09 Oct 2025 13:18:45 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 09 Oct 2025 13:18:45 GMT
ARG VERBOSE=false
# Thu, 09 Oct 2025 13:18:45 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
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
	-	`sha256:0b2791bdeb15b1d075dac04b944c19120157b4bccd40ef395bf4d7f3e0944bea`  
		Last Modified: Thu, 16 Oct 2025 00:42:45 GMT  
		Size: 113.7 KB (113681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855603634af5020167ca011a7e3f9419daeb17fa7a55523074ee2a8d031667bb`  
		Last Modified: Thu, 16 Oct 2025 00:42:47 GMT  
		Size: 17.7 MB (17655771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43845ddb1e79c26f4f51b8820f272a6a8ab494ddfc65fdcd8b10eb451b76bbb`  
		Last Modified: Thu, 16 Oct 2025 00:42:45 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10623a7b9a6bae51f09b24d9394134b1038c5bd9ae8d5f418db87161e17aa8f1`  
		Last Modified: Thu, 16 Oct 2025 00:42:45 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63743dfb242a73cf0be6519279c54087f960f3a4ed67250c6fbd4fbb94038115`  
		Last Modified: Thu, 16 Oct 2025 00:42:46 GMT  
		Size: 14.4 KB (14394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c495d0b4740fe829e7783f6c889f07745500215c9895877886e2b02e01fdb18e`  
		Last Modified: Thu, 16 Oct 2025 00:42:46 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021ec90c103b8901be971c4b961f402ec50260533644ef897c7fdf670f426648`  
		Last Modified: Thu, 16 Oct 2025 00:42:46 GMT  
		Size: 15.3 KB (15271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9907dc874304e8fc04e8a1a2419c0dc568e4fd4ff847c2b6d5a105af6ac21e`  
		Last Modified: Thu, 16 Oct 2025 00:42:47 GMT  
		Size: 5.7 MB (5728947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4680b8646c88d44b2d64027d9c8cba285db117108c4c17cdbe5d1aea43dc18`  
		Last Modified: Thu, 16 Oct 2025 03:57:26 GMT  
		Size: 365.5 MB (365506967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d2cd13b488835b65b3f9a07f095ce24bbf345e703a3a0a63f60089ba3f96e8`  
		Last Modified: Thu, 16 Oct 2025 03:56:11 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662d17274e76200b132faba0c75e56960ceca8841382501a28662bc477629199`  
		Last Modified: Thu, 16 Oct 2025 03:56:16 GMT  
		Size: 15.6 MB (15594860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:bdcf692145a79f6cc9516d61072a6dc07547eb2c35ec79c442c6b8c173026b24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc5457e5b7630fefa99caeebb8b75e542303f1f5c64aaf24c4946e5816bd59c`

```dockerfile
```

-	Layers:
	-	`sha256:9a677b4ac6a63f16d04a39e4cedf5d640f26b6eecce5f3a4dd5f71e1d33d7567`  
		Last Modified: Thu, 16 Oct 2025 06:20:50 GMT  
		Size: 4.4 MB (4358877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18232448f948c73ccd956dbbfafbc494e310675d8325cd710713dbd3e7804c50`  
		Last Modified: Thu, 16 Oct 2025 06:20:50 GMT  
		Size: 19.1 KB (19138 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:620b8df6105a98284f8b7f3309e6a794f9e8923e2ef8bc3277aeb0784f26f661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.5 MB (574462797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff4ed9fe8d6d1fe00d6f2298b1a8ef452fa2b3c0e9270e916c40ef968f104af`
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
# Thu, 09 Oct 2025 13:18:45 GMT
USER root
# Thu, 09 Oct 2025 13:18:45 GMT
ARG VERBOSE=false
# Thu, 09 Oct 2025 13:18:45 GMT
ARG OPENJ9_SCC=true
# Thu, 09 Oct 2025 13:18:45 GMT
ARG LIBERTY_VERSION=25.0.0.10
# Thu, 09 Oct 2025 13:18:45 GMT
ARG LIBERTY_BUILD_LABEL=cl251020250923-1355
# Thu, 09 Oct 2025 13:18:45 GMT
ARG LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa
# Thu, 09 Oct 2025 13:18:45 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.10 org.opencontainers.image.revision=cl251020250923-1355 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.10 com.ibm.websphere.liberty.version=25.0.0.10
# Thu, 09 Oct 2025 13:18:45 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Thu, 09 Oct 2025 13:18:45 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.10 BuildLabel=cl251020250923-1355
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
ARG LIBERTY_URL
# Thu, 09 Oct 2025 13:18:45 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Thu, 09 Oct 2025 13:18:45 GMT
USER 1001
# Thu, 09 Oct 2025 13:18:45 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 09 Oct 2025 13:18:45 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 09 Oct 2025 13:18:45 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 09 Oct 2025 13:18:45 GMT
ARG VERBOSE=false
# Thu, 09 Oct 2025 13:18:45 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
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
	-	`sha256:8302e95e32936b88e6909154fdabee00f414147f220df254882fb2acf235ef0a`  
		Last Modified: Thu, 16 Oct 2025 01:06:10 GMT  
		Size: 118.1 KB (118093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e852368bd5b4e4071105517a3fb7e708462ade6c6180cada01a4dae229fc38b`  
		Last Modified: Thu, 16 Oct 2025 01:06:14 GMT  
		Size: 17.7 MB (17656058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05cc75c945b168a44ff97275616172b782f26f35d4316fe8f43ef8d94381e7e`  
		Last Modified: Thu, 16 Oct 2025 01:06:11 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da6a36ddfdfd82f04c2cf434bc614a21e5c609beb5976858918a69a377331a4`  
		Last Modified: Thu, 16 Oct 2025 01:06:12 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2eafcd710ca5ac90e5bd270c3d06d8729789b6ccd56be08c01db585409e8ab`  
		Last Modified: Thu, 16 Oct 2025 01:06:11 GMT  
		Size: 14.4 KB (14396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd25d1b195acacf0ae5cc8bd27f62deb5fac296bdb59b62bec42d189bd69b4c`  
		Last Modified: Thu, 16 Oct 2025 01:06:11 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81e2e948dadc72d0b20c194386de229a24551c030133c2969de77fde27f6554`  
		Last Modified: Thu, 16 Oct 2025 01:06:11 GMT  
		Size: 15.3 KB (15276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e778c15965592b6bcf93cea00dd4c356ef3ef77a74fb07bfdb78e84d61b363`  
		Last Modified: Thu, 16 Oct 2025 01:06:12 GMT  
		Size: 5.4 MB (5434386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4c10dac4c4bff6f0679b2b89e23bedb178a3631c8c7175d840127fa7a77450`  
		Last Modified: Thu, 16 Oct 2025 02:10:44 GMT  
		Size: 365.5 MB (365507170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afc719d1a6d584a1b898ac6371f58c17575fa9e9ae8a5b69c6729215ef321c4`  
		Last Modified: Thu, 16 Oct 2025 01:21:44 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a6d44bdc57a76d9edd274826d9ee1bf6d27a2d3e74936c4f475f9bec973fb8`  
		Last Modified: Thu, 16 Oct 2025 01:21:46 GMT  
		Size: 13.4 MB (13367989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:b7252e6b1c72f1f04d13fe2d55e7d76817f2a3ecd4c7d4ac46c7c9d2251c021b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267e59a6b3e77a9807a87bd978bb61faf1ce6b57676deab03aaad2149fc0c331`

```dockerfile
```

-	Layers:
	-	`sha256:4343fa84c992bc588e3f4c809dc3d11359e72c9ec4c2e14a7a7fd8c4a4e1785a`  
		Last Modified: Thu, 16 Oct 2025 03:22:05 GMT  
		Size: 4.4 MB (4362152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0999f1d1e672b00cad75ad0776e272673494a1818ff6e156f7f8a962b4561728`  
		Last Modified: Thu, 16 Oct 2025 03:22:07 GMT  
		Size: 19.2 KB (19178 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:472c33f713a18f2e2f159f4f9c588a7cd126a215d897d23114c4d925b86faa91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.0 MB (566958696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feecc87acf48ab32ae9a28f80fc1e7d802607739ae71628576525eca22201678`
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
# Thu, 09 Oct 2025 13:18:45 GMT
USER root
# Thu, 09 Oct 2025 13:18:45 GMT
ARG VERBOSE=false
# Thu, 09 Oct 2025 13:18:45 GMT
ARG OPENJ9_SCC=true
# Thu, 09 Oct 2025 13:18:45 GMT
ARG LIBERTY_VERSION=25.0.0.10
# Thu, 09 Oct 2025 13:18:45 GMT
ARG LIBERTY_BUILD_LABEL=cl251020250923-1355
# Thu, 09 Oct 2025 13:18:45 GMT
ARG LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa
# Thu, 09 Oct 2025 13:18:45 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.10 org.opencontainers.image.revision=cl251020250923-1355 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.10 com.ibm.websphere.liberty.version=25.0.0.10
# Thu, 09 Oct 2025 13:18:45 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Thu, 09 Oct 2025 13:18:45 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.10 BuildLabel=cl251020250923-1355
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
ARG LIBERTY_URL
# Thu, 09 Oct 2025 13:18:45 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Thu, 09 Oct 2025 13:18:45 GMT
USER 1001
# Thu, 09 Oct 2025 13:18:45 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 09 Oct 2025 13:18:45 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 09 Oct 2025 13:18:45 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 09 Oct 2025 13:18:45 GMT
ARG VERBOSE=false
# Thu, 09 Oct 2025 13:18:45 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
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
	-	`sha256:8a81dc450cc4bb86018997302f414af4704d49d20fc56b0f477fbf0cc675c0f4`  
		Last Modified: Thu, 16 Oct 2025 00:59:51 GMT  
		Size: 114.6 KB (114621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bb1e525b4559362bfb390c873b83cccae04e1a9ed1477967c1e6ef878be294`  
		Last Modified: Thu, 16 Oct 2025 00:59:53 GMT  
		Size: 17.7 MB (17655479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b12085e10bb64dbe55c40b6914250c8cfa3ed1b71c4286393f126b11a4efa16`  
		Last Modified: Thu, 16 Oct 2025 00:59:51 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139c80bf5cb59deffbf22480dfa7fdd93b6c961769fc258ddec8d19955b8ed74`  
		Last Modified: Thu, 16 Oct 2025 00:59:51 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97807c4e2d743cb6db9e2b6abebb8f8d7daad0f2e0fc611bc7222f9912269b5d`  
		Last Modified: Thu, 16 Oct 2025 00:59:51 GMT  
		Size: 14.4 KB (14394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1484eb0a8f2868fc28e8e38b4f783195a9dae5d1aea2fca581ba0250885ec14`  
		Last Modified: Thu, 16 Oct 2025 00:59:52 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f8adbae6667aa99dd51b88ce9ef56967f5ed5942373bcf50623c709885311c`  
		Last Modified: Thu, 16 Oct 2025 00:59:52 GMT  
		Size: 15.3 KB (15264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b5dbb378f120fdf5b21069b9e7210c2ff837def2ef9d319f2ada7a52a559b1`  
		Last Modified: Thu, 16 Oct 2025 00:59:53 GMT  
		Size: 6.0 MB (6008585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa342f52ed44c6e4fd930988b0ac7d8cad9871a628be0ee999cc51a536e56e6`  
		Last Modified: Thu, 16 Oct 2025 01:59:20 GMT  
		Size: 365.5 MB (365506861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ebf2c2ba248c8e04d266d32e0375844e64a16b7f7588458147b80a64552fab`  
		Last Modified: Thu, 16 Oct 2025 01:23:12 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9795857571664d0d09bff36738f67679142af7e4a0fc13f901f80b1894e4fe34`  
		Last Modified: Thu, 16 Oct 2025 01:23:13 GMT  
		Size: 15.9 MB (15892171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:d210a91e3717b2c819b287345e9fc27c6be263d7e19a2b27b9dfc42fe7988fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4376776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1625908db697023da9413958947e794553fcd971475f401c936279d6062e908f`

```dockerfile
```

-	Layers:
	-	`sha256:638ad03a463dd2426e07c11056a4c0f9c40feacd88429fb21b6b972bcb6a7eac`  
		Last Modified: Thu, 16 Oct 2025 03:22:12 GMT  
		Size: 4.4 MB (4357638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2da1a82eee45c09b0801ee081df58090606682399dfb132860cff0738263ab50`  
		Last Modified: Thu, 16 Oct 2025 03:22:12 GMT  
		Size: 19.1 KB (19138 bytes)  
		MIME: application/vnd.in-toto+json
