## `websphere-liberty:latest`

```console
$ docker pull websphere-liberty@sha256:8230a6354822395b048cb9ff7194a29238cd09afcd7a45b53ef80b5c4b0322d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	linux; s390x
	-	unknown; unknown

### `websphere-liberty:latest` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:5f9469e0c4d9e3219803f1e3b127e692bcdd086cc1f5f26e3b974a8c7f42822a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.2 MB (555228040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40190c51cef90fa5d2fb7426de16e7ed022ecbe3fb4921f0b1492ed68ae8c67d`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 09 May 2024 05:12:02 GMT
ARG RELEASE
# Thu, 09 May 2024 05:12:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 09 May 2024 05:12:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 09 May 2024 05:12:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 09 May 2024 05:12:02 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Thu, 09 May 2024 05:12:02 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 05:12:02 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 09 May 2024 05:12:02 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 05:12:02 GMT
ENV JAVA_VERSION=8.0.8.25
# Thu, 09 May 2024 05:12:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='82be3936ccd4acbba83fdea2302770fa9a89266829fa2ff22c06b11e616281c0';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='7892771ebe4ee2988988031bf504b054c41fdc905fefc87c53d7bc499d7b44fa';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='55647d87f192db41e52e8cc5ea517266a0bded42e3c326cf2e8f03a64a473a96';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='dc1ffb2b769a6a08f161b801f7dfd413400d9cfcebed3c6e7229d48dd1a52bad';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 09 May 2024 05:12:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 18 Jun 2024 18:55:44 GMT
USER root
# Tue, 18 Jun 2024 18:55:44 GMT
ARG VERBOSE=false
# Tue, 18 Jun 2024 18:55:44 GMT
ARG OPENJ9_SCC=true
# Tue, 18 Jun 2024 18:55:44 GMT
ARG LIBERTY_VERSION=24.0.0.6
# Tue, 18 Jun 2024 18:55:44 GMT
ARG LIBERTY_BUILD_LABEL=cl240620240603-2001
# Tue, 18 Jun 2024 18:55:44 GMT
ARG LIBERTY_SHA=e2daf941ebdf3908d50bb1288c1574ccfd454796
# Tue, 18 Jun 2024 18:55:44 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.6 org.opencontainers.image.revision=cl240620240603-2001 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Tue, 18 Jun 2024 18:55:44 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Tue, 18 Jun 2024 18:55:44 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.6 BuildLabel=cl240620240603-2001
# Tue, 18 Jun 2024 18:55:44 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.6 LIBERTY_BUILD_LABEL=cl240620240603-2001 LIBERTY_SHA=e2daf941ebdf3908d50bb1288c1574ccfd454796
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 18 Jun 2024 18:55:44 GMT
ARG LIBERTY_URL
# Tue, 18 Jun 2024 18:55:44 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 18 Jun 2024 18:55:44 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.6 LIBERTY_BUILD_LABEL=cl240620240603-2001 LIBERTY_SHA=e2daf941ebdf3908d50bb1288c1574ccfd454796 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 18:55:44 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 18 Jun 2024 18:55:44 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.6 LIBERTY_BUILD_LABEL=cl240620240603-2001 LIBERTY_SHA=e2daf941ebdf3908d50bb1288c1574ccfd454796 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 18 Jun 2024 18:55:44 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 18 Jun 2024 18:55:44 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 18 Jun 2024 18:55:44 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 18 Jun 2024 18:55:44 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.6 LIBERTY_BUILD_LABEL=cl240620240603-2001 LIBERTY_SHA=e2daf941ebdf3908d50bb1288c1574ccfd454796 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Tue, 18 Jun 2024 18:55:44 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.6 LIBERTY_BUILD_LABEL=cl240620240603-2001 LIBERTY_SHA=e2daf941ebdf3908d50bb1288c1574ccfd454796 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 18 Jun 2024 18:55:44 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Tue, 18 Jun 2024 18:55:44 GMT
USER 1001
# Tue, 18 Jun 2024 18:55:44 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 18 Jun 2024 18:55:44 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 18 Jun 2024 18:55:44 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 18 Jun 2024 18:55:44 GMT
ARG VERBOSE=false
# Tue, 18 Jun 2024 18:55:44 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 18 Jun 2024 18:55:44 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Tue, 18 Jun 2024 18:55:44 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Tue, 18 Jun 2024 18:55:44 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfb9852b79dffd5d428110be3cb4bf7d4ae580d42cd7a2c00ec3163f5832667`  
		Last Modified: Tue, 25 Jun 2024 22:57:22 GMT  
		Size: 1.5 MB (1469310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8dc5494e972e03d226df580d37885081680fb879c71d3a270c277c04d388168`  
		Last Modified: Tue, 25 Jun 2024 22:57:24 GMT  
		Size: 135.0 MB (135005940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77320abf53202ab84be207b43400535206bb4fb7a4ed801933b8e3f07936076c`  
		Last Modified: Tue, 25 Jun 2024 23:56:21 GMT  
		Size: 113.3 KB (113327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbeb8f4fc60958552a56d4a613ad1ac5572dfb558dc226556dafcfbb65789d37`  
		Last Modified: Tue, 25 Jun 2024 23:56:22 GMT  
		Size: 17.4 MB (17375263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3054ea497e6c988a1d9971108fcdf2c69812ab002f65dac3d1d4d5c8d856f441`  
		Last Modified: Tue, 25 Jun 2024 23:56:22 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9295477b7319b08e7daff94113b5973af8915a81f2a6f2896fa10bc3d01a88e`  
		Last Modified: Tue, 25 Jun 2024 23:56:21 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212d756b10fd925bb1ecec273c30231dd996b81e39e31b09933482c69c88d531`  
		Last Modified: Tue, 25 Jun 2024 23:56:23 GMT  
		Size: 11.8 KB (11838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36dc01bd32cfaf49264bbd42cc17646188225210b7d51475d9f803ce1f9e0566`  
		Last Modified: Tue, 25 Jun 2024 23:56:22 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bc025d6e35e524356b680cda275e57fac496c8f502884bbba072b87000e268`  
		Last Modified: Tue, 25 Jun 2024 23:56:22 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a8db1226859ba38cb3062cb0e285e953365274188ec327d8dc9e261bae8dfd`  
		Last Modified: Tue, 25 Jun 2024 23:56:23 GMT  
		Size: 5.8 MB (5796787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecff5709bb13c7af98c5c837b53a42e5a9b88f3ad2e2c7535ad74d2c4005e0d`  
		Last Modified: Wed, 26 Jun 2024 01:05:42 GMT  
		Size: 350.2 MB (350204545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0fc2cab43d4f923e7a8a79fa68e3c1dfc6a6f1537f42229a92abb9b3acfc6c`  
		Last Modified: Wed, 26 Jun 2024 01:05:37 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea162c169a07fc0331e43b29714b3293b384bc2974d4027380fdbd4b5762dad9`  
		Last Modified: Wed, 26 Jun 2024 01:05:37 GMT  
		Size: 15.7 MB (15701320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:latest` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:a3383a3c0bb861f1714fbb74388b1f6086c3716be399f77ced307e15a08fb70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a5b439a08830d65fabd230f0a0b136c625f4a9391d892df55710e26d81b7a47`

```dockerfile
```

-	Layers:
	-	`sha256:45b59c938d5060eb06e6ffcd5fd6f6d07ffee50d8d36a17b65ca478fe9fb334e`  
		Last Modified: Wed, 26 Jun 2024 01:05:37 GMT  
		Size: 3.8 MB (3823562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0d4c6570cde45b147e05c447c32a60ed6fbea72ee7e0a7adb7fb6ec8d2d452e`  
		Last Modified: Wed, 26 Jun 2024 01:05:37 GMT  
		Size: 19.0 KB (19038 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:latest` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:69368c24bb2790e04150944f63e2664f85d741b285752c794a300f7bd664c4d4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.2 MB (559155776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c625183df3f93fb48c45b8b9c32d2cc9f500e62e07e304f8657f7e0991164580`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 03 Jun 2024 10:34:18 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:34:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:34:22 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 10:34:22 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:05:55 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 05 Jun 2024 04:06:05 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:06:05 GMT
ENV JAVA_VERSION=8.0.8.25
# Wed, 05 Jun 2024 04:06:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='82be3936ccd4acbba83fdea2302770fa9a89266829fa2ff22c06b11e616281c0';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='7892771ebe4ee2988988031bf504b054c41fdc905fefc87c53d7bc499d7b44fa';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='55647d87f192db41e52e8cc5ea517266a0bded42e3c326cf2e8f03a64a473a96';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='dc1ffb2b769a6a08f161b801f7dfd413400d9cfcebed3c6e7229d48dd1a52bad';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz;
# Wed, 05 Jun 2024 04:06:18 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 05 Jun 2024 08:16:11 GMT
USER root
# Wed, 05 Jun 2024 08:16:11 GMT
ARG VERBOSE=false
# Wed, 05 Jun 2024 08:16:12 GMT
ARG OPENJ9_SCC=true
# Tue, 18 Jun 2024 23:49:21 GMT
ARG LIBERTY_VERSION=24.0.0.6
# Tue, 18 Jun 2024 23:49:22 GMT
ARG LIBERTY_BUILD_LABEL=cl240620240603-2001
# Tue, 18 Jun 2024 23:49:22 GMT
ARG LIBERTY_SHA=e2daf941ebdf3908d50bb1288c1574ccfd454796
# Tue, 18 Jun 2024 23:49:23 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.6 org.opencontainers.image.revision=cl240620240603-2001 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Tue, 18 Jun 2024 23:49:23 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Tue, 18 Jun 2024 23:49:23 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.6 BuildLabel=cl240620240603-2001
# Tue, 18 Jun 2024 23:49:46 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240620240603-2001 LIBERTY_SHA=e2daf941ebdf3908d50bb1288c1574ccfd454796 LIBERTY_VERSION=24.0.0.6 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*;
# Tue, 18 Jun 2024 23:49:46 GMT
ARG LIBERTY_URL
# Tue, 18 Jun 2024 23:49:47 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 18 Jun 2024 23:49:58 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240620240603-2001 LIBERTY_SHA=e2daf941ebdf3908d50bb1288c1574ccfd454796 LIBERTY_VERSION=24.0.0.6 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Jun 2024 23:49:59 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 18 Jun 2024 23:50:02 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240620240603-2001 LIBERTY_SHA=e2daf941ebdf3908d50bb1288c1574ccfd454796 LIBERTY_VERSION=24.0.0.6 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env
# Tue, 18 Jun 2024 23:50:02 GMT
COPY file:7278f8f20139aab77b5c9fa76ad85e8a92836053c3ecfb9f5925f1a19788ef47 in /opt/ibm/NOTICES 
# Tue, 18 Jun 2024 23:50:03 GMT
COPY dir:9bc2ef96ad4f191171bf4612e561c64bae28466984c4742002b7dba3b9ffb3ad in /opt/ibm/helpers/ 
# Tue, 18 Jun 2024 23:50:03 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Tue, 18 Jun 2024 23:50:05 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240620240603-2001 LIBERTY_SHA=e2daf941ebdf3908d50bb1288c1574ccfd454796 LIBERTY_VERSION=24.0.0.6 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Tue, 18 Jun 2024 23:50:14 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240620240603-2001 LIBERTY_SHA=e2daf941ebdf3908d50bb1288c1574ccfd454796 LIBERTY_VERSION=24.0.0.6 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Tue, 18 Jun 2024 23:50:15 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Tue, 18 Jun 2024 23:50:15 GMT
USER 1001
# Tue, 18 Jun 2024 23:50:15 GMT
EXPOSE 9080 9443
# Tue, 18 Jun 2024 23:50:16 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 18 Jun 2024 23:50:16 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 18 Jun 2024 23:51:31 GMT
ARG VERBOSE=false
# Tue, 18 Jun 2024 23:51:31 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 18 Jun 2024 23:58:50 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw;
# Tue, 18 Jun 2024 23:58:55 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Tue, 18 Jun 2024 23:59:38 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:391f04f7f495cb5fc20be69876c8638cb8f316a2cddac5d48d77ca39244e6dea`  
		Last Modified: Wed, 05 Jun 2024 03:48:14 GMT  
		Size: 35.6 MB (35588332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174541fe61c2b5942c592eaffb21f1b2fae4f1c23360d1e953d562159e6c99c7`  
		Last Modified: Wed, 05 Jun 2024 04:07:10 GMT  
		Size: 1.6 MB (1574740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9436f591bc2eec6436500eca01f096c61b94466b1c9735a08be7221606c09b6`  
		Last Modified: Wed, 05 Jun 2024 04:07:20 GMT  
		Size: 135.5 MB (135475341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def7261fd7469c0937ff028c57f52816a3dce8a78782023e33cc91ee1214162d`  
		Last Modified: Wed, 19 Jun 2024 00:18:11 GMT  
		Size: 271.0 KB (270963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ca3889c331feb4a79b0308fc011368f76ba0bef01efadb866c3c2ca9df7cb4`  
		Last Modified: Wed, 19 Jun 2024 00:18:12 GMT  
		Size: 17.5 MB (17529520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc031cb415033a8e03cfe5f06cd374a31b245f07d0088123d61583179f8c965`  
		Last Modified: Wed, 19 Jun 2024 00:18:10 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd842d50d2a2173210ff595558c2254772bffbf42d37a0e72045611787c3cf61`  
		Last Modified: Wed, 19 Jun 2024 00:18:08 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66755107bb1e57b3ce8a2a1595f77a90c23486e90e4bbd69dcf289a83d6632d`  
		Last Modified: Wed, 19 Jun 2024 00:18:08 GMT  
		Size: 11.8 KB (11839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789d56023bc087c70c58dfb331ea4f49d26af9cb89fce940cb009ee61191ecaf`  
		Last Modified: Wed, 19 Jun 2024 00:18:08 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934df50e2c460aa71b699b575ef41e3e37c5cddd24dc99bee8b1a5cb79c6a9c5`  
		Last Modified: Wed, 19 Jun 2024 00:18:08 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0da7b0901ce634a3766a15e640c28e9bb2545fbaac354179ed1ced7beb52663`  
		Last Modified: Wed, 19 Jun 2024 00:18:09 GMT  
		Size: 5.3 MB (5255949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc356dac53abe4c0c7ac717c1cc8574cc353103a09c515e1fed4a5c97cccc04b`  
		Last Modified: Wed, 19 Jun 2024 00:18:58 GMT  
		Size: 350.2 MB (350203095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca4d7153a19d0babdb0b84060c5d891a98d6b128f5d663ee9b823efce402893`  
		Last Modified: Wed, 19 Jun 2024 00:18:40 GMT  
		Size: 950.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85c2d3e529641abd65a547a493ebb3bb09c59f7a4db16854d65490bb25c0458`  
		Last Modified: Wed, 19 Jun 2024 00:18:42 GMT  
		Size: 13.2 MB (13229997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:latest` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:ef5b4c914c0a3b4875c97ba8836cd69150abfd47dcfac329bca2a5914130f993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **550.4 MB (550394406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3222cb032a41c9f321bdc7d73c71b697a724d2a5a235bcf6d05c6feeeea4f19`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 09 May 2024 05:12:02 GMT
ARG RELEASE
# Thu, 09 May 2024 05:12:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 09 May 2024 05:12:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 09 May 2024 05:12:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 09 May 2024 05:12:02 GMT
ADD file:4fb908f3bd908a7abc338d7e2006cb2c97aa7f83aca415f3b86c0ae86d61fed1 in / 
# Thu, 09 May 2024 05:12:02 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 05:12:02 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 09 May 2024 05:12:02 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 05:12:02 GMT
ENV JAVA_VERSION=8.0.8.25
# Thu, 09 May 2024 05:12:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='82be3936ccd4acbba83fdea2302770fa9a89266829fa2ff22c06b11e616281c0';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='7892771ebe4ee2988988031bf504b054c41fdc905fefc87c53d7bc499d7b44fa';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='55647d87f192db41e52e8cc5ea517266a0bded42e3c326cf2e8f03a64a473a96';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='dc1ffb2b769a6a08f161b801f7dfd413400d9cfcebed3c6e7229d48dd1a52bad';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 09 May 2024 05:12:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 18 Jun 2024 18:55:44 GMT
USER root
# Tue, 18 Jun 2024 18:55:44 GMT
ARG VERBOSE=false
# Tue, 18 Jun 2024 18:55:44 GMT
ARG OPENJ9_SCC=true
# Tue, 18 Jun 2024 18:55:44 GMT
ARG LIBERTY_VERSION=24.0.0.6
# Tue, 18 Jun 2024 18:55:44 GMT
ARG LIBERTY_BUILD_LABEL=cl240620240603-2001
# Tue, 18 Jun 2024 18:55:44 GMT
ARG LIBERTY_SHA=e2daf941ebdf3908d50bb1288c1574ccfd454796
# Tue, 18 Jun 2024 18:55:44 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.6 org.opencontainers.image.revision=cl240620240603-2001 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Tue, 18 Jun 2024 18:55:44 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Tue, 18 Jun 2024 18:55:44 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.6 BuildLabel=cl240620240603-2001
# Tue, 18 Jun 2024 18:55:44 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.6 LIBERTY_BUILD_LABEL=cl240620240603-2001 LIBERTY_SHA=e2daf941ebdf3908d50bb1288c1574ccfd454796
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 18 Jun 2024 18:55:44 GMT
ARG LIBERTY_URL
# Tue, 18 Jun 2024 18:55:44 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 18 Jun 2024 18:55:44 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.6 LIBERTY_BUILD_LABEL=cl240620240603-2001 LIBERTY_SHA=e2daf941ebdf3908d50bb1288c1574ccfd454796 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 18:55:44 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 18 Jun 2024 18:55:44 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.6 LIBERTY_BUILD_LABEL=cl240620240603-2001 LIBERTY_SHA=e2daf941ebdf3908d50bb1288c1574ccfd454796 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 18 Jun 2024 18:55:44 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 18 Jun 2024 18:55:44 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 18 Jun 2024 18:55:44 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 18 Jun 2024 18:55:44 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.6 LIBERTY_BUILD_LABEL=cl240620240603-2001 LIBERTY_SHA=e2daf941ebdf3908d50bb1288c1574ccfd454796 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Tue, 18 Jun 2024 18:55:44 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.6 LIBERTY_BUILD_LABEL=cl240620240603-2001 LIBERTY_SHA=e2daf941ebdf3908d50bb1288c1574ccfd454796 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 18 Jun 2024 18:55:44 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Tue, 18 Jun 2024 18:55:44 GMT
USER 1001
# Tue, 18 Jun 2024 18:55:44 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 18 Jun 2024 18:55:44 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 18 Jun 2024 18:55:44 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 18 Jun 2024 18:55:44 GMT
ARG VERBOSE=false
# Tue, 18 Jun 2024 18:55:44 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 18 Jun 2024 18:55:44 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Tue, 18 Jun 2024 18:55:44 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Tue, 18 Jun 2024 18:55:44 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:22512bbfe178a8ec7b5e4e48135f8a3e1ad0245ed3ee6a47f89947ce7ffb5d4f`  
		Last Modified: Mon, 03 Jun 2024 10:47:11 GMT  
		Size: 28.0 MB (28000515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51938117bdde1396c0e2d8ef3c52c92b614260596f918f02273bccf82a7f3ff4`  
		Last Modified: Tue, 25 Jun 2024 23:29:58 GMT  
		Size: 1.5 MB (1477329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bdd291cdc1c7ce3a43a7023e6e95c2b9eea5140b0abb7cbdd8e9a372771f58`  
		Last Modified: Tue, 25 Jun 2024 23:30:02 GMT  
		Size: 131.8 MB (131758206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9256ce65019085c86d49e76cc4fcb7313f4994a542b7048a3f092d38cc6c659`  
		Last Modified: Wed, 26 Jun 2024 00:20:36 GMT  
		Size: 114.7 KB (114719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59553cb2d8fd74f769e2c558e93c7caa2e2b0d8cbac9114fc2b143ad0cb0aa5b`  
		Last Modified: Wed, 26 Jun 2024 00:20:36 GMT  
		Size: 17.4 MB (17375467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514a35d9e29fbfe5ec3fb86bd5e91029a466f39ce6f4903999c56415fe51387a`  
		Last Modified: Wed, 26 Jun 2024 00:20:36 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6e5da9ae2cd96359c468e3c84786b1590e583dd2ee9133242084e59a2bb5ef`  
		Last Modified: Wed, 26 Jun 2024 00:20:36 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eaabe14651883dfbd9e4500a27962203bbf3fa95d3291b5c58a79219f7e4b9`  
		Last Modified: Wed, 26 Jun 2024 00:20:37 GMT  
		Size: 11.8 KB (11837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac41f945b975ebe6d07a84af8300a36ec2f57009773f75a16cb80925e02a1b7`  
		Last Modified: Wed, 26 Jun 2024 00:20:37 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d85ec33441a66af242c04989460b052351887aa285d5a28d2a41ee949e49736`  
		Last Modified: Wed, 26 Jun 2024 00:20:37 GMT  
		Size: 12.6 KB (12644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f581c81145d71ec3f34023260c346602005eb44f2fe6a6b2f6bc7159fe5fff`  
		Last Modified: Wed, 26 Jun 2024 00:20:38 GMT  
		Size: 5.8 MB (5810966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec5a85af8fb88f20a45da0ad7f58c51cfdbd46133f1a993098a70b6d07050b1`  
		Last Modified: Wed, 26 Jun 2024 01:06:03 GMT  
		Size: 350.2 MB (350204970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42d4378ae829f6c54fae6b7871174c9d97038cd904a64ed57626b98afe6627e`  
		Last Modified: Wed, 26 Jun 2024 01:05:57 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd40bdddf0e61dda9b10c7ef6eda6aca4ce9fdec81a2919049345c44575bb336`  
		Last Modified: Wed, 26 Jun 2024 01:05:58 GMT  
		Size: 15.6 MB (15624459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:latest` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:e2b0eb9045b17a4e791b879bf6fdf20bd27aed802b5e13db4ea43f482e858269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3840158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc0c83e83b8db0b272926e7b669ffba88a21c217683de3f6d7b204558a1ed1c`

```dockerfile
```

-	Layers:
	-	`sha256:ed472ae5705a24901df9850e6f75be639ae54e643dbaba02366465590db9d69e`  
		Last Modified: Wed, 26 Jun 2024 01:05:56 GMT  
		Size: 3.8 MB (3821120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eff0e39a50619e4e5e50ebefb56ef2abac2501781c827f22ab1df914e4e972f4`  
		Last Modified: Wed, 26 Jun 2024 01:05:56 GMT  
		Size: 19.0 KB (19038 bytes)  
		MIME: application/vnd.in-toto+json
