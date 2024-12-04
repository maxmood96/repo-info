## `websphere-liberty:kernel-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:447c856f5365025bdd2f4449edeacc5e5f1765bd7ad32f07b0e58f4a75b9512a
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
$ docker pull websphere-liberty@sha256:407abf7cbfe6f7737050d971c13798bf2742dbaecbc2f4204d6d6b708ac04f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.4 MB (189371390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf884a95245b6f00ed8ad213684684cf351ca550a4d32a01d958c2b35e2feed`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
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
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457c1d1531a658e8df67b03b1aedd5932972c09ea092da971395b95255ad78fe`  
		Last Modified: Tue, 17 Sep 2024 00:59:12 GMT  
		Size: 1.4 MB (1438182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49083123286fc182df0b1fca6d374c8a140d8b2df476782db907a7ac50099b2e`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 135.0 MB (135014259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fa914b78abebc79a3e4678b7f1005a35310eba552c613956e161ff770bdb77`  
		Last Modified: Tue, 03 Dec 2024 22:29:16 GMT  
		Size: 113.3 KB (113332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d6dce156363d940ae9e1a7e43c9632b0726cdb45d3b5b219f1ac23e88ee0a5`  
		Last Modified: Tue, 03 Dec 2024 22:29:17 GMT  
		Size: 17.4 MB (17435827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b19bc1616ff7a4459b6a4bb73df3ddae948b8f038e43bfff0b61208cc42317`  
		Last Modified: Tue, 03 Dec 2024 22:29:16 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f85fdd3d709c101495844d0fff20474acfdb2a5ddffea5b4237bd68cfb2b92`  
		Last Modified: Tue, 03 Dec 2024 22:29:16 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3931e5bd33bcf7aebdd57a378cb940217a10747bcd3e433ea4c68a7797d3f332`  
		Last Modified: Tue, 03 Dec 2024 22:29:17 GMT  
		Size: 11.8 KB (11840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9583cc709aec5120a2ab11826288c2fcab49014d450864e6f1d3bbd7cbf05e`  
		Last Modified: Tue, 03 Dec 2024 22:29:17 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6c1fc3c49e2775487b8630a178b7247b1ff7ea72e99c9894dcef2a99ccc263`  
		Last Modified: Tue, 03 Dec 2024 22:29:17 GMT  
		Size: 12.6 KB (12644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f6604589c2ec4b0079b7a8cc3a07a4408c78365813afa532ba76ddd0bb901c`  
		Last Modified: Tue, 03 Dec 2024 22:29:18 GMT  
		Size: 5.8 MB (5807263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:c1640e39e511bf4a39eaed3a1e17cc2821c64a464a3a650df187e052fbcecec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2213962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d640957b07ecf435939a1c6d6d9560e76ad0495c33c8fb055684d0aec032d5ad`

```dockerfile
```

-	Layers:
	-	`sha256:5e18637b4c3e3a8ebfd18cde2892ae99402d56304b04683295a43c11a216a59d`  
		Last Modified: Tue, 03 Dec 2024 22:29:16 GMT  
		Size: 2.2 MB (2175804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a88ee25bc2183e18bee29f8e1c50363cb9e64e2de09321a79bc85f66f785fe0`  
		Last Modified: Tue, 03 Dec 2024 22:29:16 GMT  
		Size: 38.2 KB (38158 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:b041606c93597e3f62f5f604d59f7a3adfcc83098e5b24511edacc933c0b43e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194364995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f11469e30dd0ce30cd69706e865745107fc451e44e935c86fb7acb8243706b1e`
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
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
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
	-	`sha256:b3bbf197217bba4985ce7c81155a527635555bffe359b533bea1b556d79b3516`  
		Last Modified: Tue, 17 Sep 2024 01:31:57 GMT  
		Size: 135.5 MB (135470631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e3915de8ae4fb36a991d8ee604d9d074dd522399097fb510fa15401c2be311`  
		Last Modified: Wed, 04 Dec 2024 00:07:50 GMT  
		Size: 117.9 KB (117883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf39fa92e442bef37302eadb3dad7299c127f910a91f0e944c0e5e8fb0229e1e`  
		Last Modified: Wed, 04 Dec 2024 00:07:53 GMT  
		Size: 17.4 MB (17436317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b967b2e573ef2e03624dfc9d4c6d02d1bd5e57faaf090667f77390723a138b51`  
		Last Modified: Wed, 04 Dec 2024 00:07:50 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d427cc3076c54905f7270e9f14ddd730052dd1855983cafb07854b588e097706`  
		Last Modified: Wed, 04 Dec 2024 00:07:50 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214a1825bbabcb86dfce580cc02ee6a6fb788fc3b9c01c68c324216a2abd24c7`  
		Last Modified: Wed, 04 Dec 2024 00:07:52 GMT  
		Size: 11.8 KB (11838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e69d33d7586eb9c2942b158b67eff2964fd833be0331f873df98928fa44fc4b`  
		Last Modified: Wed, 04 Dec 2024 00:07:51 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caab66f662ce38ab1d9272d32db83b24e052c2f45a72565a0b2aa9d5d0f977d4`  
		Last Modified: Wed, 04 Dec 2024 00:07:51 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2e413ddbfc53c8287165ddae0bc47576793db03743f5d0d9990d5a7607e2e2`  
		Last Modified: Wed, 04 Dec 2024 00:07:53 GMT  
		Size: 5.3 MB (5341825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:e8690762a0d0f59b987b10ffde55980e8d05d28c70e5042fce8bf73278c56b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2215928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15be3db5cf44d63c1901c187b4380e8308bf81863aded943c49e74ea6c8722f3`

```dockerfile
```

-	Layers:
	-	`sha256:be5f3daec57fac2281cac17b35def3dbe34d6f399b9182dfe261c0b60fd279b0`  
		Last Modified: Wed, 04 Dec 2024 00:07:51 GMT  
		Size: 2.2 MB (2177724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13ce14ecee978d83836ad0a7299112be4d5f0b334bd23fe1c8f99298c1e29d65`  
		Last Modified: Wed, 04 Dec 2024 00:07:50 GMT  
		Size: 38.2 KB (38204 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:546dbb0d809c557ce915fa4cc08813dd7c136bd29316d9edb0487c5734d19517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.1 MB (185095047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b65edbdf1c9e76e586d8d782f0681204c8340e9abb02ca08cd40f5d31a1dc54`
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

### `websphere-liberty:kernel-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:bd4b6191e888a88e217e99c94d472c419dd3d80057ff11ad62a38c2cc07c78c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2211479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e62b0113aee2421378bdce07df674672916129faf36f331946155c605a9a31`

```dockerfile
```

-	Layers:
	-	`sha256:3869b0b11c23f4067c0e9314e7e320b97372e89639c38272cf45b29748ac0738`  
		Last Modified: Tue, 03 Dec 2024 23:07:23 GMT  
		Size: 2.2 MB (2173321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:357e955f69197222f615cc6a528b75ad48b1fde9d7bdecb476b0deace616db29`  
		Last Modified: Tue, 03 Dec 2024 23:07:23 GMT  
		Size: 38.2 KB (38158 bytes)  
		MIME: application/vnd.in-toto+json
