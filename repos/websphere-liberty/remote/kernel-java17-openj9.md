## `websphere-liberty:kernel-java17-openj9`

```console
$ docker pull websphere-liberty@sha256:11124f3f6ce06a0234fc25e66e615c08c4b657a7ae2d63f9915d93f691e0de14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `websphere-liberty:kernel-java17-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:acbbd5d429f9d9f87e0c7005c650ecb0dadbea8f26b4612bd3588cebbd3541a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118468339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edf2966ca9edaa66928bfd43264433356bae8d11533b25e31a7027952e77e7a5`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 11 Sep 2024 13:44:15 GMT
ARG RELEASE
# Wed, 11 Sep 2024 13:44:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 13:44:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 13:44:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 13:44:15 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 13:44:15 GMT
CMD ["/bin/bash"]
# Wed, 11 Sep 2024 13:44:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 11 Sep 2024 13:44:15 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Sep 2024 13:44:15 GMT
ENV JAVA_VERSION=jdk-17.0.12+7_openj9-0.46.1
# Wed, 11 Sep 2024 13:44:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cb2bfe44358158dcaa903e1f9aeb3e895adc1d5ace1f764e0dc1b1aeb4ffb77e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_aarch64_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='29f969c56c1e82587e0fcb1c0253dec413538c9599eaec9fcdb3983d181aad96';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_ppc64le_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='f218a8e1596197a3e89e9eff3ef4dc3e56ff41d7e293261e02cbc589a418998e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_x64_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='1490c54b365dc1c4bfea47412433df79ebfd2c3f85c9f7b1c88ce2d7ae7dee75';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_s390x_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 11 Sep 2024 13:44:15 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Sep 2024 13:44:15 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 11 Sep 2024 13:44:15 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.95/bin/apache-tomcat-9.0.95.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
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
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 11 Sep 2024 13:44:15 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.9 BuildLabel=cl241020240827-1743
# Wed, 11 Sep 2024 13:44:15 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.9 LIBERTY_BUILD_LABEL=cl241020240827-1743 LIBERTY_SHA=e0f8996103aed984661cde75149f583f80f5f91a
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 11 Sep 2024 13:44:15 GMT
ARG LIBERTY_URL
# Wed, 11 Sep 2024 13:44:15 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 11 Sep 2024 13:44:15 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.9 LIBERTY_BUILD_LABEL=cl241020240827-1743 LIBERTY_SHA=e0f8996103aed984661cde75149f583f80f5f91a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
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
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 11 Sep 2024 13:44:15 GMT
USER 1001
# Wed, 11 Sep 2024 13:44:15 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 11 Sep 2024 13:44:15 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 11 Sep 2024 13:44:15 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2164747e1ff2ca7eac681bf32f49a500610ebae6a7ec62604a1f098051d7b765`  
		Last Modified: Thu, 19 Sep 2024 20:01:39 GMT  
		Size: 12.2 MB (12156493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb949f759267157c8c5b6da2affd1e2fbb45890cb425c73a09ff662b46558b1e`  
		Last Modified: Thu, 19 Sep 2024 20:01:39 GMT  
		Size: 51.5 MB (51534126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a965409154c3ffae601b19ee5aaead25c0246b90b6f423b74baa889aaf1ef80d`  
		Last Modified: Thu, 19 Sep 2024 20:01:39 GMT  
		Size: 4.9 MB (4898019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d6a0b85a204194e3c7c64392296c4e8c6c4a2977de6a85e1054126b9907a19`  
		Last Modified: Thu, 19 Sep 2024 21:00:44 GMT  
		Size: 31.7 KB (31745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10920823ad455c8071c209547671f27855990c9548c9365d29ab96667bf1b87a`  
		Last Modified: Thu, 19 Sep 2024 21:00:45 GMT  
		Size: 17.4 MB (17432172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71fb59715996a6494ebc7bbc464d7756a6f52ad6550d814394f633519601f23`  
		Last Modified: Thu, 19 Sep 2024 21:00:44 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326f94cba005738cb80de4399d1e0f6163e0b7b245862f53566f888841d81e5f`  
		Last Modified: Thu, 19 Sep 2024 21:00:44 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a82cb7db4ecd8fce003d1e1a608496afc8553fb20714e718764d469f23d894`  
		Last Modified: Thu, 19 Sep 2024 21:00:45 GMT  
		Size: 11.8 KB (11832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f62c0abd87ea78230d16d8b5686143c6744fc763bbd832b77f96946a3dd8671`  
		Last Modified: Thu, 19 Sep 2024 21:00:45 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9bcbe10101254d9ade5f8b85120b3581677e02582c7c83f7801daec0ea83a1`  
		Last Modified: Thu, 19 Sep 2024 21:00:45 GMT  
		Size: 12.6 KB (12637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5745462d8e6365733a7f8a40b92eba4f58095625d60cedd51d032e9bdcea6d75`  
		Last Modified: Thu, 19 Sep 2024 21:00:46 GMT  
		Size: 2.9 MB (2853382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:49c72f0e6489922e5fb8db73052c9ad5c6ac1bab3d808456589c0ac2699c8aae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 KB (41709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a96c4c6b201ec162aeb3b59ec572fa3920a5e3f6d52675487983953149a658e`

```dockerfile
```

-	Layers:
	-	`sha256:c9c8e44ea344ba1efbbbf44c3a77eb4d1a2b2e11938ac6ffa45fe63bd2ceb8c5`  
		Last Modified: Thu, 19 Sep 2024 21:00:44 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a8bb83916f10517b8d9e2a31ec12c77da0eced0c21840fc987855ae5463971a`  
		Last Modified: Thu, 19 Sep 2024 21:00:45 GMT  
		Size: 40.0 KB (39952 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java17-openj9` - linux; arm64 variant v8

```console
$ docker pull websphere-liberty@sha256:aea4d3f882cd7e9d0f6aa269d964a15b3a77bb2b03aa8829b1a40db1f96ceb1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112364330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdedf47adafbea0e5a9ce355323a202949558f7fa516394e78f76ba708aaa722`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 11 Sep 2024 13:44:15 GMT
ARG RELEASE
# Wed, 11 Sep 2024 13:44:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 13:44:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 13:44:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 13:44:15 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 13:44:15 GMT
CMD ["/bin/bash"]
# Wed, 11 Sep 2024 13:44:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 11 Sep 2024 13:44:15 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Sep 2024 13:44:15 GMT
ENV JAVA_VERSION=jdk-17.0.12+7_openj9-0.46.1
# Wed, 11 Sep 2024 13:44:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cb2bfe44358158dcaa903e1f9aeb3e895adc1d5ace1f764e0dc1b1aeb4ffb77e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_aarch64_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='29f969c56c1e82587e0fcb1c0253dec413538c9599eaec9fcdb3983d181aad96';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_ppc64le_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='f218a8e1596197a3e89e9eff3ef4dc3e56ff41d7e293261e02cbc589a418998e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_x64_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='1490c54b365dc1c4bfea47412433df79ebfd2c3f85c9f7b1c88ce2d7ae7dee75';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_s390x_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 11 Sep 2024 13:44:15 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Sep 2024 13:44:15 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 11 Sep 2024 13:44:15 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
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
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 11 Sep 2024 13:44:15 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.9 BuildLabel=cl241020240827-1743
# Wed, 11 Sep 2024 13:44:15 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.9 LIBERTY_BUILD_LABEL=cl241020240827-1743 LIBERTY_SHA=e0f8996103aed984661cde75149f583f80f5f91a
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 11 Sep 2024 13:44:15 GMT
ARG LIBERTY_URL
# Wed, 11 Sep 2024 13:44:15 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 11 Sep 2024 13:44:15 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.9 LIBERTY_BUILD_LABEL=cl241020240827-1743 LIBERTY_SHA=e0f8996103aed984661cde75149f583f80f5f91a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
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
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 11 Sep 2024 13:44:15 GMT
USER 1001
# Wed, 11 Sep 2024 13:44:15 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 11 Sep 2024 13:44:15 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 11 Sep 2024 13:44:15 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3831940244be8baa42f9d6629360ed0326dedeb7d18134cfa77184874d97bf6f`  
		Last Modified: Tue, 17 Sep 2024 02:06:03 GMT  
		Size: 12.1 MB (12114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20642fa5f40650d3b2d9c9ff8d86ea87930c0b986bfbbd31aa92bf919ad6154d`  
		Last Modified: Tue, 17 Sep 2024 02:11:45 GMT  
		Size: 47.9 MB (47916904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475ec2945666c59e1a51afae49ba6bac930e0498b6086118dac325c96245df7f`  
		Last Modified: Tue, 17 Sep 2024 02:11:44 GMT  
		Size: 4.7 MB (4712183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f5bab97d0901bba176deb6d6a26d2e2db6c5407aacc78dad12ee240c5a5311`  
		Last Modified: Tue, 17 Sep 2024 07:10:51 GMT  
		Size: 42.3 KB (42323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ca7151931f10e40c409475bb4e999b2f819eafb352cb9a49e1f365c071d302`  
		Last Modified: Tue, 17 Sep 2024 07:10:51 GMT  
		Size: 17.4 MB (17432450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37c6efa2045f11f743d8c4c0b000c568736112f9f293c0cb67cdb295b6d266e`  
		Last Modified: Tue, 17 Sep 2024 07:10:50 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a47c7c481612439b12a02255a1a4629946c171f3000a1fc1523cdcf125a8dc`  
		Last Modified: Tue, 17 Sep 2024 07:10:50 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8cef26c0af9d698666d2feff42529e0b475f80db48b1c0a77d9b695e789bd2d`  
		Last Modified: Tue, 17 Sep 2024 07:10:51 GMT  
		Size: 11.8 KB (11830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6318444b986e123fec60e7e6540d9e340256dafcc29b48789ad325b22c7ea262`  
		Last Modified: Tue, 17 Sep 2024 07:10:51 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf29d4691d9469a943b5b2f6d4844b232671e9f614fbdfa71374bd61a266555e`  
		Last Modified: Tue, 17 Sep 2024 07:10:52 GMT  
		Size: 12.6 KB (12638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20628ca83d3ff6d5cbc0f3bbe3fd06e0c76e089867e7f68e934bf4d353532b1c`  
		Last Modified: Tue, 17 Sep 2024 07:10:53 GMT  
		Size: 2.8 MB (2761126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:c2c46d8fb738774044c0b073ce60cdc2585b8181a67408ac589e03b8ffba4988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acca0827e45bde49ecdc77529e631dd8f3dd38c2c048cf329fd384907ef1fe1c`

```dockerfile
```

-	Layers:
	-	`sha256:5965f4a530a067b0c1ef7f73240f3ba51f99bb4597b4d5a16e9474fe40d34333`  
		Last Modified: Tue, 17 Sep 2024 07:10:51 GMT  
		Size: 3.6 MB (3589060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8a593af8af68c38177b93ae71557fce856d34916cfbaafffb7783d56ac58d48`  
		Last Modified: Tue, 17 Sep 2024 07:10:50 GMT  
		Size: 40.3 KB (40314 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java17-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:313feb21e92b43d805ebece26eb1ee51f5c45c5fdeaf1080ef7ddc723268465b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124403443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94a18baf938e03f1cfd09410e2f52616fcc526919b1c697b39d9c2613911807`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 11 Sep 2024 13:44:15 GMT
ARG RELEASE
# Wed, 11 Sep 2024 13:44:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 13:44:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 13:44:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 13:44:15 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 13:44:15 GMT
CMD ["/bin/bash"]
# Wed, 11 Sep 2024 13:44:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 11 Sep 2024 13:44:15 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Sep 2024 13:44:15 GMT
ENV JAVA_VERSION=jdk-17.0.12+7_openj9-0.46.1
# Wed, 11 Sep 2024 13:44:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cb2bfe44358158dcaa903e1f9aeb3e895adc1d5ace1f764e0dc1b1aeb4ffb77e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_aarch64_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='29f969c56c1e82587e0fcb1c0253dec413538c9599eaec9fcdb3983d181aad96';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_ppc64le_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='f218a8e1596197a3e89e9eff3ef4dc3e56ff41d7e293261e02cbc589a418998e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_x64_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='1490c54b365dc1c4bfea47412433df79ebfd2c3f85c9f7b1c88ce2d7ae7dee75';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_s390x_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 11 Sep 2024 13:44:15 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Sep 2024 13:44:15 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 11 Sep 2024 13:44:15 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
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
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 11 Sep 2024 13:44:15 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.9 BuildLabel=cl241020240827-1743
# Wed, 11 Sep 2024 13:44:15 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.9 LIBERTY_BUILD_LABEL=cl241020240827-1743 LIBERTY_SHA=e0f8996103aed984661cde75149f583f80f5f91a
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 11 Sep 2024 13:44:15 GMT
ARG LIBERTY_URL
# Wed, 11 Sep 2024 13:44:15 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 11 Sep 2024 13:44:15 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.9 LIBERTY_BUILD_LABEL=cl241020240827-1743 LIBERTY_SHA=e0f8996103aed984661cde75149f583f80f5f91a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
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
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 11 Sep 2024 13:44:15 GMT
USER 1001
# Wed, 11 Sep 2024 13:44:15 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 11 Sep 2024 13:44:15 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 11 Sep 2024 13:44:15 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6230a31e14b4a918b32fc7a3b685fad8ecafe0901deee916736d3e6f4db6ad`  
		Last Modified: Tue, 17 Sep 2024 01:15:01 GMT  
		Size: 12.9 MB (12888132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e956f85db15bc3def81b35a583203cdacb3b7c13fc265dacab2f17dd60df77d`  
		Last Modified: Tue, 17 Sep 2024 01:23:56 GMT  
		Size: 53.1 MB (53116177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc43e2388662f4cf6daa94c3976105ece62b24da62d716f0aceefb4fbb97183e`  
		Last Modified: Tue, 17 Sep 2024 01:23:55 GMT  
		Size: 3.8 MB (3775444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f63cb6907756e20d0f260697fbea722d28062d903afb5b119c90ccec14cde1`  
		Last Modified: Tue, 17 Sep 2024 04:27:16 GMT  
		Size: 36.5 KB (36495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ad3b90152ae5618f9d4063bbdddee5ac6c9e29e44ce07021013cf5c6667bf1`  
		Last Modified: Tue, 17 Sep 2024 04:27:17 GMT  
		Size: 17.4 MB (17432780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad387002536895a5aca00ee2190484015c899cdd8604bbd0804cd3469822b485`  
		Last Modified: Tue, 17 Sep 2024 04:27:16 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73990d592ca742b573198e6f9db7f3acf842bf036cf26ae91893d3735b9d4e19`  
		Last Modified: Tue, 17 Sep 2024 04:27:16 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee5bdbe92297e8de2bc18e72ef700f73f63904607e40aa115caf120e6a263f6`  
		Last Modified: Tue, 17 Sep 2024 04:27:17 GMT  
		Size: 11.8 KB (11831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6ae881cb5f1e3a64d615980a4e07e56c85dc2a9a78e8f28d854462de06de23`  
		Last Modified: Tue, 17 Sep 2024 04:27:17 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ba3c5a1d3ee10f3a46ebca77fff45ea5489feb063ec0c709505a5a678337f3`  
		Last Modified: Tue, 17 Sep 2024 04:27:17 GMT  
		Size: 12.6 KB (12638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07898bc9b4ea7d380d1e803d2ebe8a9f78be7c631b66ef2c8d2888569711c284`  
		Last Modified: Tue, 17 Sep 2024 04:27:19 GMT  
		Size: 2.7 MB (2679454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:18628bfde311d771cd4ce22797faf90fcfff6da42e0eaf80bb8077513cbaa386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:527545b49210a11bc72541004dc71645ff9fe1c3e8644e24ab3fb3d1f9ecbccc`

```dockerfile
```

-	Layers:
	-	`sha256:4abfa5428c894528610de62521716c10e6dac4bb7c18ec55e7ef30ad33fdbb9c`  
		Last Modified: Tue, 17 Sep 2024 04:27:17 GMT  
		Size: 3.6 MB (3593283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:172f645870ad796243e8b6e6cee2cdbb65ed46402a7ed8b2256eb668144d4962`  
		Last Modified: Tue, 17 Sep 2024 04:27:16 GMT  
		Size: 40.0 KB (39993 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java17-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:64c384998c6ca5dde7e2acf83963a40749b3033bdc8d21085b796c68ebf79620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.1 MB (116056117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0a9cdc4b103fa6ba4ba2af5e0c6c956299a4b04b20658fec2e8f3a8275ef6f`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 11 Sep 2024 13:44:15 GMT
ARG RELEASE
# Wed, 11 Sep 2024 13:44:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 13:44:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 13:44:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 13:44:15 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 11 Sep 2024 13:44:15 GMT
CMD ["/bin/bash"]
# Wed, 11 Sep 2024 13:44:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 11 Sep 2024 13:44:15 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Sep 2024 13:44:15 GMT
ENV JAVA_VERSION=jdk-17.0.12+7_openj9-0.46.1
# Wed, 11 Sep 2024 13:44:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cb2bfe44358158dcaa903e1f9aeb3e895adc1d5ace1f764e0dc1b1aeb4ffb77e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_aarch64_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='29f969c56c1e82587e0fcb1c0253dec413538c9599eaec9fcdb3983d181aad96';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_ppc64le_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='f218a8e1596197a3e89e9eff3ef4dc3e56ff41d7e293261e02cbc589a418998e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_x64_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='1490c54b365dc1c4bfea47412433df79ebfd2c3f85c9f7b1c88ce2d7ae7dee75';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.12%2B7_openj9-0.46.1/ibm-semeru-open-jre_s390x_linux_17.0.12_7_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 11 Sep 2024 13:44:15 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Sep 2024 13:44:15 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 11 Sep 2024 13:44:15 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.95/bin/apache-tomcat-9.0.95.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
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
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 11 Sep 2024 13:44:15 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.9 BuildLabel=cl241020240827-1743
# Wed, 11 Sep 2024 13:44:15 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.9 LIBERTY_BUILD_LABEL=cl241020240827-1743 LIBERTY_SHA=e0f8996103aed984661cde75149f583f80f5f91a
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 11 Sep 2024 13:44:15 GMT
ARG LIBERTY_URL
# Wed, 11 Sep 2024 13:44:15 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 11 Sep 2024 13:44:15 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.9 LIBERTY_BUILD_LABEL=cl241020240827-1743 LIBERTY_SHA=e0f8996103aed984661cde75149f583f80f5f91a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
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
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 11 Sep 2024 13:44:15 GMT
USER 1001
# Wed, 11 Sep 2024 13:44:15 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 11 Sep 2024 13:44:15 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 11 Sep 2024 13:44:15 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d7fcbb74a18dbda1a95a881c01c2cc4d8a0d6fe38b3b4f8b5899f281f9815e`  
		Last Modified: Tue, 17 Sep 2024 01:57:02 GMT  
		Size: 12.2 MB (12203759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf306d6b55fcd4409a3d7914177a321a344e69fa7c2a2b6fcbfa5871e82a7fab`  
		Last Modified: Tue, 17 Sep 2024 02:04:33 GMT  
		Size: 50.5 MB (50470509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b37cc8f8b8f9d1c5741bfa4a1e93d8c6659c980ab4c801503926c834f02cb30`  
		Last Modified: Thu, 19 Sep 2024 20:15:44 GMT  
		Size: 5.0 MB (5033582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835d8ecc4d3d1e91c1e735a6fc7c8b93f9aa70aca03dab0343a730d425b2d61b`  
		Last Modified: Thu, 19 Sep 2024 21:37:40 GMT  
		Size: 33.1 KB (33110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fde4d7c4951c214d8f0bd3cc14c02767b75488c4c3c34129b2ecdf500feded2`  
		Last Modified: Thu, 19 Sep 2024 21:37:41 GMT  
		Size: 17.4 MB (17432372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f5df78ccda066233ed2f3079df59519fcd0868d607c3830ef8420d13cc4018`  
		Last Modified: Thu, 19 Sep 2024 21:37:40 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec024081c70029a1f3cf47f8603166c9bf0e436031081074fe5d5a9f6417bdeb`  
		Last Modified: Thu, 19 Sep 2024 21:37:40 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b169abcfdd4e737ca175e2d4506157a2009b70c4f63b076b33f209f2e09e2478`  
		Last Modified: Thu, 19 Sep 2024 21:37:41 GMT  
		Size: 11.8 KB (11828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d657334b20687c1f097bedafc5984de533903003f8cd2544c971c35343f846e8`  
		Last Modified: Thu, 19 Sep 2024 21:37:41 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0e513d794522d5585dd2ceef5fc83f92977a25e974a7a162fa71474b449ab8`  
		Last Modified: Thu, 19 Sep 2024 21:37:41 GMT  
		Size: 12.6 KB (12635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc5d9684bfdf0c57611da0ea40b989e42a9e0fde5444be3f59b79b7568cdf09`  
		Last Modified: Thu, 19 Sep 2024 21:37:42 GMT  
		Size: 2.9 MB (2854602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:a778750dc275621370c1460c5e10d6373d32fafbc52295a8477bd0eba1acb0ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c3ac7aa6bca066c99de567678cf705ce08921c8cf6d969440ff79aacc2120d`

```dockerfile
```

-	Layers:
	-	`sha256:bcb593a3948a95b81e08fec1e3ed4f3fc9962c5dd04c67645d2a5b88cc029978`  
		Last Modified: Thu, 19 Sep 2024 21:37:40 GMT  
		Size: 3.6 MB (3588834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:391de5c265499c0b06b035a0487b34b58240ea1d88fc482b76e7dff384957db6`  
		Last Modified: Thu, 19 Sep 2024 21:37:40 GMT  
		Size: 40.0 KB (39953 bytes)  
		MIME: application/vnd.in-toto+json
