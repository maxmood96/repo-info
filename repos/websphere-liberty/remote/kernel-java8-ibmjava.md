## `websphere-liberty:kernel-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:c0e8f9882a541c3f5f4fba7715c11886faf7174cb4638bb16eccd62398b0c2e3
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
$ docker pull websphere-liberty@sha256:6e6613c078834e7bcf1abd4d38cf9f9458a0c0a4490ef5381ab20cf1893b987d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190036416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db71f32ada548564b28d68314895ebe22a3b3127f1caa34e7c740f39ca702ff`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 14 Feb 2025 09:27:08 GMT
ARG RELEASE
# Fri, 14 Feb 2025 09:27:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Feb 2025 09:27:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Feb 2025 09:27:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 14 Feb 2025 09:27:08 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Fri, 14 Feb 2025 09:27:08 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 09:27:08 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 14 Feb 2025 09:27:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_VERSION=8.0.8.40
# Fri, 14 Feb 2025 09:27:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='20797bfcc79f9a5db0b83469f9d2dc90179ca8ef69d300d1a9f461f2e0ad49e2';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cd5b5435261af9a88e900b7780b79da4faf4b5b5dc573b3eb1106eec11a5f741';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1c112c7be92f201b0ec010d23d6b590744c3435b0b0f5398e7db1a23119fd590';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='6583c6e0bb859988ac10a2135c4700aaf069181d98b0a6d80414a17a6810e6e1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 25 Mar 2025 15:38:11 GMT
USER root
# Tue, 25 Mar 2025 15:38:11 GMT
ARG VERBOSE=false
# Tue, 25 Mar 2025 15:38:11 GMT
ARG OPENJ9_SCC=true
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_VERSION=25.0.0.3
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
# Tue, 25 Mar 2025 15:38:11 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.3 org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.3 com.ibm.websphere.liberty.version=25.0.0.3
# Tue, 25 Mar 2025 15:38:11 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Tue, 25 Mar 2025 15:38:11 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.3 BuildLabel=cl250320250310-1902
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_URL
# Tue, 25 Mar 2025 15:38:11 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Tue, 25 Mar 2025 15:38:11 GMT
USER 1001
# Tue, 25 Mar 2025 15:38:11 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 25 Mar 2025 15:38:11 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 25 Mar 2025 15:38:11 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db27cdfb76d083e85aa00bbe22cd27db8f26db49351cade3f1f1b94273a1da76`  
		Last Modified: Wed, 09 Apr 2025 01:18:32 GMT  
		Size: 1.5 MB (1450041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e999e5f4f81077186816d9ba8ce0d947fae85e4a5c0bac65f34bd23e065130`  
		Last Modified: Wed, 09 Apr 2025 01:18:35 GMT  
		Size: 135.5 MB (135522506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7048bd00d125aef1a4134025b9d900a59b8cb8148d4e3c5c7562e4c4148b3db`  
		Last Modified: Wed, 09 Apr 2025 02:17:57 GMT  
		Size: 113.8 KB (113753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da23ac6beb4bda649ecbc0b63eb215e5b201598575f8f64b69b6fa13ff4ebf9e`  
		Last Modified: Wed, 09 Apr 2025 02:17:58 GMT  
		Size: 17.5 MB (17535373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8d3079dfcf50920d61af304b1fb2f968132193fcb2881512b849ca4cb46435`  
		Last Modified: Wed, 09 Apr 2025 02:17:57 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834e659237fbecd2889b60cc3d635c8f595e0f34913535d12b01809726d5e337`  
		Last Modified: Wed, 09 Apr 2025 02:17:57 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff95b6ed85318068f0df327e9ecf10e25e5c7d50f65f0e1d9979496966f2db6`  
		Last Modified: Wed, 09 Apr 2025 02:17:58 GMT  
		Size: 12.2 KB (12232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf22d8752b9185e0607e276d2e047de6d6d4499c1e45b66e7af3b311d3e92e67`  
		Last Modified: Wed, 09 Apr 2025 02:17:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cec5b512904a432fffef682e24ce9d93d79164b1c462dc6f6fbfccf48cb1262`  
		Last Modified: Wed, 09 Apr 2025 02:17:58 GMT  
		Size: 13.0 KB (13039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d52239cb10c5e714f4d19ef01e0414c7c900a4a516f3d5a9a1298b04676d44`  
		Last Modified: Wed, 09 Apr 2025 02:18:00 GMT  
		Size: 5.9 MB (5854755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:4ddae6e7cc0b7d112ef38fa536cab5b903368d5f580e6d48d4df0231dadafd35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2215650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cdc07ea630e7a6ed5e220505a5375a3a2a2a434fd89c08372242ce106b6b4d6`

```dockerfile
```

-	Layers:
	-	`sha256:9fde9688a4546b649a05f9dad70410711af13c01edabec0c16e324a7578c9976`  
		Last Modified: Wed, 09 Apr 2025 02:17:57 GMT  
		Size: 2.2 MB (2177358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59696329db867cb130b697e2275289d80d0bf0e18d52981b685076562318e1da`  
		Last Modified: Wed, 09 Apr 2025 02:17:57 GMT  
		Size: 38.3 KB (38292 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:d823e54b1269a0da002254f25c5befd28cdb689b9b19760ded71c00ad5973e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.4 MB (195441461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5aedd91eab55dc2b0c40ce4b9103e2218b52ef4d99f1b1f244bde51e392b10`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 14 Feb 2025 09:27:08 GMT
ARG RELEASE
# Fri, 14 Feb 2025 09:27:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Feb 2025 09:27:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Feb 2025 09:27:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 14 Feb 2025 09:27:08 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Fri, 14 Feb 2025 09:27:08 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 09:27:08 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 14 Feb 2025 09:27:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_VERSION=8.0.8.40
# Fri, 14 Feb 2025 09:27:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='20797bfcc79f9a5db0b83469f9d2dc90179ca8ef69d300d1a9f461f2e0ad49e2';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cd5b5435261af9a88e900b7780b79da4faf4b5b5dc573b3eb1106eec11a5f741';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1c112c7be92f201b0ec010d23d6b590744c3435b0b0f5398e7db1a23119fd590';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='6583c6e0bb859988ac10a2135c4700aaf069181d98b0a6d80414a17a6810e6e1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 25 Mar 2025 15:38:11 GMT
USER root
# Tue, 25 Mar 2025 15:38:11 GMT
ARG VERBOSE=false
# Tue, 25 Mar 2025 15:38:11 GMT
ARG OPENJ9_SCC=true
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_VERSION=25.0.0.3
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
# Tue, 25 Mar 2025 15:38:11 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.3 org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.3 com.ibm.websphere.liberty.version=25.0.0.3
# Tue, 25 Mar 2025 15:38:11 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Tue, 25 Mar 2025 15:38:11 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.3 BuildLabel=cl250320250310-1902
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_URL
# Tue, 25 Mar 2025 15:38:11 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Tue, 25 Mar 2025 15:38:11 GMT
USER 1001
# Tue, 25 Mar 2025 15:38:11 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 25 Mar 2025 15:38:11 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 25 Mar 2025 15:38:11 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547283e0c0c821c0ccce507ca8c0bf3a722405e0f39eb5af2c012b83f5afb63e`  
		Last Modified: Wed, 09 Apr 2025 05:42:37 GMT  
		Size: 1.5 MB (1536154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e20e03e21013c0c4063080549d0a6eeb04f87b108b83647341cd63ff74c591`  
		Last Modified: Wed, 09 Apr 2025 05:42:41 GMT  
		Size: 136.4 MB (136354215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6daba6331ffa46756f10933830207f5a062cce46ad8fcf280ccfe8c868ad7e`  
		Last Modified: Wed, 09 Apr 2025 09:59:20 GMT  
		Size: 118.1 KB (118066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb904216e48550f17046fa1fd600ffbfd29af47ed65d2788d83e6ff316b9c5f3`  
		Last Modified: Wed, 09 Apr 2025 09:59:21 GMT  
		Size: 17.5 MB (17535629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0562de61263c3dd51d173292271e73df497e85517523e91539c432eddd5af002`  
		Last Modified: Wed, 09 Apr 2025 09:59:20 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a16002faa209c55e941598871a414f378c223df7caafcf92e9c53c5e9f65185`  
		Last Modified: Wed, 09 Apr 2025 09:59:20 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121f158c9dbdf25be9f88381b25edbde3b69e86d61dd2b174fcd82724c7dbbbd`  
		Last Modified: Wed, 09 Apr 2025 09:59:21 GMT  
		Size: 12.2 KB (12231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30449a0e56c60b4a09e1a14dd56489641a898132eaf1502051a5a6bd61f4311`  
		Last Modified: Wed, 09 Apr 2025 09:59:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89292ee7db792e4292427ad39a3e488d174ec23d6d1c88acbadfa49f9efd00e`  
		Last Modified: Wed, 09 Apr 2025 09:59:21 GMT  
		Size: 13.0 KB (13046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6fcfbbe3ce86d887a1ea9fd8936a7ccb002281691003b33ad83aab8fe943a5d`  
		Last Modified: Wed, 09 Apr 2025 09:59:23 GMT  
		Size: 5.4 MB (5427067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:e68e3a647adafdf092b3742411753dbc04e646f9eae3a573ee7127e86a419867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2218859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb894f2443cb56b83823df74230925204d39b5bf391e91c79fdcf3aa292bdd0b`

```dockerfile
```

-	Layers:
	-	`sha256:baf3e2fb575077bc6cfc99cfb61a6abc00ed14fd52c67d3403a423cbb6499e81`  
		Last Modified: Wed, 09 Apr 2025 09:59:20 GMT  
		Size: 2.2 MB (2180521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35b3a9cee0e4551a753887ff0b3136eecb1e7af64e37b1f7ba7918ffc4b5a975`  
		Last Modified: Wed, 09 Apr 2025 09:59:20 GMT  
		Size: 38.3 KB (38338 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:5a6e5f7ad08d895deae38adf929505a67568270a16052027848b9455b8fea505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185645422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752e0fa2dc2381ab8b76702d3ddddc080ef2f5dc73d13186be8ef0054251a6ab`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 14 Feb 2025 09:27:08 GMT
ARG RELEASE
# Fri, 14 Feb 2025 09:27:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Feb 2025 09:27:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Feb 2025 09:27:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 14 Feb 2025 09:27:08 GMT
ADD file:5d8d436f6811fd1894d694e7df7d347b9bd021b38bd57e01718331911c43a656 in / 
# Fri, 14 Feb 2025 09:27:08 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 09:27:08 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 14 Feb 2025 09:27:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_VERSION=8.0.8.40
# Fri, 14 Feb 2025 09:27:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='20797bfcc79f9a5db0b83469f9d2dc90179ca8ef69d300d1a9f461f2e0ad49e2';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cd5b5435261af9a88e900b7780b79da4faf4b5b5dc573b3eb1106eec11a5f741';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1c112c7be92f201b0ec010d23d6b590744c3435b0b0f5398e7db1a23119fd590';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='6583c6e0bb859988ac10a2135c4700aaf069181d98b0a6d80414a17a6810e6e1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 25 Mar 2025 15:38:11 GMT
USER root
# Tue, 25 Mar 2025 15:38:11 GMT
ARG VERBOSE=false
# Tue, 25 Mar 2025 15:38:11 GMT
ARG OPENJ9_SCC=true
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_VERSION=25.0.0.3
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
# Tue, 25 Mar 2025 15:38:11 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.3 org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.3 com.ibm.websphere.liberty.version=25.0.0.3
# Tue, 25 Mar 2025 15:38:11 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Tue, 25 Mar 2025 15:38:11 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.3 BuildLabel=cl250320250310-1902
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_URL
# Tue, 25 Mar 2025 15:38:11 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Tue, 25 Mar 2025 15:38:11 GMT
USER 1001
# Tue, 25 Mar 2025 15:38:11 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 25 Mar 2025 15:38:11 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 25 Mar 2025 15:38:11 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:25cf79adc8d2979d397edb23d9d8f0127bc0edfd1addfa501b8a0cc74338576b`  
		Last Modified: Mon, 07 Apr 2025 08:26:58 GMT  
		Size: 28.0 MB (28000118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6215c58d34327932bbbf6cbb5a3923233ece2ff56399c106ff3b26c6484ea063`  
		Last Modified: Wed, 09 Apr 2025 05:08:26 GMT  
		Size: 1.5 MB (1455724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a96f83eeef125d13c15be0fe185813042737a1ad8d8b818317b0b11146c6488`  
		Last Modified: Wed, 09 Apr 2025 05:08:28 GMT  
		Size: 132.5 MB (132539569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a116bd940405f04db151daccef5b90443610bb936b248996701bc25281de1560`  
		Last Modified: Wed, 09 Apr 2025 07:05:03 GMT  
		Size: 114.6 KB (114649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68d210c3f0f579f0f0fa825245400f6762f71c3cbbf608ba0b927402e327a79`  
		Last Modified: Wed, 09 Apr 2025 07:05:04 GMT  
		Size: 17.5 MB (17535054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6be77544925b26e9500ec43ff737260575dae6a9725fa80e840062fda91eac`  
		Last Modified: Wed, 09 Apr 2025 07:05:03 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcdfd2d3ed1a183e056c727134779e3ae4fdd12f572dca5f2b8e97e84faa222`  
		Last Modified: Wed, 09 Apr 2025 07:05:03 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b683239326c1bae3fe3cb0a1153c775469260b71360f560913075f0b86ba7f04`  
		Last Modified: Wed, 09 Apr 2025 07:05:04 GMT  
		Size: 12.2 KB (12231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39edd965ead9b31abc53727d6d672e0254959e4fe45977f70dffa36ca0f5aa21`  
		Last Modified: Wed, 09 Apr 2025 07:05:04 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98639789f497a0a5e51c6ab064a598ee55a43329e79a9fa6edb6db6892ce140f`  
		Last Modified: Wed, 09 Apr 2025 07:05:04 GMT  
		Size: 13.0 KB (13042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c836cea8f3cf5b09ef1d9e013b70bce6f17451960bd2930ac5fa2f14d67b786`  
		Last Modified: Wed, 09 Apr 2025 07:05:05 GMT  
		Size: 6.0 MB (5972685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:17a1ef3bb48177275155f1034cf4a88cec5222e4ab284255d41168b132d42b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d5c1baf7dae17c344c3b65ec971393da26e75970eb76a69ce6b192e6a65ad50`

```dockerfile
```

-	Layers:
	-	`sha256:0ede48689c9eaeac90616ea1a6056c70914c407d9a6125068260bf59fbc0cf11`  
		Last Modified: Wed, 09 Apr 2025 07:05:03 GMT  
		Size: 2.2 MB (2176119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b64484fe0b6b250c774b47d0a0c807842ffdde93809d9d555725653383780ca`  
		Last Modified: Wed, 09 Apr 2025 07:05:03 GMT  
		Size: 38.3 KB (38292 bytes)  
		MIME: application/vnd.in-toto+json
