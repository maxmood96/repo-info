## `websphere-liberty:kernel-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:a2b41c9778fda17a628940ba337bb0120fa80060f069e11d3730c67001548747
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
$ docker pull websphere-liberty@sha256:239842b35d30c9452df7a687e4dfe409f7f04f640f5027c5b249cca127952c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 MB (189314876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fcb7831fafd632c6a05e82dc0e3a03847617a87cdd92ccfe190f40f610f9d4`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 18 Jun 2024 18:55:44 GMT
ARG RELEASE
# Tue, 18 Jun 2024 18:55:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 18:55:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 18:55:44 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 18 Jun 2024 18:55:44 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Tue, 18 Jun 2024 18:55:44 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 18:55:44 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 18 Jun 2024 18:55:44 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 18:55:44 GMT
ENV JAVA_VERSION=8.0.8.26
# Tue, 18 Jun 2024 18:55:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9184a6a2be733e8fdb8316f6afcd373c88749c0ec154823ffff45103e528bd6d';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='995426328cc8b7d29dbe4611a1876abbae5f345dcbb2ab6126dcfff5c7985098';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='65ba530a8fc6750c928594ac37fdfeb465f2b5f46bbf809d24353e68e82617fe';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='8985c1fd333d8aef810af8c21acb775e12d741dfffc34aacc3fa4f27440b157f';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 18 Jun 2024 18:55:44 GMT
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
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238ad37218bc956fdddeacd0ff6a9c47df9d4479440ce4cd460da448cca0c28a`  
		Last Modified: Tue, 02 Jul 2024 03:03:41 GMT  
		Size: 1.4 MB (1438241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ba472852db631f821c233a385189185488282c173d367733a7581860cf2392`  
		Last Modified: Tue, 02 Jul 2024 03:03:45 GMT  
		Size: 135.0 MB (135019663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb94ceaf68bd3031ecf6601492818ef683107e26a7eeb621c1ac4def129cf20`  
		Last Modified: Tue, 02 Jul 2024 04:12:52 GMT  
		Size: 113.3 KB (113349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb5e356b3e10cf0281b1ca466c83798f60b983fd8e98fd3876a48dd6d5a739d`  
		Last Modified: Tue, 02 Jul 2024 04:12:52 GMT  
		Size: 17.4 MB (17375315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3abc5b0298a40ec135a6fd9321a53c956a63068574fe52b1fb4a22825fc4cc35`  
		Last Modified: Tue, 02 Jul 2024 04:12:52 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10eb3f7353f7c6e0d9e2f70b82cb6a86f4309179bd87a2dab59280200914a2fb`  
		Last Modified: Tue, 02 Jul 2024 04:12:53 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a7f0c22df1cf926425fbb2e5d2f066600f8dca85fd9479f3369b47581f9ff0`  
		Last Modified: Tue, 02 Jul 2024 04:12:53 GMT  
		Size: 11.8 KB (11833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d77f6462802c2fda3b4a5e8212d2218368049795a6372d1255dd5ea0199e94`  
		Last Modified: Tue, 02 Jul 2024 04:12:53 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585cb4762593f8229a1c8050be28306e4a9b242c95cad3f90919ddbe8a9adda1`  
		Last Modified: Tue, 02 Jul 2024 04:12:53 GMT  
		Size: 12.6 KB (12636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269049ca05fa6a044754d847adc2824103274ddaeac284b6b9c27100352b0a8f`  
		Last Modified: Tue, 02 Jul 2024 04:12:53 GMT  
		Size: 5.8 MB (5807438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:76983547130addf982f22333dee039a55e590de17b40fda71e5f5551afd068b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2143125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc1d656ecfd88862a86047acf85774ee586b25212913feb8f99eef0e862009f`

```dockerfile
```

-	Layers:
	-	`sha256:6938c97b56560e1043d7ee81786a9524c97e5d6cfb686d689af0828aa9c85b71`  
		Last Modified: Tue, 02 Jul 2024 04:12:52 GMT  
		Size: 2.1 MB (2105008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e911454f556abe9b30c3785d3e910fe2113ddb5bb47fc9e1f1e886ca9fb72e43`  
		Last Modified: Tue, 02 Jul 2024 04:12:52 GMT  
		Size: 38.1 KB (38117 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:377ea27d6d8b36ddd67bb67d91274b41769ec33646054683b46410d5ef328506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 MB (194260907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8f8adcea10f342c9d195c035643bcc31f4642e657dc9e672f75fb42c85af39`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 18 Jun 2024 18:55:44 GMT
ARG RELEASE
# Tue, 18 Jun 2024 18:55:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 18:55:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 18:55:44 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 18 Jun 2024 18:55:44 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Tue, 18 Jun 2024 18:55:44 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 18:55:44 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 18 Jun 2024 18:55:44 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 18:55:44 GMT
ENV JAVA_VERSION=8.0.8.26
# Tue, 18 Jun 2024 18:55:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9184a6a2be733e8fdb8316f6afcd373c88749c0ec154823ffff45103e528bd6d';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='995426328cc8b7d29dbe4611a1876abbae5f345dcbb2ab6126dcfff5c7985098';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='65ba530a8fc6750c928594ac37fdfeb465f2b5f46bbf809d24353e68e82617fe';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='8985c1fd333d8aef810af8c21acb775e12d741dfffc34aacc3fa4f27440b157f';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 18 Jun 2024 18:55:44 GMT
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
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b73fe39aa7190a4c3d9ca1d0ac575d106d4b883ca1d2e6fbd1bc4a27f3ead93`  
		Last Modified: Tue, 02 Jul 2024 10:41:25 GMT  
		Size: 1.5 MB (1523343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c039e649d90526676156eadaf6e5be4448cf66e08ffc5813ca1cfb7f5f8936`  
		Last Modified: Tue, 02 Jul 2024 10:41:29 GMT  
		Size: 135.5 MB (135494045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ee2023b25fa2c198031a4712e54632eb68b89f74ed85ae0bcb84452d690950`  
		Last Modified: Wed, 03 Jul 2024 03:13:04 GMT  
		Size: 117.9 KB (117904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3707a6415933610c33a4a9e9b81719d1e83575f085c74514b5a35eb8031b0082`  
		Last Modified: Wed, 03 Jul 2024 03:13:05 GMT  
		Size: 17.4 MB (17375828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20dd8f5374ea8064639a356cec34cbd8fb56ed2c445c9b61c0bd7959e7d45a69`  
		Last Modified: Wed, 03 Jul 2024 03:13:04 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc44d7ca135db26d99d07fa8fa06a0dcf5e30e3a1b707c1d686b3fd032d988`  
		Last Modified: Wed, 03 Jul 2024 03:13:04 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33506d86e3739d8206ca304abb935444f549b9cf5dad3dbf3cf5ad4790fe08c`  
		Last Modified: Wed, 03 Jul 2024 03:13:05 GMT  
		Size: 11.8 KB (11839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946751430d6bcdca04b669adbce1933077123da00d58dfab2dfdc69993eb6b44`  
		Last Modified: Wed, 03 Jul 2024 03:13:05 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1882e0ccbd313b80728b656a3c961cf8a80ba1d1ed64f1af07b6c120045e47e`  
		Last Modified: Wed, 03 Jul 2024 03:13:05 GMT  
		Size: 12.7 KB (12651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1223380d048fb69d39ede963eb74899d0202b054b42d5633f94d1635953b444c`  
		Last Modified: Wed, 03 Jul 2024 03:13:07 GMT  
		Size: 5.3 MB (5261863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:3ab85e0d09c28034b9e4aa57c1461e7bcfa11c8fd0985e99fdcf4bb4225767b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2145592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752e9f2588bfedaf085a770dfb240f8b5a847fa048d9b537e552774c753f929a`

```dockerfile
```

-	Layers:
	-	`sha256:93eb0f19c2b0eca8434ad3326b6a6003b42b045d09cd73c233cc380fe36b0817`  
		Last Modified: Wed, 03 Jul 2024 03:13:04 GMT  
		Size: 2.1 MB (2107430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20f0a727d06d6617cf0df77b8682ae2b1b4643d005426131c7e800bcbdc7ad16`  
		Last Modified: Wed, 03 Jul 2024 03:13:04 GMT  
		Size: 38.2 KB (38162 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:e318f7d6cd0a51db6469a43523e8eced1240044c283989cd022ec1da60b1249a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184554839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54399caab42ad8a01feb95949bdec207dd3480139dad12b13bd23ee0f7a3099`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 18 Jun 2024 18:55:44 GMT
ARG RELEASE
# Tue, 18 Jun 2024 18:55:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 18:55:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 18:55:44 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 18 Jun 2024 18:55:44 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Tue, 18 Jun 2024 18:55:44 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 18:55:44 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 18 Jun 2024 18:55:44 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 18:55:44 GMT
ENV JAVA_VERSION=8.0.8.26
# Tue, 18 Jun 2024 18:55:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9184a6a2be733e8fdb8316f6afcd373c88749c0ec154823ffff45103e528bd6d';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='995426328cc8b7d29dbe4611a1876abbae5f345dcbb2ab6126dcfff5c7985098';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='65ba530a8fc6750c928594ac37fdfeb465f2b5f46bbf809d24353e68e82617fe';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='8985c1fd333d8aef810af8c21acb775e12d741dfffc34aacc3fa4f27440b157f';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 18 Jun 2024 18:55:44 GMT
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
```

-	Layers:
	-	`sha256:bc95fae2023d2ac4f35628ab3a262084bf2801462adfa6e7304b2b4e70ff4ab1`  
		Last Modified: Thu, 27 Jun 2024 20:18:52 GMT  
		Size: 28.0 MB (28000540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30ad7703edfb983f72e74e56d3ba233db0435a1290037a46c332cd69db5ad6f`  
		Last Modified: Tue, 02 Jul 2024 06:07:56 GMT  
		Size: 1.4 MB (1441883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9f543b0489a8d3dd976994e8c395210f934f9cd74749fb1adb7dc0b3f915eb`  
		Last Modified: Tue, 02 Jul 2024 06:07:58 GMT  
		Size: 131.8 MB (131775570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c4a4cdbec2a67617d40e5e46270f8a2be8813fc679a9db9c0b892283e84b94`  
		Last Modified: Tue, 02 Jul 2024 20:56:09 GMT  
		Size: 114.6 KB (114634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d5adf40817c1ea42b6b57036854db5aa5fa69c5dc7f398dd407854d91b3a5e`  
		Last Modified: Tue, 02 Jul 2024 20:56:09 GMT  
		Size: 17.4 MB (17375394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69ce4767ccffd876650a2457d11f10c87f48f1bfb9253a3d95b2f8bffcc3957`  
		Last Modified: Tue, 02 Jul 2024 20:56:09 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303aafbc9020cdd7bc0abacba888bdf5c6c1cc99a41c36b10506c11e4138d74d`  
		Last Modified: Tue, 02 Jul 2024 20:56:09 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14196954e591ba060664ce21bf34319aca28f6cca0d4ebd2b0315436f334e572`  
		Last Modified: Tue, 02 Jul 2024 20:56:10 GMT  
		Size: 11.8 KB (11835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d803117dcf881878459d3129848006c9bfef5a7890789777df64bb266b337f8f`  
		Last Modified: Tue, 02 Jul 2024 20:56:10 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fa5b2db7888e63c7ab5f95fcf94142daadb4675c701a52304fdcc57a0e7c62`  
		Last Modified: Tue, 02 Jul 2024 20:56:10 GMT  
		Size: 12.7 KB (12651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c797efc522305afc64d590914e85aabd69d16b74ba8376d081726c0628d60a10`  
		Last Modified: Tue, 02 Jul 2024 20:56:10 GMT  
		Size: 5.8 MB (5819979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:d685f5a2d2d6dce14ffe8470feed196e24ac6ddc78a88946372cb80c2291cdad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2140683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ee85c1beecc60d736c50a56c53132a48a6a9ba9825e9e722e2c4dbbc81b928`

```dockerfile
```

-	Layers:
	-	`sha256:334afc8e7218bb51734f6b60497e1a99bafe55b8f7e05687ab382047df062ed4`  
		Last Modified: Tue, 02 Jul 2024 20:56:09 GMT  
		Size: 2.1 MB (2102566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc7308241c35d9dc98c5361d83c978de605a39588de4fcfe20f496714ed8322e`  
		Last Modified: Tue, 02 Jul 2024 20:56:09 GMT  
		Size: 38.1 KB (38117 bytes)  
		MIME: application/vnd.in-toto+json
