## `websphere-liberty:kernel`

```console
$ docker pull websphere-liberty@sha256:a7e5f901415f160a00aaa4db832d468c9bddbbf1a310459d158073b2444e77e5
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
$ docker pull websphere-liberty@sha256:c6b0a14d5742b3a5add33895ff5d97dfb2b57e89e1a7da514d660507c96d9ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 MB (189280706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356549e80fe639db73264e5334f312269dc2a00964ff2e9673b058e82a21e813`
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

### `websphere-liberty:kernel` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:0d3cc49dca8ca4a480a82332f3a965b05ee1908dd6566e54ee9b1e4451773d1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2183522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e94faeefee9897b3a9a5cedc8c9787be155d8dc1ec49f9ecbf61ed81eabe10c`

```dockerfile
```

-	Layers:
	-	`sha256:053704c5f7912edc9eea342b4480af6f1a72ecfc018ecb60280449ffdc39a17e`  
		Last Modified: Wed, 09 Oct 2024 00:04:21 GMT  
		Size: 2.1 MB (2145395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e642da2179fdf72c244f309732a7fdbcc2b1abf8ddbaacab60a9409482d8e549`  
		Last Modified: Wed, 09 Oct 2024 00:04:21 GMT  
		Size: 38.1 KB (38127 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:c63ad4f7e2f9cc99265485611660642be1adb71cb30e5051f5db2af581676e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 MB (194321335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f3c29524fe92c04842f5eaf3de3df0e2977785bc0178abe2eff86ceb6cc7b31`
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

### `websphere-liberty:kernel` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:2dc392acf58e12eeda31fed1b16992388c09ca5bc085616efd8e6b03211f5c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2185702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0c70f517774a754a8033f7989707084bbbc8c06796b1574548566744cecaf9`

```dockerfile
```

-	Layers:
	-	`sha256:075c07163789aa4b970838788cdf406913fa8f55872e76f6005177b7639f0280`  
		Last Modified: Wed, 09 Oct 2024 00:38:21 GMT  
		Size: 2.1 MB (2147527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9ab486df88548c05ab65e0d937b55dc61ff0411eb51705ee619271e85493911`  
		Last Modified: Wed, 09 Oct 2024 00:38:20 GMT  
		Size: 38.2 KB (38175 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:f70ddc4c5e439bd5d4a4b9d9e53218f2c56cab95899abfd66bd8995a3c951009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184840915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ccb7d65118fc8ddfba400eaeb0addf468403f42afddc63f1748d51214fb67bd`
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

### `websphere-liberty:kernel` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:349b6e6d8745da0c8b82859bd00e51497c5bf538fd589c2a2d9b07d9a81b53a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2181465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d602604d948a3bd755b1fc79cda99ae7dcdf6080da4e9218d058d49809743509`

```dockerfile
```

-	Layers:
	-	`sha256:5f7663bbee0f99f27195f639d3b785f7b7ecce7a0db910f82d163ff3590c4f04`  
		Last Modified: Wed, 09 Oct 2024 00:31:04 GMT  
		Size: 2.1 MB (2143336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59c41d338479c6849a6713e1a05361ae81e18dc68bbc12b8d02a4d85fd2813a6`  
		Last Modified: Wed, 09 Oct 2024 00:31:03 GMT  
		Size: 38.1 KB (38129 bytes)  
		MIME: application/vnd.in-toto+json
