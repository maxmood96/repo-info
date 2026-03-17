## `websphere-liberty:latest`

```console
$ docker pull websphere-liberty@sha256:b406070c9970cc95950f01f3cd8fee09f54605296148e54b87178fef7eb14c6b
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
$ docker pull websphere-liberty@sha256:afc33b4e902ba46faa5597d6b5fa5c92eeaaa367a06d8093c5644126694a1179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.1 MB (574113982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a1e1c2a352b0a88b351d17468fd1492fa98cd2125e5c01ee0a9c971b906894`
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
# Tue, 17 Mar 2026 02:54:22 GMT
USER root
# Tue, 17 Mar 2026 02:54:22 GMT
ARG VERBOSE=false
# Tue, 17 Mar 2026 02:54:22 GMT
ARG OPENJ9_SCC=true
# Tue, 17 Mar 2026 02:54:22 GMT
ARG LIBERTY_VERSION=26.0.0.2
# Tue, 17 Mar 2026 02:54:22 GMT
ARG LIBERTY_BUILD_LABEL=cl260220260207-1901
# Tue, 17 Mar 2026 02:54:22 GMT
ARG LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25
# Tue, 17 Mar 2026 02:54:22 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.2 org.opencontainers.image.revision=cl260220260207-1901 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.2 com.ibm.websphere.liberty.version=26.0.0.2
# Tue, 17 Mar 2026 02:54:22 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Tue, 17 Mar 2026 02:54:22 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.2 BuildLabel=cl260220260207-1901
# Tue, 17 Mar 2026 02:54:22 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 17 Mar 2026 02:54:22 GMT
ARG LIBERTY_URL
# Tue, 17 Mar 2026 02:54:22 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 17 Mar 2026 02:54:37 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:54:37 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 17 Mar 2026 02:54:38 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 17 Mar 2026 02:54:38 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 17 Mar 2026 02:54:38 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 17 Mar 2026 02:54:38 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 17 Mar 2026 02:54:38 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Tue, 17 Mar 2026 02:54:44 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 17 Mar 2026 02:54:44 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Tue, 17 Mar 2026 02:54:44 GMT
USER 1001
# Tue, 17 Mar 2026 02:54:44 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 17 Mar 2026 02:54:44 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 17 Mar 2026 02:54:44 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 17 Mar 2026 03:42:21 GMT
ARG VERBOSE=false
# Tue, 17 Mar 2026 03:42:21 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 17 Mar 2026 03:42:21 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Tue, 17 Mar 2026 03:42:22 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Tue, 17 Mar 2026 03:42:44 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
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
	-	`sha256:951e914f93a4d8f2ba1409506fcbb2f186aa29a614d4c9a3d7f1eb7fab8f9736`  
		Last Modified: Tue, 17 Mar 2026 02:54:53 GMT  
		Size: 113.7 KB (113666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeddb3241647f252889c53e324be77a7c45ead3c9fde153a317a44d92b0cbb13`  
		Last Modified: Tue, 17 Mar 2026 02:54:54 GMT  
		Size: 18.0 MB (18035650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee37c6ca4ad63a099f5f186ba623a253601ba1831c76e1e37dc2b873ae53cb57`  
		Last Modified: Tue, 17 Mar 2026 02:54:53 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5eb8b93f62c3c95785307788b05a2356b53c9505f6bf603208239eb764ce56c`  
		Last Modified: Tue, 17 Mar 2026 02:54:53 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40d8432009a0c616018b94f94a03f44df93045039f54cc3fa96aef7c5e7dd06`  
		Last Modified: Tue, 17 Mar 2026 02:54:54 GMT  
		Size: 14.1 KB (14118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1672e6eb018a06de49fbf3707f018af7d9ec95022ee7ccd147e866e37f50f9`  
		Last Modified: Tue, 17 Mar 2026 02:54:54 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7787555450327d8fe1cd64dd85a71a6f913dee8ed52e11a6c94fc9fb0cc6134c`  
		Last Modified: Tue, 17 Mar 2026 02:54:54 GMT  
		Size: 15.0 KB (14981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2346278e055403e1087502275bc4d8e2a436680d7638f8a3a3505ad224208f1b`  
		Last Modified: Tue, 17 Mar 2026 02:54:55 GMT  
		Size: 5.8 MB (5765379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbab0850c1d29d66ee4e3c969680671f0f43f3a6e7e32d73a394a7df06bf97aa`  
		Last Modified: Tue, 17 Mar 2026 03:43:18 GMT  
		Size: 367.8 MB (367826478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874a4d7c0592787584824adda34c3cee5100086664504e21e39237aeecabf27f`  
		Last Modified: Tue, 17 Mar 2026 03:43:11 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd67ba5e6c4cc66312692cc2610332e8f62caa025ac38f8ec175e0a856e5df53`  
		Last Modified: Tue, 17 Mar 2026 03:43:11 GMT  
		Size: 15.5 MB (15547468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:latest` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:4fbd7ef725a6b76dcb83ef7ea22621a814c56ec37634b8102e5cc4d665172762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4382600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f14420643561bc56536714bb18bc1d6b37253e18eb03f565d0c02713d173b08`

```dockerfile
```

-	Layers:
	-	`sha256:e382693eb7704b9094bb39b23117ec5fa2c9aa5b002d6cfa940b2459fb256328`  
		Last Modified: Tue, 17 Mar 2026 03:43:11 GMT  
		Size: 4.4 MB (4363505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b9fc3f072ad55a78b796c312c36d967f64bc966f4b0df562cae733c17f1b3bb`  
		Last Modified: Tue, 17 Mar 2026 03:43:10 GMT  
		Size: 19.1 KB (19095 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:latest` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:5a2d43c75b420bc14a4f4111642a76c9e1707022fa11b84a831e9ebb7d28b028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.5 MB (577482009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c894ec52dcd107f84f4942f7a0c944a226ef2dbb7fbd8e34dee24ab7135b11`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 10 Feb 2026 17:41:33 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:41:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:41:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:41:33 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:41:39 GMT
ADD file:0418bf4995f9b54380cc1e509e3f7d65bb07aed9a367528d0b1084f0a34f3bf3 in / 
# Tue, 10 Feb 2026 17:41:39 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:45:09 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Feb 2026 20:45:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:45:09 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Feb 2026 21:21:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0a965c513bb522004ddb195fbb3cda7124559b8c7c082fc8626b2f45b4ce9a94';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ebf5f90f77e524593cba310d9e73d993bc8d3357af0127ec4627b1ce8236f385';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8353fb367a56fd150bd5b1facb595bde690c9f9a1f3db7db3b7fb240399a6ae9';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Feb 2026 21:21:46 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 25 Feb 2026 05:27:40 GMT
USER root
# Wed, 25 Feb 2026 05:27:40 GMT
ARG VERBOSE=false
# Wed, 25 Feb 2026 05:27:40 GMT
ARG OPENJ9_SCC=true
# Wed, 25 Feb 2026 05:27:40 GMT
ARG LIBERTY_VERSION=26.0.0.2
# Wed, 25 Feb 2026 05:27:40 GMT
ARG LIBERTY_BUILD_LABEL=cl260220260207-1901
# Wed, 25 Feb 2026 05:27:40 GMT
ARG LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25
# Wed, 25 Feb 2026 05:27:40 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.2 org.opencontainers.image.revision=cl260220260207-1901 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.2 com.ibm.websphere.liberty.version=26.0.0.2
# Wed, 25 Feb 2026 05:27:40 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Wed, 25 Feb 2026 05:27:40 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.2 BuildLabel=cl260220260207-1901
# Wed, 25 Feb 2026 05:27:40 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 25 Feb 2026 05:27:40 GMT
ARG LIBERTY_URL
# Wed, 25 Feb 2026 05:27:40 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 25 Feb 2026 05:27:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 05:27:59 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 25 Feb 2026 05:28:01 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 25 Feb 2026 05:28:01 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 25 Feb 2026 05:28:01 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 25 Feb 2026 05:28:02 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 25 Feb 2026 05:28:03 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Wed, 25 Feb 2026 05:28:14 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 25 Feb 2026 05:28:14 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 25 Feb 2026 05:28:14 GMT
USER 1001
# Wed, 25 Feb 2026 05:28:14 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 25 Feb 2026 05:28:14 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 25 Feb 2026 05:28:14 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 25 Feb 2026 06:39:42 GMT
ARG VERBOSE=false
# Wed, 25 Feb 2026 06:39:42 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 25 Feb 2026 06:39:42 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Wed, 25 Feb 2026 06:39:43 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Wed, 25 Feb 2026 06:40:33 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:95401e425d899946469007a0ce4b02622cf84a67cdd684aa25d61d472fffc38f`  
		Last Modified: Tue, 10 Feb 2026 18:13:52 GMT  
		Size: 34.4 MB (34446102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7ba9d1b5a555762e1b63722491095f4d355bdcb4e2da1b884c931a246213b8`  
		Last Modified: Tue, 17 Feb 2026 20:45:40 GMT  
		Size: 1.5 MB (1536160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d44ee8635cbba8a480cc5afe52ee3f84cdc9521d2eecd6e04ec20444d16d0a`  
		Last Modified: Tue, 17 Feb 2026 21:22:20 GMT  
		Size: 136.7 MB (136749855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3722c9db7e843af4ebcba14ae95afb4f1f1c13cfbed42a03e401d5ca726df3b7`  
		Last Modified: Wed, 25 Feb 2026 05:28:36 GMT  
		Size: 118.1 KB (118075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca5a64fce089da95571b257d375c15a3a476f8808fc062860b2eaab2c20e556`  
		Last Modified: Wed, 25 Feb 2026 05:28:37 GMT  
		Size: 18.0 MB (18035942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b131e2bd84413bb3f735605c4a504a355664150e383d780d22ab0610cebf64ef`  
		Last Modified: Wed, 25 Feb 2026 05:28:36 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca71253c3489e1ef3a75dfe4dc7fdc9c294179a3cc99704b1bd4fd9c59cc0936`  
		Last Modified: Wed, 25 Feb 2026 05:28:36 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa22c3d61baaba3e4bec8233a8686ce31982595774a771c7dc5b3220bbd53693`  
		Last Modified: Wed, 25 Feb 2026 05:28:37 GMT  
		Size: 14.1 KB (14123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98c3043323319c3dd156cb4553706884ac9ac608ba2a0f85f5449df8cc8b53e`  
		Last Modified: Wed, 25 Feb 2026 05:28:37 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32362d1df8e3016e329e28b03aa3a1b8a7fa7d1c01c10b2619c6ef2f96b0eefe`  
		Last Modified: Wed, 25 Feb 2026 05:28:37 GMT  
		Size: 15.0 KB (15007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05ad5c2dc9dcc363d22def7ca903b013ad594f5536135e51bd58746c602a0dd`  
		Last Modified: Wed, 25 Feb 2026 05:28:39 GMT  
		Size: 5.5 MB (5473098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e07fed4d7acc272132ec7c0f7c9d8eec20ae2abfb08db049c09b92638fe330`  
		Last Modified: Wed, 25 Feb 2026 06:42:08 GMT  
		Size: 367.8 MB (367826222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2f7d52ad3bddba30291942ec084c4a4ef77d838f1608e992878dd9c372a7c0`  
		Last Modified: Wed, 25 Feb 2026 06:42:00 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6150a02fe31f5805523394b7c1d5bc1c17662b0cb169f7f796068b6ab1c7c2fe`  
		Last Modified: Wed, 25 Feb 2026 06:42:00 GMT  
		Size: 13.3 MB (13264121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:latest` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:df2393c78aa45543c0b8dd528e8fe4f31c3995b7857299afa24e49f401b3bc36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4385915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ee63df9b143a336a2322301c5a1aa92cec55ebaec0f9ea1c4d1c6e21c320669`

```dockerfile
```

-	Layers:
	-	`sha256:d5570cac4ee0f989c684d85b5f20da474563944d9017da3d52f62d116f7f04c6`  
		Last Modified: Wed, 25 Feb 2026 06:42:00 GMT  
		Size: 4.4 MB (4366780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6a87578576da17effedb2a384842d0d9ef9408c54bb62e0690ea05215828c55`  
		Last Modified: Wed, 25 Feb 2026 06:42:00 GMT  
		Size: 19.1 KB (19135 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:latest` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:5fab6943be6e687a79fe4e3442fa0e6235ba8a87abde51d5d06a3ad0a8ba7bd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.5 MB (570474298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8413a38fba5ee02e2d7d9afc655488ab84df0358931becc7dacaa0861728da7`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 10 Feb 2026 17:41:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:41:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:41:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:41:31 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:41:33 GMT
ADD file:682bbddd1f3d784d0c4ab5eef9460f0b47a94f3c62f629b59163a7f6543a159f in / 
# Tue, 10 Feb 2026 17:41:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:25:49 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Feb 2026 20:25:49 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:25:49 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Feb 2026 20:26:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0a965c513bb522004ddb195fbb3cda7124559b8c7c082fc8626b2f45b4ce9a94';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ebf5f90f77e524593cba310d9e73d993bc8d3357af0127ec4627b1ce8236f385';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8353fb367a56fd150bd5b1facb595bde690c9f9a1f3db7db3b7fb240399a6ae9';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Feb 2026 20:26:39 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 25 Feb 2026 01:08:57 GMT
USER root
# Wed, 25 Feb 2026 01:08:57 GMT
ARG VERBOSE=false
# Wed, 25 Feb 2026 01:08:57 GMT
ARG OPENJ9_SCC=true
# Wed, 25 Feb 2026 01:08:57 GMT
ARG LIBERTY_VERSION=26.0.0.2
# Wed, 25 Feb 2026 01:08:57 GMT
ARG LIBERTY_BUILD_LABEL=cl260220260207-1901
# Wed, 25 Feb 2026 01:08:57 GMT
ARG LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25
# Wed, 25 Feb 2026 01:08:57 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.2 org.opencontainers.image.revision=cl260220260207-1901 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.2 com.ibm.websphere.liberty.version=26.0.0.2
# Wed, 25 Feb 2026 01:08:57 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Wed, 25 Feb 2026 01:08:57 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.2 BuildLabel=cl260220260207-1901
# Wed, 25 Feb 2026 01:08:57 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 25 Feb 2026 01:08:57 GMT
ARG LIBERTY_URL
# Wed, 25 Feb 2026 01:08:57 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 25 Feb 2026 01:09:15 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 01:09:15 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 25 Feb 2026 01:09:17 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 25 Feb 2026 01:09:17 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 25 Feb 2026 01:09:18 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 25 Feb 2026 01:09:18 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 25 Feb 2026 01:09:21 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Wed, 25 Feb 2026 01:09:33 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 25 Feb 2026 01:09:33 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 25 Feb 2026 01:09:33 GMT
USER 1001
# Wed, 25 Feb 2026 01:09:33 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 25 Feb 2026 01:09:33 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 25 Feb 2026 01:09:33 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 25 Feb 2026 02:30:13 GMT
ARG VERBOSE=false
# Wed, 25 Feb 2026 02:30:13 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 25 Feb 2026 02:30:13 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Wed, 25 Feb 2026 02:30:14 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Wed, 25 Feb 2026 02:30:44 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:4e2905dbd81d6a42c24ec5f7ce51f2d8f24a616b4fe2e90d0be791922a8d3b5f`  
		Last Modified: Tue, 10 Feb 2026 18:14:06 GMT  
		Size: 28.0 MB (28004382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77d17bf550a6cfe5ae28c00f12c4faa501f3dcc6d38bb384909465bb4f46478`  
		Last Modified: Tue, 17 Feb 2026 20:27:06 GMT  
		Size: 1.5 MB (1455847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbf297943659132d399cdba79372f26c58e6fba15ec4b1c07aa432bc5db1b72`  
		Last Modified: Tue, 17 Feb 2026 20:27:09 GMT  
		Size: 133.3 MB (133270713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd566d1f28f6ab64983b3e36ab1c9996a0a502eea9765f8259bb364af038848`  
		Last Modified: Wed, 25 Feb 2026 01:10:13 GMT  
		Size: 114.8 KB (114773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c945991f658d6b545c372dc9faee443020f050556492cafb82a4bf424e534dcf`  
		Last Modified: Wed, 25 Feb 2026 01:10:13 GMT  
		Size: 18.0 MB (18035600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b49bf6a6ca28586418e06a94a582b4cabd81b4c2b0745e92fe540b691a0fe6`  
		Last Modified: Wed, 25 Feb 2026 01:10:13 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6474cc8ee4ab9e6c94549c967fb9f3f0fd8f7c6754c70ee8cc69a695645717de`  
		Last Modified: Wed, 25 Feb 2026 01:10:12 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04e2bd1d1335a297efedc2bc34676a1f58990c579e8e66de8d1efdac7fedfed`  
		Last Modified: Wed, 25 Feb 2026 01:10:13 GMT  
		Size: 14.1 KB (14122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023e80c10956ef08101f961ddee418b768b7d0ea94e15e3348b3dd240e117a1d`  
		Last Modified: Wed, 25 Feb 2026 01:10:14 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee060d92aee7d3d968ac4f939bd321b1e9beccdcd160e78f5acc1be16e30b03c`  
		Last Modified: Wed, 25 Feb 2026 01:10:14 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb22649ee742f9e37198b5f478811f06b07c5e83146de6e1246f4694017223d7`  
		Last Modified: Wed, 25 Feb 2026 01:10:14 GMT  
		Size: 6.2 MB (6222059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5873dcec2ef85b0785b118ac4515086a3ede0b2115a4c0f477493256df59cc`  
		Last Modified: Wed, 25 Feb 2026 02:31:45 GMT  
		Size: 367.8 MB (367826699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e94ddff31861e25a2fc95e05d39875b5529b10fb3739b33f22047084877f2f`  
		Last Modified: Wed, 25 Feb 2026 02:31:39 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5724ea7e7ab45ffcf6898c7b75a0a9fa712072c2de68266f12e395e619d85a`  
		Last Modified: Wed, 25 Feb 2026 02:31:39 GMT  
		Size: 15.5 MB (15511789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:latest` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:f5fb99d45cc15f46761a1187c1997c0be9ac817c1d9c7363fb2a8b04f397c624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f15447f6d4abf9d0f189e015591c7b973f608fd563b8889fde7d942f35141c`

```dockerfile
```

-	Layers:
	-	`sha256:73a17915e330cacbab2dd29fa065962c5f9f95da18147a2cb37d5dafcf13c793`  
		Last Modified: Wed, 25 Feb 2026 02:31:39 GMT  
		Size: 4.4 MB (4362266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f1359a0b05c4072041b602a5f48a77c7588c13183ef45798761e62b1f3a7627`  
		Last Modified: Wed, 25 Feb 2026 02:31:39 GMT  
		Size: 19.1 KB (19094 bytes)  
		MIME: application/vnd.in-toto+json
