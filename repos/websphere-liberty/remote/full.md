## `websphere-liberty:full`

```console
$ docker pull websphere-liberty@sha256:41bf0fb179bd243ee84132085a6989899fbcf740b2096e15a7a8f9c235b39a50
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
$ docker pull websphere-liberty@sha256:593d1b51cc738c2314099ae93548b36c5f11eff2b6717b7d816b0a8e2aa60f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.7 MB (562704416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0813972ecc0d1c44a6c4e59b5ee3ee76b58870a06a8043be9ffa0786241e031`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
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
# Wed, 11 Sep 2024 13:44:15 GMT
USER root
# Wed, 11 Sep 2024 13:44:15 GMT
ARG VERBOSE=false
# Wed, 11 Sep 2024 13:44:15 GMT
ARG OPENJ9_SCC=true
# Wed, 11 Sep 2024 13:44:15 GMT
ARG LIBERTY_VERSION=24.0.0.9
# Wed, 11 Sep 2024 13:44:15 GMT
ARG LIBERTY_BUILD_LABEL=cl241020240827-1743
# Wed, 11 Sep 2024 13:44:15 GMT
ARG LIBERTY_SHA=e0f8996103aed984661cde75149f583f80f5f91a
# Wed, 11 Sep 2024 13:44:15 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.9 org.opencontainers.image.revision=cl241020240827-1743 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 11 Sep 2024 13:44:15 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 11 Sep 2024 13:44:15 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.9 BuildLabel=cl241020240827-1743
# Wed, 11 Sep 2024 13:44:15 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.9 LIBERTY_BUILD_LABEL=cl241020240827-1743 LIBERTY_SHA=e0f8996103aed984661cde75149f583f80f5f91a
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 11 Sep 2024 13:44:15 GMT
ARG LIBERTY_URL
# Wed, 11 Sep 2024 13:44:15 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 11 Sep 2024 13:44:15 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.9 LIBERTY_BUILD_LABEL=cl241020240827-1743 LIBERTY_SHA=e0f8996103aed984661cde75149f583f80f5f91a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Sep 2024 13:44:15 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 11 Sep 2024 13:44:15 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.9 LIBERTY_BUILD_LABEL=cl241020240827-1743 LIBERTY_SHA=e0f8996103aed984661cde75149f583f80f5f91a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 11 Sep 2024 13:44:15 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 11 Sep 2024 13:44:15 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 11 Sep 2024 13:44:15 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 11 Sep 2024 13:44:15 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.9 LIBERTY_BUILD_LABEL=cl241020240827-1743 LIBERTY_SHA=e0f8996103aed984661cde75149f583f80f5f91a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 11 Sep 2024 13:44:15 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.9 LIBERTY_BUILD_LABEL=cl241020240827-1743 LIBERTY_SHA=e0f8996103aed984661cde75149f583f80f5f91a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 11 Sep 2024 13:44:15 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 11 Sep 2024 13:44:15 GMT
USER 1001
# Wed, 11 Sep 2024 13:44:15 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 11 Sep 2024 13:44:15 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 11 Sep 2024 13:44:15 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 11 Sep 2024 13:44:15 GMT
ARG VERBOSE=false
# Wed, 11 Sep 2024 13:44:15 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 11 Sep 2024 13:44:15 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Wed, 11 Sep 2024 13:44:15 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Wed, 11 Sep 2024 13:44:15 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06f8bdc5aa563a73c4f12fa33b23966ee702e684d67d02ad0f0f91fa03a0890`  
		Last Modified: Sat, 17 Aug 2024 02:04:57 GMT  
		Size: 1.4 MB (1438219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfa63a1ba8846f8a69351cc4d1774be870edf9a6bcbbe5a7c7d60905262420e`  
		Last Modified: Sat, 17 Aug 2024 02:04:59 GMT  
		Size: 135.0 MB (135014256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52736ddd2a67d18ae37aa0187c428ab38e4f74aef99b98e919e19505ebd661a7`  
		Last Modified: Thu, 12 Sep 2024 22:02:11 GMT  
		Size: 113.4 KB (113385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd518afc9545a7caf3df5e9217c9d8f5df15676cf99b9986df0af036c306ab3`  
		Last Modified: Thu, 12 Sep 2024 22:02:12 GMT  
		Size: 17.8 MB (17823713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd84f65de87f03cfdbbe684c1d60bdd577619fcfece9b3395b9e779643cf12c`  
		Last Modified: Thu, 12 Sep 2024 22:02:12 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf207a147ea21cda7a5ffcb9fe76363d57b5fc22c5ac63f6fc1f65d8586c06c5`  
		Last Modified: Thu, 12 Sep 2024 22:02:11 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11ef0c6fcdc885d7cff0fbfaceb31b4d36d250a9316b2b2204b216bf0e6e8ca`  
		Last Modified: Thu, 12 Sep 2024 22:02:12 GMT  
		Size: 11.8 KB (11835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01122166bdca07337f6c13eee7c7ef51b32abd17f58c6ad936ff87d8e0bc3824`  
		Last Modified: Thu, 12 Sep 2024 22:02:12 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b1169fcaa2bb2b62bb9842f28d84d53bdd60241820b740193e1de88ad54ea9`  
		Last Modified: Thu, 12 Sep 2024 22:02:12 GMT  
		Size: 12.6 KB (12645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aab6b16b691c1ee3da20859e7324c62aa19ab4a01cc68061d1dce25e08c8383`  
		Last Modified: Thu, 12 Sep 2024 22:02:13 GMT  
		Size: 5.8 MB (5783546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760679cbe2e402de3ff06f57b328e3764ed5aa6abd82055a3843935f9da13a6e`  
		Last Modified: Thu, 12 Sep 2024 23:13:27 GMT  
		Size: 357.4 MB (357361634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69462de778343ff2ef1bd7719dbd68954291b4f9adc7e7f2383eceeada999da`  
		Last Modified: Thu, 12 Sep 2024 23:13:16 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a9a4ab65422ccf6c9673a379370ab2a8ff15972c8689a73da391d5d06ca908`  
		Last Modified: Thu, 12 Sep 2024 23:13:17 GMT  
		Size: 15.6 MB (15605856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:10c5e41953be88ca4e65026f1cb78d79299622529c43340426b3e3d74940b9c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca85eb6fd23006fe0e86847c1b0aa281a47f0d5eb4e23848ca998d62a3bffd0`

```dockerfile
```

-	Layers:
	-	`sha256:5b30e03f161dd74985e099b90d40956632fc7cc7b7ae3907309a4146bd589e3d`  
		Last Modified: Thu, 12 Sep 2024 23:13:16 GMT  
		Size: 4.1 MB (4093058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:575e60d67742f2e8fc8c34dfd807b55bcfd939fb01a71a990b20feec34597d2d`  
		Last Modified: Thu, 12 Sep 2024 23:13:16 GMT  
		Size: 19.0 KB (19038 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:9cc97159b32b632ae8ae124718a4841f11dd9b8c8810b85e3b83f5175533413a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.0 MB (561030601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ef7159cce68a019c3d69753f92c4965a607b520f7670ce34e00b53d0604bf8`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:11 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:15 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Tue, 13 Aug 2024 09:28:15 GMT
CMD ["/bin/bash"]
# Wed, 14 Aug 2024 20:22:25 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 Aug 2024 20:22:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
ENV JAVA_VERSION=8.0.8.30
# Wed, 14 Aug 2024 20:22:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='918434b2288854235f141966710e2fe783d52a2956446dc0c6eb2902793bf068';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f84a996f9ad2aee005a670ed57a698bfcf4aff58157ec8fe2540735a87df546d';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='bb57be5b606eb9add4da90e083104979cae9fa37b0a173003c4712fc781af8bf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='e8e00b99cae3277421b8277c843f481f31ee0e2857a67cc19b97460f9136dd9a';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 14 Aug 2024 20:22:25 GMT
USER root
# Wed, 14 Aug 2024 20:22:25 GMT
ARG VERBOSE=false
# Wed, 14 Aug 2024 20:22:25 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Aug 2024 20:22:25 GMT
ARG LIBERTY_VERSION=24.0.0.8
# Wed, 14 Aug 2024 20:22:25 GMT
ARG LIBERTY_BUILD_LABEL=cl240820240729-1903
# Wed, 14 Aug 2024 20:22:25 GMT
ARG LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab
# Wed, 14 Aug 2024 20:22:25 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.8 org.opencontainers.image.revision=cl240820240729-1903 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Aug 2024 20:22:25 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 14 Aug 2024 20:22:25 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.8 BuildLabel=cl240820240729-1903
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.8 LIBERTY_BUILD_LABEL=cl240820240729-1903 LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
ARG LIBERTY_URL
# Wed, 14 Aug 2024 20:22:25 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.8 LIBERTY_BUILD_LABEL=cl240820240729-1903 LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.8 LIBERTY_BUILD_LABEL=cl240820240729-1903 LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.8 LIBERTY_BUILD_LABEL=cl240820240729-1903 LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.8 LIBERTY_BUILD_LABEL=cl240820240729-1903 LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 14 Aug 2024 20:22:25 GMT
USER 1001
# Wed, 14 Aug 2024 20:22:25 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 14 Aug 2024 20:22:25 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Aug 2024 20:22:25 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 14 Aug 2024 20:22:25 GMT
ARG VERBOSE=false
# Wed, 14 Aug 2024 20:22:25 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4e478d2a3be6bab56c5ea9225d40cb542bd132a06ee142cb3308146fe7674f`  
		Last Modified: Sat, 17 Aug 2024 01:39:03 GMT  
		Size: 1.5 MB (1523330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0126c7627e2c1fdc3f70eecee193a27c1d834c7fcf48d77fd7e0293401fb21`  
		Last Modified: Sat, 17 Aug 2024 01:39:06 GMT  
		Size: 135.5 MB (135470541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29da44496ff6ef174bc5304f5cdc0cf450a6fed9604cfe392e8a7ed399a284cf`  
		Last Modified: Sat, 17 Aug 2024 05:42:24 GMT  
		Size: 117.9 KB (117911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee541579310e5de1e4824961b81aef9e6b93c608f584c07f59c76a2556e1ddd`  
		Last Modified: Sat, 17 Aug 2024 05:42:26 GMT  
		Size: 17.4 MB (17422705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79f7c30167c24e41e327cb96ffc7cb45efbbbb6800f9fd2c73d3ac774bc5dc6`  
		Last Modified: Sat, 17 Aug 2024 05:42:24 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79962fbc9962641c3279404c67ef32c72ca8e95e870573ee0bd38acada5cc64d`  
		Last Modified: Sat, 17 Aug 2024 05:42:24 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadc02c1b786d2014756a30c8dfa5071e05cbbe6312ad984075fc3d31a21cb5b`  
		Last Modified: Sat, 17 Aug 2024 05:42:25 GMT  
		Size: 11.8 KB (11839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6a73820ca2bec5bcf91773c8425409776b3a8c7e9ef1660bfd57ebd0251ea7`  
		Last Modified: Sat, 17 Aug 2024 05:42:25 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d264c9e7fab3f732d20161d573265c3449c1ca81228f9d87bc4cc3dcc47c762`  
		Last Modified: Sat, 17 Aug 2024 05:42:25 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8024cc2a625fadded1fb35e0744db670e88c2916e23841551b580bfeeb43365d`  
		Last Modified: Sat, 17 Aug 2024 05:42:27 GMT  
		Size: 5.3 MB (5275543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d5d84fed133517fcfef38148409a294526c8479afea5858419b375ff9f4fbc`  
		Last Modified: Sat, 17 Aug 2024 09:51:36 GMT  
		Size: 353.4 MB (353433990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d458145a0f5cbf4ad94a589fbf036a0195e13c9fc1ae2ab49e7acb9931200ee2`  
		Last Modified: Sat, 17 Aug 2024 09:51:24 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a36c1c69a98795c224dbe0833f23b6585897d0bb08292bc7acd96bbe83cd7a`  
		Last Modified: Sat, 17 Aug 2024 09:51:25 GMT  
		Size: 13.3 MB (13294605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:1d8dc7ef6e4755d5d285eb71baa587a4cc2b7c830ba98c29da7859d1118237d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4094830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71d2b2d952a06f471c243dd85c4c92bee45491602fc13cffba7ccdff266582f`

```dockerfile
```

-	Layers:
	-	`sha256:fdd440d39b3a216434b9a1e1676a3365c36a6676815fc392ced6555cc7c17acb`  
		Last Modified: Sat, 17 Aug 2024 09:51:24 GMT  
		Size: 4.1 MB (4075752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64db0dc65f35dc4d25c8ad03c5f9068493a321dfacfde6b14f105dacfd93f401`  
		Last Modified: Sat, 17 Aug 2024 09:51:23 GMT  
		Size: 19.1 KB (19078 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:00a4658eb77990023e241d0d069540778bffc08887bcf5038d872034d0becda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.9 MB (553902377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5083e11e1d306ec03c7f5f939b6dac32dca8e1a8ce1079833036b5e5f8d4bc52`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:24 GMT
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
# Tue, 13 Aug 2024 09:28:24 GMT
CMD ["/bin/bash"]
# Wed, 14 Aug 2024 20:22:25 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 Aug 2024 20:22:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
ENV JAVA_VERSION=8.0.8.30
# Wed, 14 Aug 2024 20:22:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='918434b2288854235f141966710e2fe783d52a2956446dc0c6eb2902793bf068';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f84a996f9ad2aee005a670ed57a698bfcf4aff58157ec8fe2540735a87df546d';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='bb57be5b606eb9add4da90e083104979cae9fa37b0a173003c4712fc781af8bf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='e8e00b99cae3277421b8277c843f481f31ee0e2857a67cc19b97460f9136dd9a';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 14 Aug 2024 20:22:25 GMT
USER root
# Wed, 14 Aug 2024 20:22:25 GMT
ARG VERBOSE=false
# Wed, 14 Aug 2024 20:22:25 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Aug 2024 20:22:25 GMT
ARG LIBERTY_VERSION=24.0.0.8
# Wed, 14 Aug 2024 20:22:25 GMT
ARG LIBERTY_BUILD_LABEL=cl240820240729-1903
# Wed, 14 Aug 2024 20:22:25 GMT
ARG LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab
# Wed, 14 Aug 2024 20:22:25 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.8 org.opencontainers.image.revision=cl240820240729-1903 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Aug 2024 20:22:25 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 14 Aug 2024 20:22:25 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.8 BuildLabel=cl240820240729-1903
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.8 LIBERTY_BUILD_LABEL=cl240820240729-1903 LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
ARG LIBERTY_URL
# Wed, 14 Aug 2024 20:22:25 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.8 LIBERTY_BUILD_LABEL=cl240820240729-1903 LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.8 LIBERTY_BUILD_LABEL=cl240820240729-1903 LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.8 LIBERTY_BUILD_LABEL=cl240820240729-1903 LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.8 LIBERTY_BUILD_LABEL=cl240820240729-1903 LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 14 Aug 2024 20:22:25 GMT
USER 1001
# Wed, 14 Aug 2024 20:22:25 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 14 Aug 2024 20:22:25 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Aug 2024 20:22:25 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 14 Aug 2024 20:22:25 GMT
ARG VERBOSE=false
# Wed, 14 Aug 2024 20:22:25 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:e280dadf5b2aeff3eee5ef7e055d95037f9fdf834a26d90fa2a2127a91d7cf49`  
		Last Modified: Tue, 13 Aug 2024 10:45:20 GMT  
		Size: 28.0 MB (28001322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bd23a2bae158f6db334cabf77fa6c837c47102c7aa7f55dc0c5bba3d8a9928`  
		Last Modified: Sat, 17 Aug 2024 02:32:13 GMT  
		Size: 1.4 MB (1441904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808f3238c3f6757b06376048a60f6fa222d812b6857cbe88081b9c0af6a97080`  
		Last Modified: Sat, 17 Aug 2024 02:32:15 GMT  
		Size: 131.9 MB (131936932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2423ac912b86f82954408793392a6a428542a2c5149c55181c8a26945413c9`  
		Last Modified: Sat, 17 Aug 2024 05:12:35 GMT  
		Size: 114.7 KB (114688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f86236f563be208f42401d92701c49f93c7c6aed7c8e2b97b8571b84fa3912`  
		Last Modified: Sat, 17 Aug 2024 05:12:35 GMT  
		Size: 17.4 MB (17422354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee59423fef8deb09c787e49e44d1e71f1ae4fd0f35c6e52f58de054c5004b46`  
		Last Modified: Sat, 17 Aug 2024 05:12:35 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2d56e1e0ee6a010e11d5b3b43a74433f0276713a6d9e3597c82ec60100d281`  
		Last Modified: Sat, 17 Aug 2024 05:12:35 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58540a8fd9066b07484c170048f5500e7d52ee69372db6e0c7ad9b89cb92647`  
		Last Modified: Sat, 17 Aug 2024 05:12:36 GMT  
		Size: 11.8 KB (11829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b8166ea5112e03b744477f11156affe5b94d9b5d9849b8ce911b6ff99e3f5f`  
		Last Modified: Sat, 17 Aug 2024 05:12:36 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e11cc914f517bdcd7a57a36ae918ae60efc79e71707f817b4375ffbcb43941`  
		Last Modified: Sat, 17 Aug 2024 05:12:36 GMT  
		Size: 12.6 KB (12643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a79c4b302a48a3920ba225834afac39995123c92365b248209696b6ee21764`  
		Last Modified: Sat, 17 Aug 2024 05:12:36 GMT  
		Size: 5.9 MB (5880626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e1d5dc87ab6db910e3ddb5db688e5e5b94096f38a4389dc385eda617e802692`  
		Last Modified: Sat, 17 Aug 2024 06:24:03 GMT  
		Size: 353.4 MB (353433004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93c78b0d23f7442dd2a4c5d197efdadaecf80a36b7684948ed0c16e9a2917f8`  
		Last Modified: Sat, 17 Aug 2024 06:23:58 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4488af67ca2e5312e85d03123d9d76a6e0b82aa7127846b7f0ca97d25ff3d082`  
		Last Modified: Sat, 17 Aug 2024 06:23:59 GMT  
		Size: 15.6 MB (15643789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:572eee02e8b4509276a6cf7ac95375e24064b78a04c1eaee2c5e312392fe92d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4090607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7448e037a72ac784a4184119f70c4ba3e1b583f981ee70f162550acc7dbe16b`

```dockerfile
```

-	Layers:
	-	`sha256:84df92ada05e326f4203ea1cbe99a2492ee028d474901d30c59a80baadf119e5`  
		Last Modified: Sat, 17 Aug 2024 06:23:57 GMT  
		Size: 4.1 MB (4071569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86aee6413aca6ea15a032d541f85ae9a5e772593845c54a2dd23baf75253651b`  
		Last Modified: Sat, 17 Aug 2024 06:23:57 GMT  
		Size: 19.0 KB (19038 bytes)  
		MIME: application/vnd.in-toto+json
