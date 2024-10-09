## `websphere-liberty:latest`

```console
$ docker pull websphere-liberty@sha256:83543507ca31a60675df5a1c1bedc1ba43ce2ce1eea03c6921c4ffa9939e4e50
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
$ docker pull websphere-liberty@sha256:36e31e184cf6e82a2d7e1bc42db75b407cbb0e562ef426c7b02c0d975eb11b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.4 MB (562360158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf44db3bb6037cb0d8744dbb2db487645eb3608394c50ebeaa1cff94474bb47`
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
# Tue, 08 Oct 2024 20:01:46 GMT
USER root
# Tue, 08 Oct 2024 20:01:46 GMT
ARG VERBOSE=false
# Tue, 08 Oct 2024 20:01:46 GMT
ARG OPENJ9_SCC=true
# Tue, 08 Oct 2024 20:01:46 GMT
ARG LIBERTY_VERSION=24.0.0.10
# Tue, 08 Oct 2024 20:01:46 GMT
ARG LIBERTY_BUILD_LABEL=cl241020240923-1638
# Tue, 08 Oct 2024 20:01:46 GMT
ARG LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf
# Tue, 08 Oct 2024 20:01:46 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.10 org.opencontainers.image.revision=cl241020240923-1638 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Tue, 08 Oct 2024 20:01:46 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Tue, 08 Oct 2024 20:01:46 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.10 BuildLabel=cl241020240923-1638
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
ARG LIBERTY_URL
# Tue, 08 Oct 2024 20:01:46 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Tue, 08 Oct 2024 20:01:46 GMT
USER 1001
# Tue, 08 Oct 2024 20:01:46 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 08 Oct 2024 20:01:46 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 08 Oct 2024 20:01:46 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 08 Oct 2024 20:01:46 GMT
ARG VERBOSE=false
# Tue, 08 Oct 2024 20:01:46 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
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
	-	`sha256:3bc8d26397b783b3431e236ed1a33362fcb10dd69a1e1f6cff35eb760275a419`  
		Last Modified: Wed, 09 Oct 2024 00:04:21 GMT  
		Size: 113.4 KB (113354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0c27aac81efd1ae185a6d21252a26b5f2c2ab931cc78217519cc0de6b13731`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 17.4 MB (17420399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa3b6349fe5a8671a4a3b0d085dc7caf1f1f9d22d7f9c5de0cbb0ce756cacee`  
		Last Modified: Wed, 09 Oct 2024 00:04:21 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63b908e89216f45719752de82c298677d89284c28a08ca676198c79dbf21eca`  
		Last Modified: Wed, 09 Oct 2024 00:04:21 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1a2f9dd4ebde7ec942901cc4c8c080044a55315b66211c2b28117b69e31088`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 11.8 KB (11838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69644d083b62f10661cde021814f4907571293bb2423520517cdd4464b80d98`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b964983b5062d10df19e3f05f631a6b7ef61569444f5497600fe77474393e527`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 12.6 KB (12640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edb32f50f90a7fa1138740c487ad3896cce08473ef7bda267b2d301a9e7471f`  
		Last Modified: Wed, 09 Oct 2024 00:04:23 GMT  
		Size: 5.7 MB (5731989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2cab1a194d5fd42c2ce78537cec80df8ae7933f6cefd0d51191707d486dc13`  
		Last Modified: Wed, 09 Oct 2024 01:06:56 GMT  
		Size: 357.4 MB (357435711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99bcd1ec18ac91a6f1f353672c1a3d05498d17235529e9586b296a238f6263e5`  
		Last Modified: Wed, 09 Oct 2024 01:06:52 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1e4ff14467a64a7925f5a7efe35f35c17775fd5ce31fb90ad01ee6be4798ef`  
		Last Modified: Wed, 09 Oct 2024 01:06:52 GMT  
		Size: 15.6 MB (15642792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:latest` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:8f60610a9fb5d43feefc5d4e04043074b8780d807684d69b88ecaa00b2a39b6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4114450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b471f883e87b2f21639d1a0b030cab83950ddd133dda6fc0aa3d971d0ca1e8d3`

```dockerfile
```

-	Layers:
	-	`sha256:d4b51e23f10f23295187ebfbaf1f3767e5fcc8ee03e00fcffc4109602b0ec8f5`  
		Last Modified: Wed, 09 Oct 2024 01:06:51 GMT  
		Size: 4.1 MB (4095407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:913a4a605b89fec19a67e79f42f26499e0b65f868ef4393bc07c779ee158d4f5`  
		Last Modified: Wed, 09 Oct 2024 01:06:51 GMT  
		Size: 19.0 KB (19043 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:latest` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:594f9f224413d138e68526848e4feafe82e2e13f8e67c513d3084d5894580654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.0 MB (565000715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:057ab15a3e3f2224666681828859fb494f27b570d0d45347e6fd174f23090677`
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
# Tue, 08 Oct 2024 20:01:46 GMT
USER root
# Tue, 08 Oct 2024 20:01:46 GMT
ARG VERBOSE=false
# Tue, 08 Oct 2024 20:01:46 GMT
ARG OPENJ9_SCC=true
# Tue, 08 Oct 2024 20:01:46 GMT
ARG LIBERTY_VERSION=24.0.0.10
# Tue, 08 Oct 2024 20:01:46 GMT
ARG LIBERTY_BUILD_LABEL=cl241020240923-1638
# Tue, 08 Oct 2024 20:01:46 GMT
ARG LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf
# Tue, 08 Oct 2024 20:01:46 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.10 org.opencontainers.image.revision=cl241020240923-1638 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Tue, 08 Oct 2024 20:01:46 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Tue, 08 Oct 2024 20:01:46 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.10 BuildLabel=cl241020240923-1638
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
ARG LIBERTY_URL
# Tue, 08 Oct 2024 20:01:46 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Tue, 08 Oct 2024 20:01:46 GMT
USER 1001
# Tue, 08 Oct 2024 20:01:46 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 08 Oct 2024 20:01:46 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 08 Oct 2024 20:01:46 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 08 Oct 2024 20:01:46 GMT
ARG VERBOSE=false
# Tue, 08 Oct 2024 20:01:46 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
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
	-	`sha256:695f7b78c6605fcb28d89f13063d56a31b6ba487e86561a8513bf020169026e1`  
		Last Modified: Wed, 09 Oct 2024 00:38:21 GMT  
		Size: 117.9 KB (117867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056e51229c69b2d34a4c4e07b2b4168ab01fbfdd7c1849d442454e386736c5d2`  
		Last Modified: Wed, 09 Oct 2024 00:38:22 GMT  
		Size: 17.4 MB (17420795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a559d20c6da7ef4b280a4a30c6230357f172c69059b64d1c4692f9957bff0bb`  
		Last Modified: Wed, 09 Oct 2024 00:38:21 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce755e3683b31149f207dcb74125fdb4a3524e32948aa22ec6ccd3328255865`  
		Last Modified: Wed, 09 Oct 2024 00:38:21 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e59e504296bff579f33459a687a2e9521eaa6d3e10564b274b32803977377f`  
		Last Modified: Wed, 09 Oct 2024 00:38:22 GMT  
		Size: 11.8 KB (11839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2f67057da1a04a8ebf9a52c7df891133b365bf9384a80415f8ce9c9d101be6`  
		Last Modified: Wed, 09 Oct 2024 00:38:22 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7be01c2c11ee80aaf677f376b45cb6540fa05c5855384714ee6af916310b63`  
		Last Modified: Wed, 09 Oct 2024 00:38:22 GMT  
		Size: 12.6 KB (12647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3e8bcf625ac5676c7f01ac977c03bdcc1102f2393a4e0813689ae9fc4cadc8`  
		Last Modified: Wed, 09 Oct 2024 00:38:23 GMT  
		Size: 5.3 MB (5313705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24fee530ac143dcf97664fb2c9850a8e89c18e1920e9783df35532fe2e83ef19`  
		Last Modified: Wed, 09 Oct 2024 01:28:39 GMT  
		Size: 357.4 MB (357435345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0b6db2e6ca0013df20393ac0d4e1859f4583ed190f7fee496a4b94c0bf7e1b`  
		Last Modified: Wed, 09 Oct 2024 01:28:29 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451483378d5e863a59efd3745ada25c773900b34c4c766a402e5bd330a23e9c6`  
		Last Modified: Wed, 09 Oct 2024 01:28:30 GMT  
		Size: 13.2 MB (13243079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:latest` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:265958b3232f9cb4c514990567e29751c8ccd970380cd0129214fed3d9692a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4116622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e8f1f9c9557bd36ca16a9a0d5bdc5b6df5c8135bda3c99879ae0e5f3c727fb`

```dockerfile
```

-	Layers:
	-	`sha256:209ddd9340743f4778313355b09b1b77af00fb10cd9a3adf8793b3bfd3c27c5d`  
		Last Modified: Wed, 09 Oct 2024 01:28:29 GMT  
		Size: 4.1 MB (4097539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92d4f60b42e6a258083ff26c304e9effa6af9a6eee02475927e8dbc4a7703cdf`  
		Last Modified: Wed, 09 Oct 2024 01:28:28 GMT  
		Size: 19.1 KB (19083 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:latest` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:64769de74e65e9120c636de097b45a1faf673d9946010e7e01da2ac16db36b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.0 MB (558036660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54062f093c636408ec07064295e747223d185e56259d4a05ef0af6cc6f1d65c3`
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
# Tue, 08 Oct 2024 20:01:46 GMT
USER root
# Tue, 08 Oct 2024 20:01:46 GMT
ARG VERBOSE=false
# Tue, 08 Oct 2024 20:01:46 GMT
ARG OPENJ9_SCC=true
# Tue, 08 Oct 2024 20:01:46 GMT
ARG LIBERTY_VERSION=24.0.0.10
# Tue, 08 Oct 2024 20:01:46 GMT
ARG LIBERTY_BUILD_LABEL=cl241020240923-1638
# Tue, 08 Oct 2024 20:01:46 GMT
ARG LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf
# Tue, 08 Oct 2024 20:01:46 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.10 org.opencontainers.image.revision=cl241020240923-1638 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Tue, 08 Oct 2024 20:01:46 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Tue, 08 Oct 2024 20:01:46 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.10 BuildLabel=cl241020240923-1638
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
ARG LIBERTY_URL
# Tue, 08 Oct 2024 20:01:46 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.10 LIBERTY_BUILD_LABEL=cl241020240923-1638 LIBERTY_SHA=464d34c631faa13b85a78de7058ecaa5dbdbbaaf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Tue, 08 Oct 2024 20:01:46 GMT
USER 1001
# Tue, 08 Oct 2024 20:01:46 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 08 Oct 2024 20:01:46 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 08 Oct 2024 20:01:46 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 08 Oct 2024 20:01:46 GMT
ARG VERBOSE=false
# Tue, 08 Oct 2024 20:01:46 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Tue, 08 Oct 2024 20:01:46 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
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
	-	`sha256:ac215ae4e67778c3878158efa24c83e9d6006bcca6da073a60a774515ef4eb0e`  
		Last Modified: Wed, 09 Oct 2024 00:31:03 GMT  
		Size: 114.7 KB (114736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e2fc8e42d51e1a18ccc4ad8d680b4f3946706cfb9737b9b0886300bf8246fc`  
		Last Modified: Wed, 09 Oct 2024 00:31:04 GMT  
		Size: 17.4 MB (17420551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371b3c5ce923867d3e4b08a22cd3c39ebfd89fdd8cb137499085a2ebc5aa2309`  
		Last Modified: Wed, 09 Oct 2024 00:31:04 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b30183d1eec70ca37c122ecaf206f7525f63d7deed6c1ad6c49bef2e61ec165`  
		Last Modified: Wed, 09 Oct 2024 00:31:04 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4487a832dd56fbabd257c327e7f824ecce902b4c3ee19aeeb498feafdda8c4b3`  
		Last Modified: Wed, 09 Oct 2024 00:31:04 GMT  
		Size: 11.8 KB (11839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e35ff034642e3e5f0a8bd0621c9e3878ac749b8ec851e98cc93c70c300de84`  
		Last Modified: Wed, 09 Oct 2024 00:31:04 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a006b6faabc618244bf5da07b6713a4cd756c7fc20cd228fab2e6e0c6c63c823`  
		Last Modified: Wed, 09 Oct 2024 00:31:05 GMT  
		Size: 12.6 KB (12645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314838066852c9b61f48352745f8b1f6d86a8e0da2ed389c7424629d2b883706`  
		Last Modified: Wed, 09 Oct 2024 00:31:05 GMT  
		Size: 5.9 MB (5898546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f58366bc6a25a1abec02d5c340abecb9fc492fa60fab5bf718d023b265fe24`  
		Last Modified: Wed, 09 Oct 2024 01:12:26 GMT  
		Size: 357.4 MB (357436406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed092e09a2c5618c4b1b8812bb73efc97cc05d1c80d5eb0758b57a1735b3eb3c`  
		Last Modified: Wed, 09 Oct 2024 01:12:21 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728fd12fbabf031373fb8f66a57de9e716eec5376666e217b799071fcc980fea`  
		Last Modified: Wed, 09 Oct 2024 01:12:21 GMT  
		Size: 15.8 MB (15758389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:latest` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:088ce006dd1e4a5128c828aac36440e9ffe6b51766f8a418e8f8d56ec2bb1548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba1d185acf468f7786872915c7cdb30e17795a75126c6d5cf7b328cab31e938e`

```dockerfile
```

-	Layers:
	-	`sha256:bdcfc147f9738ff521c431335eb675f015f62acb0c0bee4b2863fffe4714c8e7`  
		Last Modified: Wed, 09 Oct 2024 01:12:20 GMT  
		Size: 4.1 MB (4093348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d91ccd2ca8d53d0f738b01a6a6eca31644f1e96c1ffa77f7444b7d0e982ed131`  
		Last Modified: Wed, 09 Oct 2024 01:12:20 GMT  
		Size: 19.0 KB (19043 bytes)  
		MIME: application/vnd.in-toto+json
