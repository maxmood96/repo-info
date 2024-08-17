## `websphere-liberty:full`

```console
$ docker pull websphere-liberty@sha256:b4a81f0e05ddbe286138c16b0b7cade228495e63a36c763a1a990e7f45d0e415
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
$ docker pull websphere-liberty@sha256:9d6a8fd37d04bb1de50de7fbbebcee482660ac507592d9a915d45da55c7cbd2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.6 MB (558597586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6509b69b6644ab583f258905a77a3f4db03dabf1d699a35a97f5c8a23185131`
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
	-	`sha256:9d33f40b95e22169d8c9eeb62b41551a3e81c0d6e6a1387f455984d0aec4d75a`  
		Last Modified: Sat, 17 Aug 2024 04:08:34 GMT  
		Size: 113.4 KB (113364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf24a9fe5ccecdf8b0aa526f40ea565430377cff4fde92353d40714ac272eae`  
		Last Modified: Sat, 17 Aug 2024 04:08:35 GMT  
		Size: 17.4 MB (17422148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbac3f88a77a706e82bb1596c1c814e9f61122f6027d1a8b7218c7229191d6f7`  
		Last Modified: Sat, 17 Aug 2024 04:08:34 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6153c2cbc6ac18da5b5c4319974fe5cf835278f06cdf57b8a8abb79bd6f76f`  
		Last Modified: Sat, 17 Aug 2024 04:08:34 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43c8cc59da4e65a46168291ae09bb481d9d73f1cc95195ad3f5dfee684d7c05`  
		Last Modified: Sat, 17 Aug 2024 04:08:35 GMT  
		Size: 11.8 KB (11834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a73e5997181b77a6dc805a8ef330910a1eee3e0ea6c2258eb0c7e20e538b75`  
		Last Modified: Sat, 17 Aug 2024 04:08:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88178161de755f6edf3e8a465236f970f9f786d41cdb6593f483c0af921438e9`  
		Last Modified: Sat, 17 Aug 2024 04:08:35 GMT  
		Size: 12.6 KB (12647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e640b78ef807b7a2638bd58e9ebad738f5e80da583a70f9c6090ef29806b6c0`  
		Last Modified: Sat, 17 Aug 2024 04:08:36 GMT  
		Size: 5.8 MB (5759181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d6d988941f2ca47bda5525d01bce3cc1fac0d3231fd6497b7a3b5857c176fc`  
		Last Modified: Sat, 17 Aug 2024 05:09:06 GMT  
		Size: 353.4 MB (353433405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207ddb8f160ae34d856f44a7955acd21cce21d42b83d8f6de42caf5945595371`  
		Last Modified: Sat, 17 Aug 2024 05:08:58 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27a9c7ec5a8df5890977fe659bf015fa1e07c62b58e4f5b47d4c16efdc447ad`  
		Last Modified: Sat, 17 Aug 2024 05:08:59 GMT  
		Size: 15.9 MB (15853207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:907a094ff373489a9a86854c3013557cfbf4b93050c7dc6f8e9a891294e779f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da137a61947e2b4ac382d5d6f542cccea8326c035d364143e2b3f5cc0ad0a8b7`

```dockerfile
```

-	Layers:
	-	`sha256:eb19cb3e1ce70270fafa8aec56448c6be2862b375cfdb04f918a426878c0402d`  
		Last Modified: Sat, 17 Aug 2024 05:08:59 GMT  
		Size: 4.1 MB (4073616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ed16db99e1fb79009723fdf7d133f1cc60ea1d3c2b3c90f23d639f3503a471b`  
		Last Modified: Sat, 17 Aug 2024 05:08:58 GMT  
		Size: 19.0 KB (19038 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:cffde8d8861ec044fddfff3f133bf1bb3e3fe0decb641c8ec8813c384c124e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.0 MB (560974460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14219da266d43a1730e4f0bfa466b00d8716eeaa78f7f6e9d6c5fee64c61e1f`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
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
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b823c911ee157eda0ab24a76ac49580a066062d8c3dbbe00bf159415ecbf49b6`  
		Last Modified: Thu, 15 Aug 2024 18:18:41 GMT  
		Size: 1.5 MB (1523275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb773c68b75c4a8719fbee948996532dc99714792b4c99f1fe5794da98e12a5`  
		Last Modified: Thu, 15 Aug 2024 18:18:45 GMT  
		Size: 135.5 MB (135470553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58206147f3edbada0e8bdb38dc76c933d552cfb60f4b02122cad620325facb6f`  
		Last Modified: Thu, 15 Aug 2024 20:04:31 GMT  
		Size: 117.9 KB (117907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4a4df4c02e90692b6c74c44db3365b15d3a74aab151947d7e01fd94855dcbf`  
		Last Modified: Thu, 15 Aug 2024 20:04:32 GMT  
		Size: 17.4 MB (17422660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ebbcbb0d80b25ab21cccda3b002474fdad86fff3df081a50ef5a23509a432a`  
		Last Modified: Thu, 15 Aug 2024 20:04:31 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10776c873f9a06625f976ca67fae29e522c55d20407e50f9abe5982f33db0d93`  
		Last Modified: Thu, 15 Aug 2024 20:04:31 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ca4e620ea296c5e9db050d79ee435eaa65fa373999b5357e09b4aa06fd127a`  
		Last Modified: Thu, 15 Aug 2024 20:04:32 GMT  
		Size: 11.8 KB (11834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3804fa22bc70839c30270a288faab72de16c0067ef5dce9b19b71437803c95f3`  
		Last Modified: Thu, 15 Aug 2024 20:04:32 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa39523a5f104ee127b011bde5586436a7d8d0b2d4fcb89f6cbd71e63cbfd12`  
		Last Modified: Thu, 15 Aug 2024 20:04:32 GMT  
		Size: 12.6 KB (12638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0848e73348ad35337508deb7d0a1b8cca6268ff609bf928423f91ae4589781`  
		Last Modified: Thu, 15 Aug 2024 20:04:33 GMT  
		Size: 5.3 MB (5339657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c916169c816ca2eb41d06c9363328dcb7d6d0e6013254f31fa402650f19b259`  
		Last Modified: Thu, 15 Aug 2024 21:03:57 GMT  
		Size: 353.4 MB (353433761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f46351fccc3a237bb3a5b28a5cbd6d08a632ef1dd80111c4a13e4be12bf146`  
		Last Modified: Thu, 15 Aug 2024 21:03:45 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de30d4e97c3b998359ec9702bf2f78c962e9a71bb27b74a4f59b93b9384f2f25`  
		Last Modified: Thu, 15 Aug 2024 21:03:45 GMT  
		Size: 13.2 MB (13177794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:4bb2175f328ed6607941dae8e50efb0973e0c524f88b5c374e83c6c496b4e4cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4096718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22cbcdbe7f3a53f89b91f4a88b5310cb0d8b3932ba6ed923c89f71544305f95b`

```dockerfile
```

-	Layers:
	-	`sha256:e2788087c6e14a90c12a7e447e84a77d0beb16e06507fea59f2d0102dfed6d6e`  
		Last Modified: Thu, 15 Aug 2024 21:03:44 GMT  
		Size: 4.1 MB (4077640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:babdefef4a55445ed6f0e5a3f216ae60a9f7c944f6c971831b734d08ab4c72fc`  
		Last Modified: Thu, 15 Aug 2024 21:03:44 GMT  
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
