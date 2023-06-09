## `websphere-liberty:full-java17-openj9`

```console
$ docker pull websphere-liberty@sha256:0cdd4e64519e01fbead18341065991454f174eb4385ab75dce4615c11f2fe57f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:full-java17-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:6e7d739af519d2524ec0a547bc81b49e5704b9183854a0d553f662757ce2334f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.1 MB (489079874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91d59327ac56ea43db1fe9b91fa501fd7e77dd0eb4712b7072692d2c6e15129f`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:46:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:46:22 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:49:49 GMT
ENV JAVA_VERSION=jdk-17.0.6+10_openj9-0.36.0
# Tue, 18 Apr 2023 01:50:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='492bd87e39fc0eb78218746e98c4c0f6730af9c998b872c1a175c0e907d11510';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.6%2B10_openj9-0.36.0/ibm-semeru-open-jre_aarch64_linux_17.0.6_10_openj9-0.36.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='f1342b0a8b472d2de6e882030d2797b9c37e1cd7a90e4cb0c3bd969d4cf8158c';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.6%2B10_openj9-0.36.0/ibm-semeru-open-jre_ppc64le_linux_17.0.6_10_openj9-0.36.0.tar.gz';          ;;        amd64|x86_64)          ESUM='69ca1728f9aad7031908bd9a939b5a9a9c5e931d65bb5c72cbe6f599c7d00cc6';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.6%2B10_openj9-0.36.0/ibm-semeru-open-jre_x64_linux_17.0.6_10_openj9-0.36.0.tar.gz';          ;;        s390x)          ESUM='542359aebfb91b6605c67db6523b2ce154bda63f7fa8a6c243944b2091f4eb2b';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.6%2B10_openj9-0.36.0/ibm-semeru-open-jre_s390x_linux_17.0.6_10_openj9-0.36.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 18 Apr 2023 01:50:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:50:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 18 Apr 2023 01:51:21 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Tue, 18 Apr 2023 06:56:20 GMT
ARG VERBOSE=false
# Tue, 18 Apr 2023 06:56:20 GMT
ARG OPENJ9_SCC=true
# Thu, 04 May 2023 16:31:51 GMT
ARG EN_SHA=d7580938d35387110e39c3c8b3bb5c1f8dc9f0418a2f77799dbcf69a2ab63093
# Thu, 04 May 2023 16:31:51 GMT
ARG NON_IBM_SHA=0d97a3e5cf5403a9b3be514509977f4e9be4a2ac4258e692ef8e64761910f4c0
# Thu, 04 May 2023 16:31:51 GMT
ARG NOTICES_SHA=71f58dc38b4c9b60beaec4459b97b0d08228ad8e5fe5e3a0f4fd7e7c66285925
# Thu, 04 May 2023 16:31:51 GMT
LABEL org.opencontainers.image.authors=Chris Potter, Christy Jesuraj, Melissa Lee org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=23.0.0.4 org.opencontainers.image.revision=cl230420230418-0035 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 04 May 2023 16:31:51 GMT
ENV LIBERTY_VERSION=23.0.0_04
# Thu, 04 May 2023 16:31:51 GMT
ARG LIBERTY_URL
# Thu, 04 May 2023 16:31:51 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 04 May 2023 16:32:05 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=d7580938d35387110e39c3c8b3bb5c1f8dc9f0418a2f77799dbcf69a2ab63093 NON_IBM_SHA=0d97a3e5cf5403a9b3be514509977f4e9be4a2ac4258e692ef8e64761910f4c0 NOTICES_SHA=71f58dc38b4c9b60beaec4459b97b0d08228ad8e5fe5e3a0f4fd7e7c66285925 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 16:32:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Thu, 04 May 2023 16:32:05 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=23.0.0.4 BuildLabel=cl230420230418-0035
# Thu, 04 May 2023 16:32:05 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 04 May 2023 16:32:06 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=d7580938d35387110e39c3c8b3bb5c1f8dc9f0418a2f77799dbcf69a2ab63093 NON_IBM_SHA=0d97a3e5cf5403a9b3be514509977f4e9be4a2ac4258e692ef8e64761910f4c0 NOTICES_SHA=71f58dc38b4c9b60beaec4459b97b0d08228ad8e5fe5e3a0f4fd7e7c66285925 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 04 May 2023 16:32:06 GMT
COPY dir:0f3e336b1e5adb84a625050153035561e1c9802a57b7b90b5a17ebb82adba489 in /opt/ibm/helpers/ 
# Thu, 04 May 2023 16:32:06 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 04 May 2023 16:32:07 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=d7580938d35387110e39c3c8b3bb5c1f8dc9f0418a2f77799dbcf69a2ab63093 NON_IBM_SHA=0d97a3e5cf5403a9b3be514509977f4e9be4a2ac4258e692ef8e64761910f4c0 NOTICES_SHA=71f58dc38b4c9b60beaec4459b97b0d08228ad8e5fe5e3a0f4fd7e7c66285925 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 04 May 2023 16:32:13 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=d7580938d35387110e39c3c8b3bb5c1f8dc9f0418a2f77799dbcf69a2ab63093 NON_IBM_SHA=0d97a3e5cf5403a9b3be514509977f4e9be4a2ac4258e692ef8e64761910f4c0 NOTICES_SHA=71f58dc38b4c9b60beaec4459b97b0d08228ad8e5fe5e3a0f4fd7e7c66285925 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 04 May 2023 16:32:13 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 04 May 2023 16:32:13 GMT
USER 1001
# Thu, 04 May 2023 16:32:13 GMT
EXPOSE 9080 9443
# Thu, 04 May 2023 16:32:13 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 04 May 2023 16:32:13 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 04 May 2023 16:51:36 GMT
ARG VERBOSE=false
# Thu, 04 May 2023 16:51:36 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 04 May 2023 17:00:43 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Thu, 04 May 2023 17:00:44 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Thu, 04 May 2023 17:01:12 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59060db11c04ba6b24aa769f7968a1ff7e5c4029ff838bb2a0c95f83a0c318c2`  
		Last Modified: Tue, 18 Apr 2023 01:54:10 GMT  
		Size: 16.0 MB (16002795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b69597426e81f23b8a8992f8d859f0723f65b1e2e137f9eb726f26d6f77147`  
		Last Modified: Tue, 18 Apr 2023 01:55:50 GMT  
		Size: 48.2 MB (48218475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be43806b8223fc6a690cd269fca157fa48e865925c5ca378aede4b0f4ea2dc93`  
		Last Modified: Tue, 18 Apr 2023 01:55:44 GMT  
		Size: 4.9 MB (4888324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cdc8af6647754c8f750ef3d539fb6603f0aea98a896eae7c8673d1250af5e4a`  
		Last Modified: Thu, 04 May 2023 17:21:59 GMT  
		Size: 14.8 MB (14759648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64add632ba2ec145a315e85f8134e9bc325b4b4b23f219ad31e7634baa5523a0`  
		Last Modified: Thu, 04 May 2023 17:21:55 GMT  
		Size: 678.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b431a15105bd29552e3e4a42fb54054c857dc0890e457aa9716be974eaf84e40`  
		Last Modified: Thu, 04 May 2023 17:21:55 GMT  
		Size: 9.8 KB (9810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5347ad5eb43c81d6267974e6f0087dbcd53bd5a3f57375421a0c2681407f68`  
		Last Modified: Thu, 04 May 2023 17:21:55 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2633dba471182d162b4a2c73d02e8b386fa8cca9fb1745f6df30fb52ca3056bf`  
		Last Modified: Thu, 04 May 2023 17:21:56 GMT  
		Size: 10.8 KB (10796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389968c51e5e394ceadc1c2b94d2f067fb2f7a9c0d8c98d11e8221659fc38b75`  
		Last Modified: Thu, 04 May 2023 17:21:56 GMT  
		Size: 2.7 MB (2651373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e8f356cc6a284d150d43f6804ba62493f9d7fa16c63ceb574cb284aea01763`  
		Last Modified: Thu, 04 May 2023 17:23:09 GMT  
		Size: 359.1 MB (359070120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00289681e68f59db784512ff964d916fe7493e293bd2288c84edb48ded0d3de5`  
		Last Modified: Thu, 04 May 2023 17:22:52 GMT  
		Size: 944.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c789a9b269b0838adaaa092c44e345d98d850c5eb0732b25444c8af048201fb0`  
		Last Modified: Thu, 04 May 2023 17:22:54 GMT  
		Size: 14.9 MB (14888077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full-java17-openj9` - linux; arm64 variant v8

```console
$ docker pull websphere-liberty@sha256:059f45d6ff39a4cb5aabae1472cb1fabe9cca43dc6457f0e9ccdc9ecd10bf202
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.5 MB (484536164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3806f957015445a2ef07bd8ec4034356d576fba9d39d218d5f05639f07f44f`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:45:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:45:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:49:01 GMT
ENV JAVA_VERSION=jdk-17.0.6+10_openj9-0.36.0
# Tue, 18 Apr 2023 01:50:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='492bd87e39fc0eb78218746e98c4c0f6730af9c998b872c1a175c0e907d11510';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.6%2B10_openj9-0.36.0/ibm-semeru-open-jre_aarch64_linux_17.0.6_10_openj9-0.36.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='f1342b0a8b472d2de6e882030d2797b9c37e1cd7a90e4cb0c3bd969d4cf8158c';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.6%2B10_openj9-0.36.0/ibm-semeru-open-jre_ppc64le_linux_17.0.6_10_openj9-0.36.0.tar.gz';          ;;        amd64|x86_64)          ESUM='69ca1728f9aad7031908bd9a939b5a9a9c5e931d65bb5c72cbe6f599c7d00cc6';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.6%2B10_openj9-0.36.0/ibm-semeru-open-jre_x64_linux_17.0.6_10_openj9-0.36.0.tar.gz';          ;;        s390x)          ESUM='542359aebfb91b6605c67db6523b2ce154bda63f7fa8a6c243944b2091f4eb2b';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.6%2B10_openj9-0.36.0/ibm-semeru-open-jre_s390x_linux_17.0.6_10_openj9-0.36.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 18 Apr 2023 01:50:04 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:50:05 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 18 Apr 2023 01:50:39 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 04 May 2023 09:01:06 GMT
ARG VERBOSE=false
# Thu, 04 May 2023 09:01:06 GMT
ARG OPENJ9_SCC=true
# Thu, 04 May 2023 09:01:06 GMT
ARG EN_SHA=d7580938d35387110e39c3c8b3bb5c1f8dc9f0418a2f77799dbcf69a2ab63093
# Thu, 04 May 2023 09:01:06 GMT
ARG NON_IBM_SHA=0d97a3e5cf5403a9b3be514509977f4e9be4a2ac4258e692ef8e64761910f4c0
# Thu, 04 May 2023 09:01:06 GMT
ARG NOTICES_SHA=71f58dc38b4c9b60beaec4459b97b0d08228ad8e5fe5e3a0f4fd7e7c66285925
# Thu, 04 May 2023 09:01:06 GMT
LABEL org.opencontainers.image.authors=Chris Potter, Christy Jesuraj, Melissa Lee org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=23.0.0.4 org.opencontainers.image.revision=cl230420230418-0035 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 04 May 2023 09:01:07 GMT
ENV LIBERTY_VERSION=23.0.0_04
# Thu, 04 May 2023 09:01:07 GMT
ARG LIBERTY_URL
# Thu, 04 May 2023 09:01:07 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 04 May 2023 09:01:19 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=d7580938d35387110e39c3c8b3bb5c1f8dc9f0418a2f77799dbcf69a2ab63093 NON_IBM_SHA=0d97a3e5cf5403a9b3be514509977f4e9be4a2ac4258e692ef8e64761910f4c0 NOTICES_SHA=71f58dc38b4c9b60beaec4459b97b0d08228ad8e5fe5e3a0f4fd7e7c66285925 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 09:01:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Thu, 04 May 2023 09:01:19 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=23.0.0.4 BuildLabel=cl230420230418-0035
# Thu, 04 May 2023 09:01:19 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 04 May 2023 09:01:19 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=d7580938d35387110e39c3c8b3bb5c1f8dc9f0418a2f77799dbcf69a2ab63093 NON_IBM_SHA=0d97a3e5cf5403a9b3be514509977f4e9be4a2ac4258e692ef8e64761910f4c0 NOTICES_SHA=71f58dc38b4c9b60beaec4459b97b0d08228ad8e5fe5e3a0f4fd7e7c66285925 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 04 May 2023 09:01:20 GMT
COPY dir:0f3e336b1e5adb84a625050153035561e1c9802a57b7b90b5a17ebb82adba489 in /opt/ibm/helpers/ 
# Thu, 04 May 2023 09:01:20 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 04 May 2023 09:01:20 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=d7580938d35387110e39c3c8b3bb5c1f8dc9f0418a2f77799dbcf69a2ab63093 NON_IBM_SHA=0d97a3e5cf5403a9b3be514509977f4e9be4a2ac4258e692ef8e64761910f4c0 NOTICES_SHA=71f58dc38b4c9b60beaec4459b97b0d08228ad8e5fe5e3a0f4fd7e7c66285925 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 04 May 2023 09:01:24 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=d7580938d35387110e39c3c8b3bb5c1f8dc9f0418a2f77799dbcf69a2ab63093 NON_IBM_SHA=0d97a3e5cf5403a9b3be514509977f4e9be4a2ac4258e692ef8e64761910f4c0 NOTICES_SHA=71f58dc38b4c9b60beaec4459b97b0d08228ad8e5fe5e3a0f4fd7e7c66285925 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 04 May 2023 09:01:25 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 04 May 2023 09:01:25 GMT
USER 1001
# Thu, 04 May 2023 09:01:25 GMT
EXPOSE 9080 9443
# Thu, 04 May 2023 09:01:25 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 04 May 2023 09:01:25 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 04 May 2023 09:11:21 GMT
ARG VERBOSE=false
# Thu, 04 May 2023 09:11:22 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 04 May 2023 09:20:31 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Thu, 04 May 2023 09:20:34 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Thu, 04 May 2023 09:20:57 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:2378679266ac5157323158b6e52e7a884e559db5217037e57992e47a1667d525`  
		Last Modified: Fri, 14 Apr 2023 07:39:20 GMT  
		Size: 27.2 MB (27196396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7751d4fbf2062d96159da55aa2a9331cd03b66d2d7a5bae5db82dd2693de8cb5`  
		Last Modified: Tue, 18 Apr 2023 01:53:16 GMT  
		Size: 15.9 MB (15865841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14cf99bcb696e2b3db477787e19cc4caba82db9c1e06c71d69bfda8bba8aa59a`  
		Last Modified: Tue, 18 Apr 2023 01:54:44 GMT  
		Size: 46.4 MB (46435138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450dadaefa25ce9d71bdc68815bd7473c5819574c61531ed7796c0aac8dd85a0`  
		Last Modified: Tue, 18 Apr 2023 01:54:39 GMT  
		Size: 4.6 MB (4576737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f33a03ff0fc6855e27d4aad8426841e3d3975b65f4b37645394edf462241f30`  
		Last Modified: Thu, 04 May 2023 09:59:48 GMT  
		Size: 14.7 MB (14749576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37eee167486d44d8824b6690f2765ff0ba0b006ca3f169cd6cc70c5dc131afe`  
		Last Modified: Thu, 04 May 2023 09:59:45 GMT  
		Size: 675.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7511526f8105db7a339e2f0b61838746d72610aa9f0bdcd792feea98f021c06`  
		Last Modified: Thu, 04 May 2023 09:59:46 GMT  
		Size: 9.8 KB (9817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384b07c1fd643dd853357960f845ed52ade3e2c5806cc3394fa9d6d875894c21`  
		Last Modified: Thu, 04 May 2023 09:59:45 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1859c7ddb3e416e8040fb8140db1bbcded904d82071d6c6793ed98c54a19d6aa`  
		Last Modified: Thu, 04 May 2023 09:59:45 GMT  
		Size: 10.8 KB (10794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007348b41b44b52152cfbfb82a7e330a753574bbc8e5fd0edd372d2f25b70458`  
		Last Modified: Thu, 04 May 2023 09:59:46 GMT  
		Size: 2.6 MB (2589376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b9a3c17b0fdac4c5d0b0fdb1a39f51b35a023b8b274cb1014f772aba5efca6`  
		Last Modified: Thu, 04 May 2023 10:00:28 GMT  
		Size: 359.1 MB (359070523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb5b0eb5a90d5dc5a340563fd9427831c8531b572eaed7f7273f6b3ec0136e9`  
		Last Modified: Thu, 04 May 2023 10:00:14 GMT  
		Size: 947.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888506e5228f5750bf2bd58b7e29f78c716c2c0d8961e70f1165592593caf1c8`  
		Last Modified: Thu, 04 May 2023 10:00:16 GMT  
		Size: 14.0 MB (14030073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full-java17-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:4fe6418b429d8cb5214c8aafdff87d337d8cfc8f5ca13b30abaf39d86e7b3b1b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.0 MB (493003849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c62c4e077835d4d77ca6f73bf57d4bc342d5ce75294979a4d32e64925a1764a3`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:24:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:25:21 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:29:26 GMT
ENV JAVA_VERSION=jdk-17.0.6+10_openj9-0.36.0
# Tue, 18 Apr 2023 01:30:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='492bd87e39fc0eb78218746e98c4c0f6730af9c998b872c1a175c0e907d11510';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.6%2B10_openj9-0.36.0/ibm-semeru-open-jre_aarch64_linux_17.0.6_10_openj9-0.36.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='f1342b0a8b472d2de6e882030d2797b9c37e1cd7a90e4cb0c3bd969d4cf8158c';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.6%2B10_openj9-0.36.0/ibm-semeru-open-jre_ppc64le_linux_17.0.6_10_openj9-0.36.0.tar.gz';          ;;        amd64|x86_64)          ESUM='69ca1728f9aad7031908bd9a939b5a9a9c5e931d65bb5c72cbe6f599c7d00cc6';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.6%2B10_openj9-0.36.0/ibm-semeru-open-jre_x64_linux_17.0.6_10_openj9-0.36.0.tar.gz';          ;;        s390x)          ESUM='542359aebfb91b6605c67db6523b2ce154bda63f7fa8a6c243944b2091f4eb2b';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.6%2B10_openj9-0.36.0/ibm-semeru-open-jre_s390x_linux_17.0.6_10_openj9-0.36.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 18 Apr 2023 01:30:48 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:30:48 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 18 Apr 2023 01:31:26 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Tue, 18 Apr 2023 03:23:00 GMT
ARG VERBOSE=false
# Tue, 18 Apr 2023 03:23:00 GMT
ARG OPENJ9_SCC=true
# Thu, 04 May 2023 20:39:48 GMT
ARG EN_SHA=d7580938d35387110e39c3c8b3bb5c1f8dc9f0418a2f77799dbcf69a2ab63093
# Thu, 04 May 2023 20:39:48 GMT
ARG NON_IBM_SHA=0d97a3e5cf5403a9b3be514509977f4e9be4a2ac4258e692ef8e64761910f4c0
# Thu, 04 May 2023 20:39:49 GMT
ARG NOTICES_SHA=71f58dc38b4c9b60beaec4459b97b0d08228ad8e5fe5e3a0f4fd7e7c66285925
# Thu, 04 May 2023 20:39:49 GMT
LABEL org.opencontainers.image.authors=Chris Potter, Christy Jesuraj, Melissa Lee org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=23.0.0.4 org.opencontainers.image.revision=cl230420230418-0035 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 04 May 2023 20:39:50 GMT
ENV LIBERTY_VERSION=23.0.0_04
# Thu, 04 May 2023 20:39:50 GMT
ARG LIBERTY_URL
# Thu, 04 May 2023 20:39:50 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 04 May 2023 20:40:30 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=d7580938d35387110e39c3c8b3bb5c1f8dc9f0418a2f77799dbcf69a2ab63093 NON_IBM_SHA=0d97a3e5cf5403a9b3be514509977f4e9be4a2ac4258e692ef8e64761910f4c0 NOTICES_SHA=71f58dc38b4c9b60beaec4459b97b0d08228ad8e5fe5e3a0f4fd7e7c66285925 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 20:40:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Thu, 04 May 2023 20:40:32 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=23.0.0.4 BuildLabel=cl230420230418-0035
# Thu, 04 May 2023 20:40:32 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 04 May 2023 20:40:35 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=d7580938d35387110e39c3c8b3bb5c1f8dc9f0418a2f77799dbcf69a2ab63093 NON_IBM_SHA=0d97a3e5cf5403a9b3be514509977f4e9be4a2ac4258e692ef8e64761910f4c0 NOTICES_SHA=71f58dc38b4c9b60beaec4459b97b0d08228ad8e5fe5e3a0f4fd7e7c66285925 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 04 May 2023 20:40:36 GMT
COPY dir:0f3e336b1e5adb84a625050153035561e1c9802a57b7b90b5a17ebb82adba489 in /opt/ibm/helpers/ 
# Thu, 04 May 2023 20:40:36 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 04 May 2023 20:40:37 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=d7580938d35387110e39c3c8b3bb5c1f8dc9f0418a2f77799dbcf69a2ab63093 NON_IBM_SHA=0d97a3e5cf5403a9b3be514509977f4e9be4a2ac4258e692ef8e64761910f4c0 NOTICES_SHA=71f58dc38b4c9b60beaec4459b97b0d08228ad8e5fe5e3a0f4fd7e7c66285925 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 04 May 2023 20:40:50 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=d7580938d35387110e39c3c8b3bb5c1f8dc9f0418a2f77799dbcf69a2ab63093 NON_IBM_SHA=0d97a3e5cf5403a9b3be514509977f4e9be4a2ac4258e692ef8e64761910f4c0 NOTICES_SHA=71f58dc38b4c9b60beaec4459b97b0d08228ad8e5fe5e3a0f4fd7e7c66285925 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 04 May 2023 20:40:50 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 04 May 2023 20:40:51 GMT
USER 1001
# Thu, 04 May 2023 20:40:51 GMT
EXPOSE 9080 9443
# Thu, 04 May 2023 20:40:52 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 04 May 2023 20:40:53 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 04 May 2023 21:18:54 GMT
ARG VERBOSE=false
# Thu, 04 May 2023 21:18:54 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 04 May 2023 21:37:14 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Thu, 04 May 2023 21:37:20 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Thu, 04 May 2023 21:38:20 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:d276072145993a42aed3e2b3e8cd26b6e08aab266d9c9d792ee89b26150681da`  
		Last Modified: Fri, 14 Apr 2023 09:36:00 GMT  
		Size: 33.3 MB (33300980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a328f93092ceadb7a1b931cc278addf4dfae1321b9f8ced8d4ea73dc90facfb`  
		Last Modified: Tue, 18 Apr 2023 01:34:37 GMT  
		Size: 17.2 MB (17176898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc4fe87f3e1ae2088dbb6c1d240f2210894fcfc5f16fc53893a903ceb8e8ca2`  
		Last Modified: Tue, 18 Apr 2023 01:37:05 GMT  
		Size: 49.3 MB (49325137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788f22ea43e560dcd86481b6db76e207091483f89d2d61dd6eacac91dda99a38`  
		Last Modified: Tue, 18 Apr 2023 01:36:53 GMT  
		Size: 3.8 MB (3761938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726c19526972445fce2a3a132fa9cce9c73ffc122c45834112f5d24005e64984`  
		Last Modified: Thu, 04 May 2023 22:18:41 GMT  
		Size: 14.8 MB (14781498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7524355d7b3a8c49e95d956cdad08de0f8d20f84df3d83f870177a7ec257541`  
		Last Modified: Thu, 04 May 2023 22:18:37 GMT  
		Size: 679.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd132d0f272c7a412fa32ab0b0faf646bdd74e0db07af094e51faf014466a513`  
		Last Modified: Thu, 04 May 2023 22:18:37 GMT  
		Size: 9.8 KB (9816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd5e036897f636897a20b537fa3a24cf78a0ea48c381df729382434ba3e7259`  
		Last Modified: Thu, 04 May 2023 22:18:37 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d87facea8a5c01a2130c79039484ab7fe94ad70cc8ca7920544c7161f45366`  
		Last Modified: Thu, 04 May 2023 22:18:37 GMT  
		Size: 10.8 KB (10803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9b99ed1dc83c357954a73261a42b21262ca736014952bbc53bf8e64a0becd0`  
		Last Modified: Thu, 04 May 2023 22:18:38 GMT  
		Size: 2.6 MB (2575053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b0e5988a692d4b8121a4ccbe54d092253cc158eb0a58fd9f30ef7373c21915`  
		Last Modified: Thu, 04 May 2023 22:20:38 GMT  
		Size: 359.1 MB (359072074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ef602414936166a8b7fdcc58f645efc5b2c680ee2769c7479eda8a056c2fc7`  
		Last Modified: Thu, 04 May 2023 22:20:07 GMT  
		Size: 947.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d15be90d2381c61d7cae89279cb89fc4e1ccaf3d28a04d67f64242a5c63e3d`  
		Last Modified: Thu, 04 May 2023 22:20:10 GMT  
		Size: 13.0 MB (12987753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full-java17-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:68d7a31b582fa392ea7fe2830fd87009c302e0d924ef466bc7ee9fd99027c8b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.0 MB (491955673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:790b5c38919af14c6a6ebc93250bb81c4ed5b504c2c0b365ce8e1944574bde30`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:35 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:37 GMT
ADD file:44c66c03ba0afcc05de1b2078f83e8bfe04706b31491fcd3fdd93cfc88d5f06c in / 
# Thu, 13 Apr 2023 13:09:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:20:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:20:42 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 31 May 2023 23:52:03 GMT
ENV JAVA_VERSION=jdk-17.0.7+8_openj9-0.38.0
# Wed, 31 May 2023 23:52:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='601dba428fe9d9b5a883aaccbdd37f88c1fb0da2e5b5de65b40cf0a4a0e5fccb';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.7%2B7_openj9-0.38.0/ibm-semeru-open-jre_aarch64_linux_17.0.7_7_openj9-0.38.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='dee6b87258ceba918543956dddf97291cbc2735ffa0288d25239a07c7766d567';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.7%2B7_openj9-0.38.0/ibm-semeru-open-jre_ppc64le_linux_17.0.7_7_openj9-0.38.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ffda41aa8390d14edbce1775d652f0e4e779df025ac1404c1970802697963aab';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.7%2B7_openj9-0.38.0/ibm-semeru-open-jre_x64_linux_17.0.7_7_openj9-0.38.0.tar.gz';          ;;        s390x)          ESUM='ee08d6830990562fcc45bec336748390d15357028d3ca0cf4a78bcea7bdfaefe';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.7%2B7_openj9-0.38.0/ibm-semeru-open-jre_s390x_linux_17.0.7_7_openj9-0.38.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 31 May 2023 23:52:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 May 2023 23:52:10 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 31 May 2023 23:52:43 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 01 Jun 2023 00:16:08 GMT
ARG VERBOSE=false
# Thu, 01 Jun 2023 00:16:08 GMT
ARG OPENJ9_SCC=true
# Fri, 09 Jun 2023 04:25:22 GMT
ARG EN_SHA=16669604ed86a6ad4bd60b99ca85fad2a819ae3ff3e68d5585a64f3d51504ee3
# Fri, 09 Jun 2023 04:25:22 GMT
ARG NON_IBM_SHA=89faf793b9e068a80bda72d6c1cbf9b4e1362c699525710ae3247a6c135a0b11
# Fri, 09 Jun 2023 04:25:22 GMT
ARG NOTICES_SHA=f02cefd8eb429cd471b9f494c2ac7f3df10ef042f1b7e8271895afd2a46ae997
# Fri, 09 Jun 2023 04:25:22 GMT
LABEL org.opencontainers.image.authors=Chris Potter, Christy Jesuraj, Melissa Lee org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=23.0.0.5 org.opencontainers.image.revision=cl230520230514-1901 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 09 Jun 2023 04:25:22 GMT
ENV LIBERTY_VERSION=23.0.0_05
# Fri, 09 Jun 2023 04:25:22 GMT
ARG LIBERTY_URL
# Fri, 09 Jun 2023 04:25:22 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 09 Jun 2023 04:25:33 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=16669604ed86a6ad4bd60b99ca85fad2a819ae3ff3e68d5585a64f3d51504ee3 NON_IBM_SHA=89faf793b9e068a80bda72d6c1cbf9b4e1362c699525710ae3247a6c135a0b11 NOTICES_SHA=f02cefd8eb429cd471b9f494c2ac7f3df10ef042f1b7e8271895afd2a46ae997 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Jun 2023 04:25:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Fri, 09 Jun 2023 04:25:34 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=23.0.0.5 BuildLabel=cl230520230514-1901
# Fri, 09 Jun 2023 04:25:34 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 09 Jun 2023 04:25:35 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=16669604ed86a6ad4bd60b99ca85fad2a819ae3ff3e68d5585a64f3d51504ee3 NON_IBM_SHA=89faf793b9e068a80bda72d6c1cbf9b4e1362c699525710ae3247a6c135a0b11 NOTICES_SHA=f02cefd8eb429cd471b9f494c2ac7f3df10ef042f1b7e8271895afd2a46ae997 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 09 Jun 2023 04:25:35 GMT
COPY dir:914bfb97242d950c6caece0b64a51887f4841dba2f2ab4120f6cb39eedace555 in /opt/ibm/helpers/ 
# Fri, 09 Jun 2023 04:25:35 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 09 Jun 2023 04:25:35 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=16669604ed86a6ad4bd60b99ca85fad2a819ae3ff3e68d5585a64f3d51504ee3 NON_IBM_SHA=89faf793b9e068a80bda72d6c1cbf9b4e1362c699525710ae3247a6c135a0b11 NOTICES_SHA=f02cefd8eb429cd471b9f494c2ac7f3df10ef042f1b7e8271895afd2a46ae997 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 09 Jun 2023 04:25:39 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=16669604ed86a6ad4bd60b99ca85fad2a819ae3ff3e68d5585a64f3d51504ee3 NON_IBM_SHA=89faf793b9e068a80bda72d6c1cbf9b4e1362c699525710ae3247a6c135a0b11 NOTICES_SHA=f02cefd8eb429cd471b9f494c2ac7f3df10ef042f1b7e8271895afd2a46ae997 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 09 Jun 2023 04:25:39 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 09 Jun 2023 04:25:40 GMT
USER 1001
# Fri, 09 Jun 2023 04:25:40 GMT
EXPOSE 9080 9443
# Fri, 09 Jun 2023 04:25:40 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 09 Jun 2023 04:25:40 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 09 Jun 2023 04:46:46 GMT
ARG VERBOSE=false
# Fri, 09 Jun 2023 04:46:46 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 09 Jun 2023 04:58:58 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Fri, 09 Jun 2023 04:59:04 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 09 Jun 2023 04:59:29 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:f11b609b1d63f2d37c0e3789823e7a7e62a078bddca7c46da8602655989c62d9`  
		Last Modified: Fri, 14 Apr 2023 09:38:39 GMT  
		Size: 27.0 MB (27016370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904a0c815c072ccdf47e2b629d60ff91ad3ae9a1485d39c406b7c5e846233b1c`  
		Last Modified: Tue, 18 Apr 2023 01:29:20 GMT  
		Size: 15.7 MB (15693377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231e4c058ee17ba9fb19647c365495f3d6d9917bee195cf6ea13189a6064ef5e`  
		Last Modified: Wed, 31 May 2023 23:57:25 GMT  
		Size: 47.6 MB (47567686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68000780a2ef5417777d86b9e293b235abd4382a0440acee506af8a88c07ac5`  
		Last Modified: Wed, 31 May 2023 23:57:19 GMT  
		Size: 4.9 MB (4935087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10e556a8d5588f3c54d9cbe9e8fecc4feacc1c7ace05e38edcec8a3c6bc37c2`  
		Last Modified: Fri, 09 Jun 2023 06:01:48 GMT  
		Size: 19.4 MB (19354912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ae14d2f08677ba2786e14a69480cb9d87a446fb4f682a5e67f4994671b1aff`  
		Last Modified: Fri, 09 Jun 2023 06:01:46 GMT  
		Size: 677.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54c81ed4e5ab676d33b2c1437a9d8fbc911aab254c8dc6512069cff15cf325e`  
		Last Modified: Fri, 09 Jun 2023 06:01:46 GMT  
		Size: 10.5 KB (10530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a7051253eae4b1bc9fc9ebf0bf3ea982d1182ea53f93e019561ee556d5b6e0`  
		Last Modified: Fri, 09 Jun 2023 06:01:46 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f405f94dd90ac3063ee2132f228e41af9d97bd85be6c47385902a9df8a794c`  
		Last Modified: Fri, 09 Jun 2023 06:01:46 GMT  
		Size: 11.5 KB (11511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16cd12c4285ba10af8e1725a99e059c54d87c0978d444fc701e5c4b5f2512bf`  
		Last Modified: Fri, 09 Jun 2023 06:01:46 GMT  
		Size: 2.6 MB (2606433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ca0355dc1181c23d73399e00816a8a2b73a9e3d38d7bdc59ec436479766ab8`  
		Last Modified: Fri, 09 Jun 2023 06:02:46 GMT  
		Size: 359.3 MB (359251437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7cd1e9935a5c5cc8e35b0ed8d91e18e6ca2dc374044d6a959c89571e6ee6c9`  
		Last Modified: Fri, 09 Jun 2023 06:02:31 GMT  
		Size: 941.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c294ba694bbca4a1db5d8a608f90d8b3024acd671a3706454d6201b6b7d139`  
		Last Modified: Fri, 09 Jun 2023 06:02:33 GMT  
		Size: 15.5 MB (15506442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
