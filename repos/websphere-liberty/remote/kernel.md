## `websphere-liberty:kernel`

```console
$ docker pull websphere-liberty@sha256:72f5b79b71902b2a1d44c1500481ea32c3547dad4c02bb195176fed312ceb883
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
$ docker pull websphere-liberty@sha256:75bfd650101e81a37b5d2dce3e23a0e4cf88384da74383a39d5be166cedf6548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.5 MB (190502881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f04d587a3adff365c2fbd36a4e9f6f1bcaa97404e25146224804bed42e2504e2`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:38:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Mar 2026 01:38:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:38:00 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Mar 2026 01:38:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0a965c513bb522004ddb195fbb3cda7124559b8c7c082fc8626b2f45b4ce9a94';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ebf5f90f77e524593cba310d9e73d993bc8d3357af0127ec4627b1ce8236f385';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8353fb367a56fd150bd5b1facb595bde690c9f9a1f3db7db3b7fb240399a6ae9';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Mar 2026 01:38:42 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 25 Mar 2026 17:54:11 GMT
USER root
# Wed, 25 Mar 2026 17:54:11 GMT
ARG VERBOSE=false
# Wed, 25 Mar 2026 17:54:11 GMT
ARG OPENJ9_SCC=true
# Wed, 25 Mar 2026 17:54:11 GMT
ARG LIBERTY_VERSION=26.0.0.3
# Wed, 25 Mar 2026 17:54:11 GMT
ARG LIBERTY_BUILD_LABEL=cl260320260309-1102
# Wed, 25 Mar 2026 17:54:11 GMT
ARG LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4
# Wed, 25 Mar 2026 17:54:11 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.3 org.opencontainers.image.revision=cl260320260309-1102 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.3 com.ibm.websphere.liberty.version=26.0.0.3
# Wed, 25 Mar 2026 17:54:11 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Wed, 25 Mar 2026 17:54:11 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.3 BuildLabel=cl260320260309-1102
# Wed, 25 Mar 2026 17:54:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 25 Mar 2026 17:54:11 GMT
ARG LIBERTY_URL
# Wed, 25 Mar 2026 17:54:11 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 25 Mar 2026 17:54:30 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Mar 2026 17:54:30 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 25 Mar 2026 17:54:30 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 25 Mar 2026 17:54:30 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 25 Mar 2026 17:54:30 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 25 Mar 2026 17:54:30 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 25 Mar 2026 17:54:30 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Wed, 25 Mar 2026 17:54:36 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 25 Mar 2026 17:54:36 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 25 Mar 2026 17:54:36 GMT
USER 1001
# Wed, 25 Mar 2026 17:54:36 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 25 Mar 2026 17:54:36 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 25 Mar 2026 17:54:36 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907aa1863e414cc3bd625d16f193eb2a7a696d737f29ea8028674b7ff063b7ea`  
		Last Modified: Tue, 17 Mar 2026 01:38:55 GMT  
		Size: 1.5 MB (1450031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31583ab84185052af0267c732938b8d9abf260403c2b16db59ce3c029cb1306e`  
		Last Modified: Tue, 17 Mar 2026 01:38:58 GMT  
		Size: 135.8 MB (135804403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9263164b3f629a6788853331cbd1d0719707984afbc6e2669130a58f32609da`  
		Last Modified: Wed, 25 Mar 2026 17:54:44 GMT  
		Size: 113.7 KB (113679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5751ecfde0b7b17f47fa8988e09355de898988bed4a9ed25c57b961343931ec9`  
		Last Modified: Wed, 25 Mar 2026 17:54:45 GMT  
		Size: 17.8 MB (17834539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afdf8a81b97108d413fdefa9a562d70f123b568147b1e7c0df7f7672ce846e97`  
		Last Modified: Wed, 25 Mar 2026 17:54:45 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad600ccd5103e18b46a35666945a11144f3fbdbe5ee86fec1389e4e48c878c40`  
		Last Modified: Wed, 25 Mar 2026 17:54:45 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd382af83ec754ba1585c1001eba259009cfd02714ba7798ea264dafe3a7f37`  
		Last Modified: Wed, 25 Mar 2026 17:54:46 GMT  
		Size: 14.1 KB (14122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4771e7e0668363a0f1081147c4047b0f187c5dea9a1336f9656218224e195fd8`  
		Last Modified: Wed, 25 Mar 2026 17:54:46 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c9b34dd930549b613cdca81ebea045b2c670679edd8cb6cf7eb9e83210dc05`  
		Last Modified: Wed, 25 Mar 2026 17:54:46 GMT  
		Size: 15.0 KB (14989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c016ddb6a304701c2a5bc43cc689367584843662100a14ba9f19abc667372202`  
		Last Modified: Wed, 25 Mar 2026 17:54:47 GMT  
		Size: 5.7 MB (5730240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:6cc5f7e0d8308c5daad96b665bcc72b97356b9d6bbb9320bbce697efc1505ad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2341982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad87db13583718f1c97017678ed0bb34a3a01f248edf7a0317ba78edf973b34a`

```dockerfile
```

-	Layers:
	-	`sha256:4df1d4d3246d09149e56478eafc3711285ad284f6d194415e49fa0793691eded`  
		Last Modified: Wed, 25 Mar 2026 17:54:45 GMT  
		Size: 2.3 MB (2303003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e34956974a53625a535afddccbd9f991a7d964cedc2073ee9fec8a5f11d90bd`  
		Last Modified: Wed, 25 Mar 2026 17:54:44 GMT  
		Size: 39.0 KB (38979 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:33a894a4cb920fa163162439972b1547eb88feb156afe2ee932c569ef246fd10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196157814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8589d00bdff33985e3beeeb9de6cb8184a6ce7a603eec36cfdeebdd3a7a7738`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 24 Feb 2026 07:34:11 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:34:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:34:16 GMT
ADD file:8cdc5dcac981a23986a941c048f55a86d8ba46328e91ad30db9af43286781c61 in / 
# Tue, 24 Feb 2026 07:34:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 09:00:17 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Mar 2026 09:00:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 09:00:17 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Mar 2026 09:00:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0a965c513bb522004ddb195fbb3cda7124559b8c7c082fc8626b2f45b4ce9a94';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ebf5f90f77e524593cba310d9e73d993bc8d3357af0127ec4627b1ce8236f385';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8353fb367a56fd150bd5b1facb595bde690c9f9a1f3db7db3b7fb240399a6ae9';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Mar 2026 09:00:59 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 25 Mar 2026 18:08:35 GMT
USER root
# Wed, 25 Mar 2026 18:08:35 GMT
ARG VERBOSE=false
# Wed, 25 Mar 2026 18:08:35 GMT
ARG OPENJ9_SCC=true
# Wed, 25 Mar 2026 18:08:35 GMT
ARG LIBERTY_VERSION=26.0.0.3
# Wed, 25 Mar 2026 18:08:35 GMT
ARG LIBERTY_BUILD_LABEL=cl260320260309-1102
# Wed, 25 Mar 2026 18:08:35 GMT
ARG LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4
# Wed, 25 Mar 2026 18:08:35 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.3 org.opencontainers.image.revision=cl260320260309-1102 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.3 com.ibm.websphere.liberty.version=26.0.0.3
# Wed, 25 Mar 2026 18:08:35 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Wed, 25 Mar 2026 18:08:35 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.3 BuildLabel=cl260320260309-1102
# Wed, 25 Mar 2026 18:08:35 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 25 Mar 2026 18:08:35 GMT
ARG LIBERTY_URL
# Wed, 25 Mar 2026 18:08:35 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 25 Mar 2026 18:08:53 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Mar 2026 18:08:53 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 25 Mar 2026 18:08:55 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 25 Mar 2026 18:08:56 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 25 Mar 2026 18:08:56 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 25 Mar 2026 18:08:57 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 25 Mar 2026 18:08:58 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Wed, 25 Mar 2026 18:09:08 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 25 Mar 2026 18:09:08 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 25 Mar 2026 18:09:08 GMT
USER 1001
# Wed, 25 Mar 2026 18:09:08 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 25 Mar 2026 18:09:08 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 25 Mar 2026 18:09:08 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:31e4dc9ee1718c21d378c7cdb3929e157eabf4d70fe4bbe2e6b8ec5289e836dc`  
		Last Modified: Tue, 24 Feb 2026 08:08:05 GMT  
		Size: 34.5 MB (34453448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058d2f7f8365d8d5d5c83ad30e1c8995b2eaa6b1c50b7e1b1caa14e6ba0d13e1`  
		Last Modified: Tue, 17 Mar 2026 09:01:28 GMT  
		Size: 1.5 MB (1536093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b990e2f2714a48197073ae8696b1699afebaa89893fb7cfe4bbed983bbd1a3b0`  
		Last Modified: Tue, 17 Mar 2026 09:01:35 GMT  
		Size: 136.7 MB (136749908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ad51e0ba70ef38e3e6f966aaa96d13a98318bf90e6651fbbbc401ad5143e8a`  
		Last Modified: Wed, 25 Mar 2026 18:09:41 GMT  
		Size: 118.0 KB (117991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9f1ce76a5b4a81bdb7665ec813cb5b885c7a1ff631037b3e42ae4ed0eacf84`  
		Last Modified: Wed, 25 Mar 2026 18:09:42 GMT  
		Size: 17.8 MB (17834786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976f8964b0542ebc976cc9d8886b7b31c3ac6fae9a652b115e2e2baf44bb0ed7`  
		Last Modified: Wed, 25 Mar 2026 18:09:41 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed8da26931901b68b4a6e4f19e699b8a27efe6b43a483b6afcf0c6385684115`  
		Last Modified: Wed, 25 Mar 2026 18:09:41 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c02bab308a46309120e69349bcb851148ad29927825935839c9e8b2664b454`  
		Last Modified: Wed, 25 Mar 2026 18:09:42 GMT  
		Size: 14.1 KB (14120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea0ba0a4baa8af0e0dd33699066ecfbd1f7b81fade0983e927ca64621ce26d5`  
		Last Modified: Wed, 25 Mar 2026 18:09:42 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca55f1aa2c24b477ed95ca4ebfea10bc90c3e9faad092650d208f973c0b7a87`  
		Last Modified: Wed, 25 Mar 2026 18:09:43 GMT  
		Size: 15.0 KB (15005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a22254a4d87e3d54d15627e76174ae48e3d58fabaef2ce90e8c873b2d3983c5`  
		Last Modified: Wed, 25 Mar 2026 18:09:44 GMT  
		Size: 5.4 MB (5434107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:aa8e02e32658b2938940d626d59bc4b8f972146ae7b0d791ae8af6bd9be646f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2345304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5540787ef00c6e0e24659a611d3dc70de94ccfbe65232a72f81748ed461e3f6`

```dockerfile
```

-	Layers:
	-	`sha256:c0a77aef82084d06e7fe9d36b0e0210d061e31151a5a7ce19150a51ea8db8bdb`  
		Last Modified: Wed, 25 Mar 2026 18:09:41 GMT  
		Size: 2.3 MB (2306278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fc2da412b8f0d5fdfed4900de01e5851df1dc1913906484fb5d82aeded58cb8`  
		Last Modified: Wed, 25 Mar 2026 18:09:41 GMT  
		Size: 39.0 KB (39026 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:42da9a8a15192a13f09f2dc3330b91210f39b54b196be8ecde865e7039f285d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.8 MB (186803848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb9833344b1a64e96fb66c5d64ed1136dcd864b6dbd7916c6645d7daf286a13`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:34 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:35 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:36 GMT
ADD file:03057d2fc9102d77c6c1ba39821174f9277c7aeb8de5358b12c437097e81cdb8 in / 
# Tue, 24 Feb 2026 07:33:36 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:34:08 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Mar 2026 02:34:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:34:08 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Mar 2026 02:35:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0a965c513bb522004ddb195fbb3cda7124559b8c7c082fc8626b2f45b4ce9a94';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ebf5f90f77e524593cba310d9e73d993bc8d3357af0127ec4627b1ce8236f385';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8353fb367a56fd150bd5b1facb595bde690c9f9a1f3db7db3b7fb240399a6ae9';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Mar 2026 02:35:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 25 Mar 2026 17:57:37 GMT
USER root
# Wed, 25 Mar 2026 17:57:37 GMT
ARG VERBOSE=false
# Wed, 25 Mar 2026 17:57:37 GMT
ARG OPENJ9_SCC=true
# Wed, 25 Mar 2026 17:57:37 GMT
ARG LIBERTY_VERSION=26.0.0.3
# Wed, 25 Mar 2026 17:57:37 GMT
ARG LIBERTY_BUILD_LABEL=cl260320260309-1102
# Wed, 25 Mar 2026 17:57:37 GMT
ARG LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4
# Wed, 25 Mar 2026 17:57:37 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.3 org.opencontainers.image.revision=cl260320260309-1102 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.3 com.ibm.websphere.liberty.version=26.0.0.3
# Wed, 25 Mar 2026 17:57:37 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Wed, 25 Mar 2026 17:57:37 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.3 BuildLabel=cl260320260309-1102
# Wed, 25 Mar 2026 17:57:37 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 25 Mar 2026 17:57:37 GMT
ARG LIBERTY_URL
# Wed, 25 Mar 2026 17:57:37 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 25 Mar 2026 17:57:49 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Mar 2026 17:57:49 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 25 Mar 2026 17:57:50 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 25 Mar 2026 17:57:50 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 25 Mar 2026 17:57:50 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 25 Mar 2026 17:57:50 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 25 Mar 2026 17:57:50 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Wed, 25 Mar 2026 17:57:55 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 25 Mar 2026 17:57:55 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 25 Mar 2026 17:57:55 GMT
USER 1001
# Wed, 25 Mar 2026 17:57:55 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 25 Mar 2026 17:57:55 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 25 Mar 2026 17:57:55 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:b108e2a3f64e047295acfb714c51eedfbd4912d55d53e8bbbad5c2ac52fdf289`  
		Last Modified: Tue, 24 Feb 2026 08:08:19 GMT  
		Size: 28.0 MB (28007102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ec19658856db1b8624bd8ebec866bdd80a75f89b9975fa0a83c84c0a82533d`  
		Last Modified: Tue, 17 Mar 2026 02:35:34 GMT  
		Size: 1.5 MB (1455803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530c4a63b925697e8ab7861cc42e5a891be2cb407053bb6155a9b92a251f0926`  
		Last Modified: Tue, 17 Mar 2026 02:35:36 GMT  
		Size: 133.3 MB (133270717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7ed5c00388940676ac015a23cd6a393780737c7df2f73be5e760705b62b00b`  
		Last Modified: Wed, 25 Mar 2026 17:58:12 GMT  
		Size: 114.7 KB (114681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed30084349b657ac0af39e70fd55a892dfe5527da6c20b147adde8eb80c4526`  
		Last Modified: Wed, 25 Mar 2026 17:58:12 GMT  
		Size: 17.8 MB (17834293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b67285bf604e7c2bc4ac04f10c1451d0c5a2b3bd639d463330610174d89f3c9`  
		Last Modified: Wed, 25 Mar 2026 17:58:12 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c25035fe99db815651b8008df7bfbea527e28216f61af8ef8f9726c1f38dc3`  
		Last Modified: Wed, 25 Mar 2026 17:58:12 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c4fa843e7727d6e3e7421d60fbee94d513b686891baa44950fdfe4b319e455`  
		Last Modified: Wed, 25 Mar 2026 17:58:13 GMT  
		Size: 14.1 KB (14124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf162e110c306511fbf1a46cf8d22967efeff3b5421f049c49dae7c3c505b48`  
		Last Modified: Wed, 25 Mar 2026 17:58:12 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef92ce2fef9ec12343df9ff8c97726d3c9042b8f0a5081658411b02e96a75ff7`  
		Last Modified: Wed, 25 Mar 2026 17:58:13 GMT  
		Size: 15.0 KB (15001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441698a54957facfdefcc4a7621680166985b8cc0fdaafb51bdcc572120846dd`  
		Last Modified: Wed, 25 Mar 2026 17:58:14 GMT  
		Size: 6.1 MB (6089768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:51b625a03c110053037c48719f287909fd074a55c98c9f71803a254890466abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2340744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4da238f0f824ffd5c6887bbc8a4e63820878fd3ce14334eb1b9a04611089ffa`

```dockerfile
```

-	Layers:
	-	`sha256:282fc6adca8689e24e20543e01efc86acec033e5f955edfd9782daf0b93233f7`  
		Last Modified: Wed, 25 Mar 2026 17:58:12 GMT  
		Size: 2.3 MB (2301764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c555de215758358b68cfdaf4a3b85d611c982f0c7fef320f00e2c9b5a4871c7`  
		Last Modified: Wed, 25 Mar 2026 17:58:12 GMT  
		Size: 39.0 KB (38980 bytes)  
		MIME: application/vnd.in-toto+json
