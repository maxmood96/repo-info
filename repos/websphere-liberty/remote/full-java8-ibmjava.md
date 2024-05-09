## `websphere-liberty:full-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:9b66bd67eb8597d30d9d990edb6bb3b86fd04d9a0aee9b09248a8e4fee87486c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:full-java8-ibmjava` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:6b52e91b2175cb02a937ed6e7719d1ff18382890fd1133b9eb758d74b78ec414
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.0 MB (555963374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:335376707aa8a9ce76d646dcb49dca0cc9140628e8326b23ea03cde830f76b52`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:25:37 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 02 May 2024 02:25:55 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 09 May 2024 16:25:46 GMT
ENV JAVA_VERSION=8.0.8.25
# Thu, 09 May 2024 16:25:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='82be3936ccd4acbba83fdea2302770fa9a89266829fa2ff22c06b11e616281c0';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='7892771ebe4ee2988988031bf504b054c41fdc905fefc87c53d7bc499d7b44fa';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='55647d87f192db41e52e8cc5ea517266a0bded42e3c326cf2e8f03a64a473a96';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='dc1ffb2b769a6a08f161b801f7dfd413400d9cfcebed3c6e7229d48dd1a52bad';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz;
# Thu, 09 May 2024 16:25:58 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Thu, 09 May 2024 16:47:50 GMT
USER root
# Thu, 09 May 2024 16:47:50 GMT
ARG VERBOSE=false
# Thu, 09 May 2024 16:47:50 GMT
ARG OPENJ9_SCC=true
# Thu, 09 May 2024 16:47:50 GMT
ARG LIBERTY_VERSION=24.0.0.4
# Thu, 09 May 2024 16:47:50 GMT
ARG LIBERTY_BUILD_LABEL=cl240420240408-2000
# Thu, 09 May 2024 16:47:50 GMT
ARG LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3
# Thu, 09 May 2024 16:47:50 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.4 org.opencontainers.image.revision=cl240420240408-2000 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 09 May 2024 16:47:51 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Thu, 09 May 2024 16:47:51 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.4 BuildLabel=cl240420240408-2000
# Thu, 09 May 2024 16:47:59 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*;
# Thu, 09 May 2024 16:47:59 GMT
ARG LIBERTY_URL
# Thu, 09 May 2024 16:47:59 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 09 May 2024 16:48:07 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 09 May 2024 16:48:08 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 09 May 2024 16:48:09 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env
# Thu, 09 May 2024 16:48:09 GMT
COPY file:7278f8f20139aab77b5c9fa76ad85e8a92836053c3ecfb9f5925f1a19788ef47 in /opt/ibm/NOTICES 
# Thu, 09 May 2024 16:48:09 GMT
COPY dir:9bc2ef96ad4f191171bf4612e561c64bae28466984c4742002b7dba3b9ffb3ad in /opt/ibm/helpers/ 
# Thu, 09 May 2024 16:48:09 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 09 May 2024 16:48:10 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 09 May 2024 16:48:17 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 09 May 2024 16:48:17 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Thu, 09 May 2024 16:48:17 GMT
USER 1001
# Thu, 09 May 2024 16:48:17 GMT
EXPOSE 9080 9443
# Thu, 09 May 2024 16:48:17 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 09 May 2024 16:48:17 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 09 May 2024 16:48:29 GMT
ARG VERBOSE=false
# Thu, 09 May 2024 16:48:29 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 09 May 2024 16:55:42 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw;
# Thu, 09 May 2024 16:55:43 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Thu, 09 May 2024 16:56:19 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f8db45b3d5d0ac0b6b07122767bc090d41c210ecb9b4b374ecae77c6a71bbd`  
		Last Modified: Thu, 02 May 2024 02:26:48 GMT  
		Size: 1.5 MB (1469725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a78ea0a20549516f864538c4071c42e658ee010dfa95606233855d8e7f5cba`  
		Last Modified: Thu, 09 May 2024 16:26:48 GMT  
		Size: 135.0 MB (135005908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02136bf86be3cfd6ed41816b35d582b83d4a1fca45b8533e5a93b0349d7e3a29`  
		Last Modified: Thu, 09 May 2024 17:14:06 GMT  
		Size: 266.6 KB (266595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8e028f67d14dd4ccf5a96a4dc7b81fc2961972499d5920ee4bae074ad31a80`  
		Last Modified: Thu, 09 May 2024 17:14:07 GMT  
		Size: 17.4 MB (17365940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f61904c20f103d3e0ba6332f24e50aae85e3ca856dec80599fd4524b04e259`  
		Last Modified: Thu, 09 May 2024 17:14:05 GMT  
		Size: 640.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9450432bde384fcd9d186dd17149b791ca330c969deec5a6962474caceb9add2`  
		Last Modified: Thu, 09 May 2024 17:14:03 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850186d88a3c94667958ad39309e3cd4808955a90f62484f10c3db1363bccf64`  
		Last Modified: Thu, 09 May 2024 17:14:03 GMT  
		Size: 11.9 KB (11867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3399ca54bbffcc43099a208c4909bdb88eb42e74195221ddc724053e24681a`  
		Last Modified: Thu, 09 May 2024 17:14:03 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4981f41fada403186f5cbd1ac0ca81cbb60d30c73ac207a2e9e5ab82d8f66c4`  
		Last Modified: Thu, 09 May 2024 17:14:04 GMT  
		Size: 12.8 KB (12788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265ea250edeb8a929450fa7726bf321b76a6b1c89feec706a3142ef2b2f82174`  
		Last Modified: Thu, 09 May 2024 17:14:04 GMT  
		Size: 5.8 MB (5758477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3966cf3a9a0a24bf297d3184bdf1bab1d2606b09f5295a98c8cd9c868b555eb3`  
		Last Modified: Thu, 09 May 2024 17:14:34 GMT  
		Size: 349.9 MB (349855282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca894ef38b6e8604cd268e16e0091107d4db0f894ea8451561b236d433ca2549`  
		Last Modified: Thu, 09 May 2024 17:14:18 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40119225af97503f59a296178f5c4657fac127b5aaa5920dac2d51669197d3e1`  
		Last Modified: Thu, 09 May 2024 17:14:20 GMT  
		Size: 15.8 MB (15773762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:1201517a349d0704992e921ebdbfe10b931591dce51b2de79d41f4ba1ac717dd
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.6 MB (558570082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8814529e6bf157a26fdd977d4b73bb3c16b924c9a3c41b042e18cd43198d7e1`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:13 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:17 GMT
ADD file:3ab2760f4e449111dcca3f0816583c72999e1ce2ec20beac068dccfd6c9d8b81 in / 
# Sat, 27 Apr 2024 13:18:17 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:38:39 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 02 May 2024 01:38:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 09 May 2024 16:17:38 GMT
ENV JAVA_VERSION=8.0.8.25
# Thu, 09 May 2024 16:17:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='82be3936ccd4acbba83fdea2302770fa9a89266829fa2ff22c06b11e616281c0';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='7892771ebe4ee2988988031bf504b054c41fdc905fefc87c53d7bc499d7b44fa';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='55647d87f192db41e52e8cc5ea517266a0bded42e3c326cf2e8f03a64a473a96';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='dc1ffb2b769a6a08f161b801f7dfd413400d9cfcebed3c6e7229d48dd1a52bad';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz;
# Thu, 09 May 2024 16:17:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Thu, 09 May 2024 16:38:01 GMT
USER root
# Thu, 09 May 2024 16:38:01 GMT
ARG VERBOSE=false
# Thu, 09 May 2024 16:38:02 GMT
ARG OPENJ9_SCC=true
# Thu, 09 May 2024 16:38:02 GMT
ARG LIBERTY_VERSION=24.0.0.4
# Thu, 09 May 2024 16:38:02 GMT
ARG LIBERTY_BUILD_LABEL=cl240420240408-2000
# Thu, 09 May 2024 16:38:03 GMT
ARG LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3
# Thu, 09 May 2024 16:38:03 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.4 org.opencontainers.image.revision=cl240420240408-2000 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 09 May 2024 16:38:03 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Thu, 09 May 2024 16:38:04 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.4 BuildLabel=cl240420240408-2000
# Thu, 09 May 2024 16:38:16 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*;
# Thu, 09 May 2024 16:38:17 GMT
ARG LIBERTY_URL
# Thu, 09 May 2024 16:38:17 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 09 May 2024 16:38:28 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 09 May 2024 16:38:29 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 09 May 2024 16:38:30 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env
# Thu, 09 May 2024 16:38:31 GMT
COPY file:7278f8f20139aab77b5c9fa76ad85e8a92836053c3ecfb9f5925f1a19788ef47 in /opt/ibm/NOTICES 
# Thu, 09 May 2024 16:38:31 GMT
COPY dir:9bc2ef96ad4f191171bf4612e561c64bae28466984c4742002b7dba3b9ffb3ad in /opt/ibm/helpers/ 
# Thu, 09 May 2024 16:38:31 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 09 May 2024 16:38:33 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 09 May 2024 16:38:42 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 09 May 2024 16:38:42 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Thu, 09 May 2024 16:38:43 GMT
USER 1001
# Thu, 09 May 2024 16:38:43 GMT
EXPOSE 9080 9443
# Thu, 09 May 2024 16:38:44 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 09 May 2024 16:38:44 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 09 May 2024 16:38:55 GMT
ARG VERBOSE=false
# Thu, 09 May 2024 16:38:55 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 09 May 2024 16:46:26 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw;
# Thu, 09 May 2024 16:46:33 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Thu, 09 May 2024 16:47:17 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:ef1313ed517c6def5644ab70e25cc66f1c4cd52b1e81c07fb33bfb8850b39c25`  
		Last Modified: Thu, 02 May 2024 01:40:15 GMT  
		Size: 35.6 MB (35588524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d160f4318a88a056643db72fa03a8b4f47253fd4510ad83ce855372df5d000c4`  
		Last Modified: Thu, 02 May 2024 01:40:10 GMT  
		Size: 1.6 MB (1574876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d55a2b6671c4d9d73cd45efdd613e63a36b662a6db877d81758e62aafb86186`  
		Last Modified: Thu, 09 May 2024 16:18:59 GMT  
		Size: 135.5 MB (135475395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079f280b3e8356fdcc8c0a559f7bdd3a77497e4085525b444d923895e3e276f4`  
		Last Modified: Thu, 09 May 2024 17:07:41 GMT  
		Size: 271.1 KB (271070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eced47787f002786f08432d50ff73a9181016f266cbc5c7dc45e43061eac970`  
		Last Modified: Thu, 09 May 2024 17:07:42 GMT  
		Size: 17.4 MB (17366665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6f9ef6074a48170ebf563d05770a823ebcf4e5d362b07558aa71116f8a3d34`  
		Last Modified: Thu, 09 May 2024 17:07:40 GMT  
		Size: 645.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64af91e8aef0fa4f4a614eff709ef52a1b0b0b2727d50ee3d4f030d8776c5e25`  
		Last Modified: Thu, 09 May 2024 17:07:38 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00938aa0ed1f15aa326ef09e31b0da47cd366d892234ebb212f8d43e279d97a2`  
		Last Modified: Thu, 09 May 2024 17:07:38 GMT  
		Size: 11.9 KB (11864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88b7f1b4d91b5a0888f0d76720e6cb2e8a4d2ac07ce6e930f82158548604329`  
		Last Modified: Thu, 09 May 2024 17:07:38 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0acd698a555acc551b145be8cfc4a8b9eb14f0a931f229537fd08fa56017c74`  
		Last Modified: Thu, 09 May 2024 17:07:38 GMT  
		Size: 12.8 KB (12791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ba5af909224d0e31f7b03efa73acf77129c1716977b59756d44a2d11dfc221`  
		Last Modified: Thu, 09 May 2024 17:07:39 GMT  
		Size: 5.2 MB (5240211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff15d8a640af209688b8d04f4b2bcf2b13b114bac5eced4b169bef8fe35637c`  
		Last Modified: Thu, 09 May 2024 17:08:11 GMT  
		Size: 349.9 MB (349855605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb034137283c08d7fe72421384ea3cd797b8a9fd28696c9599c62a25530f889`  
		Last Modified: Thu, 09 May 2024 17:07:52 GMT  
		Size: 944.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fbe64c5cacb748781e5cb78dba138be4f50f7d60bb2d5b890d2a86332208881`  
		Last Modified: Thu, 09 May 2024 17:07:54 GMT  
		Size: 13.2 MB (13169699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:72e5ae1fa2451923c81c062e21bcb6c50a708be188952c7f31f6894dd54412c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **550.9 MB (550850716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ea0a840130e5d9882dca0c7a12a509acc78aa90a4944b07bd727a4a86fa5dc`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 27 Apr 2024 13:52:56 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:52:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:52:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:52:56 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:52:58 GMT
ADD file:7d693ab3b1f45d4992a119ec94444efc96c176ad954375f3bc1299ab813a46a0 in / 
# Sat, 27 Apr 2024 13:52:58 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:12:28 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 02 May 2024 01:12:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 09 May 2024 16:43:02 GMT
ENV JAVA_VERSION=8.0.8.25
# Thu, 09 May 2024 16:43:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='82be3936ccd4acbba83fdea2302770fa9a89266829fa2ff22c06b11e616281c0';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='7892771ebe4ee2988988031bf504b054c41fdc905fefc87c53d7bc499d7b44fa';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='55647d87f192db41e52e8cc5ea517266a0bded42e3c326cf2e8f03a64a473a96';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='dc1ffb2b769a6a08f161b801f7dfd413400d9cfcebed3c6e7229d48dd1a52bad';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz;
# Thu, 09 May 2024 16:43:25 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Thu, 09 May 2024 17:07:31 GMT
USER root
# Thu, 09 May 2024 17:07:31 GMT
ARG VERBOSE=false
# Thu, 09 May 2024 17:07:32 GMT
ARG OPENJ9_SCC=true
# Thu, 09 May 2024 17:07:32 GMT
ARG LIBERTY_VERSION=24.0.0.4
# Thu, 09 May 2024 17:07:33 GMT
ARG LIBERTY_BUILD_LABEL=cl240420240408-2000
# Thu, 09 May 2024 17:07:33 GMT
ARG LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3
# Thu, 09 May 2024 17:07:33 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.4 org.opencontainers.image.revision=cl240420240408-2000 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 09 May 2024 17:07:34 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Thu, 09 May 2024 17:07:34 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.4 BuildLabel=cl240420240408-2000
# Thu, 09 May 2024 17:07:44 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*;
# Thu, 09 May 2024 17:07:45 GMT
ARG LIBERTY_URL
# Thu, 09 May 2024 17:07:46 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 09 May 2024 17:07:57 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 09 May 2024 17:07:59 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 09 May 2024 17:08:01 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env
# Thu, 09 May 2024 17:08:02 GMT
COPY file:7278f8f20139aab77b5c9fa76ad85e8a92836053c3ecfb9f5925f1a19788ef47 in /opt/ibm/NOTICES 
# Thu, 09 May 2024 17:08:02 GMT
COPY dir:9bc2ef96ad4f191171bf4612e561c64bae28466984c4742002b7dba3b9ffb3ad in /opt/ibm/helpers/ 
# Thu, 09 May 2024 17:08:03 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 09 May 2024 17:08:04 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 09 May 2024 17:08:16 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240420240408-2000 LIBERTY_SHA=9a153c5e45bb0c6ceed3f4ebe18d4e425d0444a3 LIBERTY_VERSION=24.0.0.4 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 09 May 2024 17:08:17 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Thu, 09 May 2024 17:08:18 GMT
USER 1001
# Thu, 09 May 2024 17:08:18 GMT
EXPOSE 9080 9443
# Thu, 09 May 2024 17:08:19 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 09 May 2024 17:08:19 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 09 May 2024 17:08:46 GMT
ARG VERBOSE=false
# Thu, 09 May 2024 17:08:46 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 09 May 2024 17:16:10 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw;
# Thu, 09 May 2024 17:16:39 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Thu, 09 May 2024 17:17:15 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:ffda8878ec88daab976ebae63a8dc770c7ff669cb06828bf12b1a5acca67f1f8`  
		Last Modified: Thu, 02 May 2024 01:13:50 GMT  
		Size: 28.6 MB (28637522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ddcae10b4f44029844c59ada01f332a62187c487a21182c2b4143cc0c7db95`  
		Last Modified: Thu, 02 May 2024 01:13:46 GMT  
		Size: 1.5 MB (1477663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccab1d62ffd8c0a77b0abe9fde0646625fd1c4ebbf972d882db3f1df6ef6532f`  
		Last Modified: Thu, 09 May 2024 16:44:53 GMT  
		Size: 131.8 MB (131758105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a588dbe240348a73066264fc852467ea2215bfbf7611438796c3da2d65729430`  
		Last Modified: Thu, 09 May 2024 17:36:10 GMT  
		Size: 268.0 KB (268006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d332c8f458c9fbb62e7eb5ea37aae2b75dfca065d791d5205ee07376062bee`  
		Last Modified: Thu, 09 May 2024 17:36:11 GMT  
		Size: 17.4 MB (17366255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7293c5dc14567e754acc01031af77e1fe7d29fea45f75cd1774caeab58d9aa1b`  
		Last Modified: Thu, 09 May 2024 17:36:10 GMT  
		Size: 645.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b9f2e1e9780a194e6b893a02b48be2af078a17dfe47361c4ae0e1385b943ea`  
		Last Modified: Thu, 09 May 2024 17:36:08 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8694ea7b0cfd84bb69ad8a63f9375c4785d603aa88829c9492c43464509fea26`  
		Last Modified: Thu, 09 May 2024 17:36:08 GMT  
		Size: 11.9 KB (11864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6895426cd6440c037122931df9785c2a8326af4d8c03d0b6a90108aefd3a0b55`  
		Last Modified: Thu, 09 May 2024 17:36:08 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aa6ed85299b73edd8b9346a64490f26ca2d020e4864d872f277015e5d664ac`  
		Last Modified: Thu, 09 May 2024 17:36:08 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7abbfe4978457bd8f5f4092a61700bc74521aeafecc24cb67f7da871115a1522`  
		Last Modified: Thu, 09 May 2024 17:36:09 GMT  
		Size: 5.9 MB (5920766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c5e7b522fc43f695941d48e2170bba2d9684ba9919212a384de36e487a277f`  
		Last Modified: Thu, 09 May 2024 17:36:33 GMT  
		Size: 349.9 MB (349855420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987171a46fca9e2c8ed2ed2351bd8c4ab667b0d329038fe239d67d5e1d3704d5`  
		Last Modified: Thu, 09 May 2024 17:36:18 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656cd7b056ab4a5b8166db438ced6c97b6acb13ddfae3e0dd8349629dcc26fda`  
		Last Modified: Thu, 09 May 2024 17:36:21 GMT  
		Size: 15.5 MB (15538912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
